# Luna Key Persistence Patterns

This note collects the practical Java persistence patterns for `AES`, `RSA`, and `ML-KEM` when working with a Thales Luna provider.

It is intentionally focused on:

- what kind of key object you are persisting
- whether you usually persist one object or a keypair
- which Java keystore pattern fits best
- what is most consistent with the `private key never leaves the HSM` story

## Quick summary

The short version is:

- `AES`: persist a `SecretKey`
- `RSA`: usually persist the private key as a `PrivateKeyEntry` plus certificate chain
- `ML-KEM`: usually persist the recipient keypair, but the exact Java storage model may be more provider-specific than the RSA case

## 1. Persisting an AES key

For a symmetric key such as `AES`, the normal Java keystore model is a secret-key entry.

This is the pattern you mentioned:

```java
KeyGenerator kg = KeyGenerator.getInstance("AES", "LunaProvider");
kg.init(256);

LunaKey key = (LunaKey) kg.generateKey();
myStore.setKeyEntry("myPersistentAESKey", key, null, null);
```

How to think about it:

- there is only one secret key
- there is no public/private pair
- there is no certificate chain involved
- `setKeyEntry(..., key, null, null)` is the normal secret-key style

This is the cleanest persistence model of the three because it maps directly to a single `SecretKey`.

## 2. Persisting an RSA keypair

For RSA, the usual Java keystore pattern is different.

You normally persist the **private key** as a `PrivateKeyEntry`, and that entry requires a certificate chain.
The first certificate in that chain carries the matching public key.

That is why Java and Luna RSA samples typically look like this:

```java
KeyPairGenerator kpg = KeyPairGenerator.getInstance("RSA", "LunaProvider");
kpg.initialize(3072);
KeyPair rsaKeyPair = kpg.generateKeyPair();

X509Certificate selfSigned = generateSelfSignedCertificate(rsaKeyPair);
myStore.setKeyEntry("myPersistentRsaKey", rsaKeyPair.getPrivate(), null, new Certificate[]{selfSigned});
```

What that means:

- yes, you are effectively persisting the keypair
- the private key is the important secret
- the public key is represented through the certificate chain
- Java wants a certificate because this is a `PrivateKeyEntry`, not a secret-key entry

### Why a certificate is involved

The certificate is not there to hide the private key.
It is there because Java `PrivateKeyEntry` requires the matching public-key metadata in certificate form.

So for RSA, the normal Java keystore story is:

- private key entry
- certificate chain
- public key lives in the certificate

## 3. Persisting an ML-KEM keypair

For ML-KEM, the conceptual answer is:

- yes, you usually want to persist the recipient keypair if it is a long-lived decapsulation keypair

Why:

- the decapsulation private key must still exist later
- the matching public key must remain available to senders

So operationally, you usually want to keep:

- the ML-KEM private key persistent on the Luna side
- the matching ML-KEM public key available by alias, provider object, or exportable representation

### The practical difference from RSA

RSA fits Java's classic `PrivateKeyEntry + certificate chain` model very naturally.
ML-KEM does not always fit that model as neatly in current Java ecosystems.

Why:

- RSA has a long-established X.509 and Java keystore story
- ML-KEM is much newer
- some providers may expose ML-KEM persistence through provider-native persistent token objects rather than a polished certificate-backed `PrivateKeyEntry` pattern

So for ML-KEM, the safest practical guidance is:

- conceptually persist the keypair
- operationally use the Luna-supported provider-native persistence model that keeps the private key resident on the Luna side

## Do you typically store both halves of RSA or ML-KEM?

The most accurate answer is:

- conceptually, yes, you are preserving the keypair
- operationally, the private key is the sensitive half
- the public key may be stored, exported, or represented differently depending on the provider model

For RSA:

- the private key is usually persisted as a `PrivateKeyEntry`
- the public key is carried by the certificate

For ML-KEM:

- the private key should remain persistent on the Luna side
- the public key usually needs to remain retrievable or exportable for encapsulation use

## What is the most HSM-aligned way to describe this?

The best wording is usually:

- `AES`: persist a secret key object
- `RSA`: persist a provider-backed private key entry, with certificate carrying the public key
- `ML-KEM`: persist a provider-backed recipient keypair, using the Luna-supported persistent object model

That is much better than saying:

- `just export the key bytes and save them somewhere`

because exporting raw private-key bytes does not match the stronger HSM message.

## Code samples in one place

### AES secret key persistence

```java
KeyStore lunaKeyStore = KeyStore.getInstance("Luna");
KeyGenerator kg = KeyGenerator.getInstance("AES", "LunaProvider");
kg.init(256);

SecretKey aesKey = kg.generateKey();
lunaKeyStore.setKeyEntry("myPersistentAESKey", aesKey, null, null);
```

### RSA keypair persistence as `PrivateKeyEntry`

```java
KeyStore lunaKeyStore = KeyStore.getInstance("Luna");

KeyPairGenerator kpg = KeyPairGenerator.getInstance("RSA", "LunaProvider");
kpg.initialize(3072);
KeyPair rsaKeyPair = kpg.generateKeyPair();

X509Certificate selfSignedCertificate = generateSelfSignedCertificate(rsaKeyPair);
lunaKeyStore.setKeyEntry(
        "myPersistentRsaKey",
        rsaKeyPair.getPrivate(),
        null,
        new java.security.cert.Certificate[]{selfSignedCertificate}
);
```

### ML-KEM keypair persistence: conceptual provider-native pattern

```java
KeyPairGenerator kpg = KeyPairGenerator.getInstance("ML-KEM-768", "LunaProvider");
KeyPair mlKemKeyPair = kpg.generateKeyPair();

// Provider-specific note:
// In a Luna-backed design, the preferred model is that the ML-KEM private key
// remains persistent on the Luna side and is later referenced by alias or
// provider-backed key object rather than exported as raw software key bytes.
```

That last example is intentionally more conceptual because the exact persistence shape depends on what the Luna provider exposes for ML-KEM object storage and retrieval in the Java layer.

## When to use which model

Use `SecretKeyEntry` style when:

- you are persisting a symmetric key such as AES

Use `PrivateKeyEntry` style when:

- you are persisting an RSA private key in normal Java keystore form
- you have or can create a certificate carrying the public key

Use a provider-native persistent object model when:

- the key type is newer or more provider-specific
- the provider/HSM abstraction is the real source of truth
- you want the strongest `private key never leaves the HSM` story

## Best practice summary

If the goal is a future Luna-backed architecture, the most defensible mental model is:

- generate keys on Luna
- keep private keys resident on Luna
- refer to them through provider-backed Java objects, aliases, or keystore entries
- export public keys only when needed for sender-side operations

That gives you the cleanest progression from software demo to real HSM-backed key management.

## Related project files

- [src/main/java/com/example/pqc/LunaIntegrationSupport.java](E:\codex\work\pqc\src\main\java\com\example\pqc\LunaIntegrationSupport.java)
- [src/main/java/com/example/pqc/CertificateBackedRsaKeyStoreRepository.java](E:\codex\work\pqc\src\main\java\com\example\pqc\CertificateBackedRsaKeyStoreRepository.java)
- [src/main/java/com/example/pqc/RsaPrivateKeyEntryDemo.java](E:\codex\work\pqc\src\main\java\com\example\pqc\RsaPrivateKeyEntryDemo.java)

## Reference samples

The Luna Java sample names that map most closely to these patterns are:

- `PersistRSAKeyPairUsingKeyStore.java`
- `GenerateMLKEMKeyPair.java`
- `KeyEncapsulation_MLKEM.java`

If you later want, this note can be extended with a second section that maps each of these patterns to an equivalent Thales Luna sample step by step.
