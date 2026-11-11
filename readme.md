# Warnerscorner Content Guide

[Browse the hosted content](https://markbwarner.github.io/warnerscorner/)

Business briefings, technical guides, assessment resources, and supporting media for Thales data protection, key management, analytics, and post-quantum migration.

Each document includes a summary and a link to the hosted content.

## Browse by topic

- [Crypto Agility](#agility) (`agility/`)
- [AI and RAG Data Protection](#ai) (`ai/`)
- [Cloud Key Control and Data Governance](#cckm) (`cckm/`)
- [CRDP Design, Implementation, and Operations](#crdp) (`crdp/`)
- [Database, Analytics, and Secure AI](#database) (`database/`)
- [Client-Side End-to-End Data Protection](#end-to-end) (`end-to-end/`)
- [JDBC Protection for Cloud Data Access](#jdbc) (`jdbc/`)
- [CipherTrust Integration Operations](#misc) (`misc/`)
- [Luna & PQC Key Wrapping Basics and Value](#pqc) (`pqc/`)
- [Application Assessment: PII and PQC Migration](#scanner) (`scanner/`)

<a id="agility"></a>

## Crypto Agility

Planning and testing changes to cryptographic algorithms, keys, and policies.

### Crypto Agility in Practice

_Practical guide · `agility/crypto_agility.html`_

[Crypto Agility in Practice](https://markbwarner.github.io/warnerscorner/agility/crypto_agility.html) — Explains the three pillars of crypto agility: key generation, algorithm support, and key lifecycle management. It shows how to inventory dependencies, rehearse a cutover, and use CipherTrust RESTful Data Protection (CRDP) to manage supported field protection changes through policy.

[https://markbwarner.github.io/warnerscorner/agility/crypto_agility.html](https://markbwarner.github.io/warnerscorner/agility/crypto_agility.html)

<a id="ai"></a>

## AI and RAG Data Protection

Solution and implementation guidance for protecting sensitive values during document preparation and generative AI requests.

### Protecting RAG Data with Thales

_Solution overview · `ai/thales-rag-protection.html`_

[Protecting RAG Data with Thales](https://markbwarner.github.io/warnerscorner/ai/thales-rag-protection.html) — Explains protection across document preparation and application requests for retrieval-augmented generation (RAG). It maps discovery, sensitive-field inspection, CipherTrust protection, secrets management, and authorized reveal to a reference architecture. It identifies the loader and response-processing work needed to complete the examples.

[https://markbwarner.github.io/warnerscorner/ai/thales-rag-protection.html](https://markbwarner.github.io/warnerscorner/ai/thales-rag-protection.html)

### Implementing Thales RAG Protection

_Technical implementation guide · `ai/thales-rag-protection-implementation-guide.html`_

[Implementing Thales RAG Protection](https://markbwarner.github.io/warnerscorner/ai/thales-rag-protection-implementation-guide.html) — Maps the reference design to React and Spring Boot components, DDC report extraction, document conversion, DLP inspection, and CRDP or CADP protection. It covers policy tags, CSM configuration, request identity, pipeline execution, and validation. It distinguishes the active prompt-protection path and output simulator from retrieval and full-response integrations.

[https://markbwarner.github.io/warnerscorner/ai/thales-rag-protection-implementation-guide.html](https://markbwarner.github.io/warnerscorner/ai/thales-rag-protection-implementation-guide.html)

<a id="cckm"></a>

## Cloud Key Control and Data Governance

Cloud key custody, shared responsibility, and the practical differences between Bring Your Own Key (BYOK) and Hold Your Own Key (HYOK).

### When the Cloud Gets a Subpoena: Who Holds Your Keys?

_Business and architecture article · `cckm/protecting-subpoena-in-csp.html`

[When the Cloud Gets a Subpoena: Who Holds Your Keys?](https://markbwarner.github.io/warnerscorner/cckm/protecting-subpoena-in-csp.html) — Examines cloud disclosure requests through the lens of key custody. It explains BYOK, HYOK, CCKM, AWS XKS, Google Cloud EKM, and Microsoft Double Key Encryption, including the limits created by plaintext copies, cached keys, and service-specific behavior. It also outlines a coordinated legal and security response.

[https://markbwarner.github.io/warnerscorner/cckm/protecting-subpoena-in-csp.html](https://markbwarner.github.io/warnerscorner/cckm/protecting-subpoena-in-csp.html)

<a id="crdp"></a>

## CRDP Design, Implementation, and Operations

Practical guides for configuring CipherTrust RESTful Data Protection, validating application integration, and operating containerized protection services.

### CRDP Best Practices: Design, Deployment, and Operations

_Best-practices guide · `crdp/crdp-best-practices-streamlined.html`_

[CRDP Best Practices: Design, Deployment, and Operations](https://markbwarner.github.io/warnerscorner/crdp/crdp-best-practices-streamlined.html) — Organizes CRDP design and operations around domains, keys, protection policies, UserSets, JWT identity, caching, rotation, monitoring, recovery, and licensing reconciliation. It explains the responsibilities shared by security, application, and platform teams, with deployment workflows and operational examples.

[https://markbwarner.github.io/warnerscorner/crdp/crdp-best-practices-streamlined.html](https://markbwarner.github.io/warnerscorner/crdp/crdp-best-practices-streamlined.html)

### CRDP Implementation Guide

_Technical implementation guide · `crdp/crdp-implementation-guide-2026-10-23.html`_

[CRDP Implementation Guide](https://markbwarner.github.io/warnerscorner/crdp/crdp-implementation-guide-2026-10-23.html) — Provides configuration procedures, API requests, workflow diagrams, Docker validation, Kubernetes and Helm deployment templates, and an optional AKS path. It includes JWT authorization tests, bulk-response validation, Prometheus metrics, load-testing examples, autoscaling guidance, and upgrade and recovery procedures.

[https://markbwarner.github.io/warnerscorner/crdp/crdp-implementation-guide-2026-10-23.html](https://markbwarner.github.io/warnerscorner/crdp/crdp-implementation-guide-2026-10-23.html)

### Application Metrics with CRDP

_Observability overview · `crdp/application_metrics.html`_

[Application Metrics with CRDP](https://markbwarner.github.io/warnerscorner/crdp/application_metrics.html) — Explains caller-level reliability and security metrics across shared CRDP services. It connects authenticated workload identity, gateway and middleware telemetry, CRDP counters, infrastructure signals, and audit records to troubleshooting and incident investigation.

[https://markbwarner.github.io/warnerscorner/crdp/application_metrics.html](https://markbwarner.github.io/warnerscorner/crdp/application_metrics.html)

### Application Metrics with CRDP Implementation Guide

_Technical implementation guide · `crdp/application_detailed_metrics.html`_

[Application Metrics with CRDP Implementation Guide](https://markbwarner.github.io/warnerscorner/crdp/application_detailed_metrics.html) — Details runtime counter collection, latency dashboards, caller attribution, audit collection on Kubernetes and Docker, gateway analytics, capacity scaling, and validation. It includes an event contract and guidance for correlating application, middleware, CRDP, and infrastructure evidence.

[https://markbwarner.github.io/warnerscorner/crdp/application_detailed_metrics.html](https://markbwarner.github.io/warnerscorner/crdp/application_detailed_metrics.html)

<a id="database"></a>

## Database, Analytics, and Secure AI

Databricks and Snowflake materials connect governed data protection to analytics, streaming, SQL access, and retrieval augmented generation (RAG).

### Thales CRDP for Databricks

_Platform brochure · `database/databricks/thales-databricks-crdp-brochure.html`

[Thales CRDP for Databricks](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-crdp-brochure.html) — Introduces governed protect and reveal patterns across Databricks SQL Warehouse, compute clusters, Structured Streaming, and Lakeflow Declarative Pipelines. It compares Unity Catalog functions, Java UDFs, Python helpers, and Pandas approaches while keeping key and policy governance in Thales.

[https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-crdp-brochure.html](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-crdp-brochure.html)

### Snowflake and Thales: Reduce Risk and Accelerate Value

_Business-value article · `database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html`

[Snowflake and Thales: Reduce Risk and Accelerate Value](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html) — Presents the business case for combining Snowflake discovery and governance with Thales policy-based protection and customer key control. It connects sensitive-data visibility, compliance evidence, sovereignty, and analytics usability.

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html)

### Snowflake Cortex and Thales: From Discovery to Protection

_Workflow article · `database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html`

[Snowflake Cortex and Thales: From Discovery to Protection](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html) — Walks through identifying sensitive columns, applying classification and governance tags, reviewing proposed transformations, and using Thales CRDP for protection and authorized reveal. It turns discovery into a repeatable protection workflow.

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html)

### Secure RAG for Enterprise Knowledge

_Business-value article · `database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html`

[Secure RAG for Enterprise Knowledge](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html) — Explains the value of using Snowflake Cortex Search with Thales CRDP to make internal knowledge useful while limiting exposure of sensitive values. It discusses protected retrieval context, user-specific access, and authorized reveal.

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html)

### Building Secure RAG with Snowflake Cortex Search and Thales CRDP

_Technical architecture · `database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html`

[Building Secure RAG with Snowflake Cortex Search and Thales CRDP](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html) — Details a pipeline that parses staged documents, detects and validates sensitive entities, protects them through CRDP, and indexes sanitized text in Cortex Search. Answers remain protected by default, with reveal handled through a separate authorized path.

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html)

### Thales CRDP on Snowpark Container Services: Business Value

_Business briefing · `database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html`

[Thales CRDP on Snowpark Container Services: Business Value](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html) — Explains why a Snowflake-hosted container integration can bring SQL-accessible encryption and tokenization closer to the data while preserving centralized Thales policy and key management. It covers operational ownership and the distinction from external-function deployments.

[https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html)

### Thales CRDP on Snowpark Container Services: Technical Overview

_Technical overview · `database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html`

[Thales CRDP on Snowpark Container Services: Technical Overview](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html) — Describes SQL service functions, a Java/Spring Boot adapter, private CRDP service endpoints, and CipherTrust Manager. It covers image repositories, compute pools, role grants, secrets, TLS, network controls, telemetry, and rollout considerations.

[https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html)

### Thales Databricks Integration Story Video

_Video (WMV) · `database/databricks/thales-databricks-integration-story.wmv`

[Thales Databricks Integration Story Video](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv) — A downloadable WMV video resource for the Databricks integration story. Playback may require a compatible local media player.

[https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv)

### Cloud Database Column Protection Options

_Architecture decision guide · `database/snowflake/thales-cloud-database-column-protection-options.html`_

[Cloud Database Column Protection Options](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-cloud-database-column-protection-options.html) — Compares server-side Snowpark Container Services integration with client-side Snowflake JDBC protection and hybrid approaches. It covers consumer coverage, bypass paths, identity, workload performance, schema and metadata impacts, operational ownership, and managed-database extensibility limits.

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-cloud-database-column-protection-options.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-cloud-database-column-protection-options.html)

### JDBC Protection for Snowflake: Database Resource

_Business brochure · `database/snowflake/thales-jdbc-snowflake-brochure.html`_

[JDBC Protection for Snowflake: Database Resource](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-brochure.html) — Presents the Snowflake JDBC wrapper as a policy-aware access layer for familiar SQL tools, BI clients, and applications. It explains configured protected fields, connected-user identity, CRDP or CADP Centralized reveal, policy and metadata choices, datasource overrides, and userset-based allowlist controls.

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-brochure.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-brochure.html)

### Snowflake JDBC Technical Overview: Database Resource

_Technical overview · `database/snowflake/thales-jdbc-snowflake-technical-overview.html`_

[Snowflake JDBC Technical Overview: Database Resource](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-technical-overview.html) — Details the wrapper and vendor-driver flow, object-scoped field mappings, identity normalization, bulk reveal, per-row metadata headers, allowlist checks, and credential sources. It also covers DbVisualizer dependency deployment, validation and in-place transformation utilities, and CSV loader modes.

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-technical-overview.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-technical-overview.html)

### Thales Snowflake Customer Security Overview

_Customer overview · `database/snowflake/thales-snowflake-customer-security-overview.html`_

[Thales Snowflake Customer Security Overview](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-snowflake-customer-security-overview.html) — A customer-facing overview for discussing Thales security and data protection in Snowflake environments.

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-snowflake-customer-security-overview.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-snowflake-customer-security-overview.html)

<a id="end-to-end"></a>

## Client-Side End-to-End Data Protection

A client-side protection pattern that encrypts fields at capture, unwraps keys in a trusted backend, and applies durable Thales protection before storage.

### Client-Side End-to-End Protection: Business Value

_Business briefing · `end-to-end/thales-client-side-end-to-end-business-value.html`

[Client-Side End-to-End Protection: Business Value](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-business-value.html) — Introduces protection at the browser, mobile, kiosk, or IoT capture point. It explains single-use AES keys, public-key wrapping, cached public-key distribution, a brief trusted-backend plaintext transition, and durable CRDP protection for downstream use.

[https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-business-value.html](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-business-value.html)

### Client-Side End-to-End Protection: Technical Overview

_Technical overview · `end-to-end/thales-client-side-end-to-end-technical-overview.html`

[Client-Side End-to-End Protection: Technical Overview](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-technical-overview.html) — Describes browser Web Crypto AES-GCM encryption and RSA-OAEP wrapping, backend REST or CADP unwrap paths, CRDP bulk protect and reveal, key versioning, and Redis caching. It distinguishes prototype components from production requirements and identifies the trusted-backend plaintext window.

[https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-technical-overview.html](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-technical-overview.html)

### Client-Side End-to-End Protection PDF

_PDF companion · `end-to-end/thales-client-side-end-to-end.pdf`

[Client-Side End-to-End Protection PDF](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end.pdf) — The folder's downloadable PDF companion for the client-side end-to-end protection topic.

[https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end.pdf](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end.pdf)

<a id="jdbc"></a>

## JDBC Protection for Cloud Data Access

Business and technical resources for applying Thales policy through JDBC wrappers and drivers used by SQL tools, BI clients, and applications.

### JDBC Protection for Cloud Databases

_Solution brochure · `jdbc/thales-jdbc-cloud-databases-brochure.html`

[JDBC Protection for Cloud Databases](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-cloud-databases-brochure.html) — Introduces JDBC-based field protection and reveal for PostgreSQL, MySQL, and MariaDB across AWS, Google Cloud, and Microsoft Azure database services. It explains CRDP and CADP Centralized policy paths, configured protected columns, and familiar SQL and BI workflows.

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-cloud-databases-brochure.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-cloud-databases-brochure.html)

### JDBC Protection for Databricks

_Business brochure · `jdbc/thales-jdbc-databricks-brochure.html`

[JDBC Protection for Databricks](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-brochure.html) — Presents client-side policy-aware protect and reveal for Databricks JDBC consumers. It connects pre-protected data, centrally defined policy, and read-time ciphertext, masked, or cleartext outcomes in familiar SQL workflows.

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-brochure.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-brochure.html)

### Databricks JDBC Technical Overview: Developer Preview/Beta

_Technical overview / preview · `jdbc/thales-jdbc-databricks-technical-overview.html`

[Databricks JDBC Technical Overview: Developer Preview/Beta](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-technical-overview.html) — Explains the wrapper-plus-delegate-driver design, object-scoped mappings, tag aliases, result-set interception, SQL session identity, batching, and CRDP or CADP Centralized enforcement. The source labels this implementation a developer preview/beta.

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-technical-overview.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-technical-overview.html)

### JDBC Protection for Snowflake

_Business brochure · `jdbc/thales-jdbc-snowflake-brochure.html`

[JDBC Protection for Snowflake](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-brochure.html) — Explains how a Snowflake JDBC wrapper adds configured field detection, identity-aware reveal, policy options, batching, and optional userset checks while delegating SQL execution and connectivity to Snowflake.

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-brochure.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-brochure.html)

### Snowflake JDBC Technical Overview

_Technical overview · `jdbc/thales-jdbc-snowflake-technical-overview.html`

[Snowflake JDBC Technical Overview](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-technical-overview.html) — Details JDBC connection, statement, and result-set proxies; object and default field mappings; identity normalization; bulk reveal; policy types; credential sources; and fail-closed allowlist behavior. It also distinguishes result handling from limitations on automatic protected-predicate rewriting.

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-technical-overview.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-technical-overview.html)

<a id="misc"></a>

## CipherTrust Integration Operations

An operational pattern for keeping long-running CipherTrust REST integrations working across token expiry.

### CipherTrust REST Token Refresh Pattern

_Operational guide · `misc/ciphertrust-rest-token-refresh-pattern.html`

[CipherTrust REST Token Refresh Pattern](https://markbwarner.github.io/warnerscorner/misc/ciphertrust-rest-token-refresh-pattern.html) — Explains a reusable Java helper that refreshes JWTs before expiry and refreshes and retries once when an unauthorized or token-expired response still occurs. It covers batch jobs, stream consumers, backend services, thick clients, and packaging as a utility or library.

[https://markbwarner.github.io/warnerscorner/misc/ciphertrust-rest-token-refresh-pattern.html](https://markbwarner.github.io/warnerscorner/misc/ciphertrust-rest-token-refresh-pattern.html)

<a id="pqc"></a>

## Luna & PQC Key Wrapping Basics and Value

A progression from the business risk of legacy key transport to project planning, Luna-native implementation, and stronger private-key custody.

### ML-KEM Wrap Blog

_Business article · `pqc/ml-kem-wrap-blog.html`

[ML-KEM Wrap Blog](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-wrap-blog.html) — Explains envelope encryption in business-friendly language: AES protects the content, while RSA wrapping or ML-KEM key establishment protects the key exchange between systems. It frames ML-KEM as a practical response to harvest-now-decrypt-later risk and connects algorithm choices to private-key custody.

[https://markbwarner.github.io/warnerscorner/pqc/ml-kem-wrap-blog.html](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-wrap-blog.html)

### PQC Key-Wrapping Project Briefing

_Project-manager briefing · `pqc/pqc-key-wrapping-project-briefing.html`

[PQC Key-Wrapping Project Briefing](https://markbwarner.github.io/warnerscorner/pqc/pqc-key-wrapping-project-briefing.html) — Turns cryptography into a delivery discussion: what changes from RSA wrapping to ML-KEM key establishment, what remains stable with AES-GCM, where Luna fits, and how discovery, dependencies, compatibility, and phased rollout shape the project.

[https://markbwarner.github.io/warnerscorner/pqc/pqc-key-wrapping-project-briefing.html](https://markbwarner.github.io/warnerscorner/pqc/pqc-key-wrapping-project-briefing.html)

### ML-KEM Luna Implementation Guide

_Implementation guide · `pqc/ml-kem-luna-implementation-guide.html`

[ML-KEM Luna Implementation Guide](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-luna-implementation-guide.html) — Provides the technical story for Luna-native RSA-OAEP wrapping and ML-KEM encapsulation and decapsulation with AES-GCM field protection. It explains the transport envelope, Luna-backed private-key operations, and provider compatibility considerations; the RSA example creates its AES key separately from Luna.

[https://markbwarner.github.io/warnerscorner/pqc/ml-kem-luna-implementation-guide.html](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-luna-implementation-guide.html)

### Luna Key Persistence Patterns

_Technical note (Markdown) · `pqc/luna-key-persistence-patterns.md`

[Luna Key Persistence Patterns](https://markbwarner.github.io/warnerscorner/pqc/luna-key-persistence-patterns.md) — Collects Java persistence patterns for AES secret keys, RSA private-key entries with certificate chains, and ML-KEM recipient keypairs. It emphasizes provider-native persistence and keeping private keys on Luna; the ML-KEM example is conceptual and provider-dependent.

[https://markbwarner.github.io/warnerscorner/pqc/luna-key-persistence-patterns.md](https://markbwarner.github.io/warnerscorner/pqc/luna-key-persistence-patterns.md)

### Defense in Depth: Protecting Keys Beyond the File System

_Security architecture guide · `pqc/defense-in-depth-key-custody.html`

[Defense in Depth: Protecting Keys Beyond the File System](https://markbwarner.github.io/warnerscorner/pqc/defense-in-depth-key-custody.html) — Places HSM custody within a layered design covering people, identity, networks, applications, and data. It compares storage models and uses incident lessons to distinguish reduced key-copy risk from the continuing need to govern authorized cryptographic operations.

[https://markbwarner.github.io/warnerscorner/pqc/defense-in-depth-key-custody.html](https://markbwarner.github.io/warnerscorner/pqc/defense-in-depth-key-custody.html)

### PQC Guide for Thales CipherTrust Manager

_Migration planning guide · `pqc/ciphertrust-pqc-cm-guide.html`_

[PQC Guide for Thales CipherTrust Manager](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-guide.html) — Explains how quantum risk affects confidentiality and long-term trust. It covers CipherTrust Manager capabilities and limits, signing in a Zero Trust design, and using a cryptographic bill of materials (CBOM) to prioritize migration work.

[https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-guide.html](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-guide.html)

### PQC Implementation Guide for Thales CipherTrust Manager

_Technical implementation guide · `pqc/ciphertrust-pqc-cm-implementation-guide.html`_

[PQC Implementation Guide for Thales CipherTrust Manager](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-implementation-guide.html) — Walks through ML-DSA artifact signing, signing mode selection, external mu, and a GitHub Actions pipeline. It compares CipherTrust Manager and Luna HSM roles and includes inventory examples and acceptance tests.

[https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-implementation-guide.html](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-implementation-guide.html)

<a id="scanner"></a>

## Application Assessment: PII and PQC Migration

Source-code assessment materials for finding sensitive-data and cryptography touchpoints, identifying likely change owners, and planning migration work. These are guides and positioning resources for the scanners.

### Application Code Sensitive Data Scanner

_PII assessment brochure · `scanner/pii/code-impact-scanner-brochure.html`

[Application Code Sensitive Data Scanner](https://markbwarner.github.io/warnerscorner/scanner/pii/code-impact-scanner-brochure.html) — Introduces source-code scanning for sensitive field references, likely backend and data-access owners, JDBC candidates, complexity, and planning exports. It looks for code evidence such as field names and integration patterns rather than scanning production data values.

[https://markbwarner.github.io/warnerscorner/scanner/pii/code-impact-scanner-brochure.html](https://markbwarner.github.io/warnerscorner/scanner/pii/code-impact-scanner-brochure.html)

### How the PII Scanner Works

_PII technical explainer · `scanner/pii/how-the-pii-scanner-works.html`

[How the PII Scanner Works](https://markbwarner.github.io/warnerscorner/scanner/pii/how-the-pii-scanner-works.html) — Explains file classification, identifier normalization, built-in and custom rules, optional literal matching, API and SQL clues, ownership correlation, complexity scoring, and JSON, CSV, and DBA-planning outputs. It shows how findings become candidate CRDP, JDBC, or data-access work.

[https://markbwarner.github.io/warnerscorner/scanner/pii/how-the-pii-scanner-works.html](https://markbwarner.github.io/warnerscorner/scanner/pii/how-the-pii-scanner-works.html)

### Application Protection Decision Guide

_PII customer handout · `scanner/pii/application-protection-customer-handout.html`

[Application Protection Decision Guide](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-customer-handout.html) — Explains why shared backend services are often the best protect-and-reveal integration point, when direct clients are valid exceptions, and how scanner correlations help identify likely owners. It includes useful report filters and DBA handoff fields.

[https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-customer-handout.html](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-customer-handout.html)

### Application Protection Decision Matrix

_PII architecture matrix · `scanner/pii/application-protection-decision-matrix.html`

[Application Protection Decision Matrix](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-decision-matrix.html) — Compares integration points for multi-tier applications, direct clients, batch services, Kafka flows, JDBC-heavy services, and shared APIs. A criteria matrix connects reuse, business logic, audit needs, and existing boundaries to the architecture choice.

[https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-decision-matrix.html](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-decision-matrix.html)

### Application PQC Readiness Scanner

_PQC assessment brochure · `scanner/pqc/pqc-readiness-scanner-brochure.html`

[Application PQC Readiness Scanner](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-readiness-scanner-brochure.html) — Introduces source and dependency assessment for RSA, ECC, TLS, JWT, certificates, SSH, KMS, and signing touchpoints. It distinguishes implementation owners from references and describes migration worklists and CBOM-style outputs.

[https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-readiness-scanner-brochure.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-readiness-scanner-brochure.html)

### How the PQC Scanner Works

_PQC technical explainer · `scanner/pqc/how-the-pqc-scanner-works.html`

[How the PQC Scanner Works](https://markbwarner.github.io/warnerscorner/scanner/pqc/how-the-pqc-scanner-works.html) — Explains file classification, configurable cryptography rules, dependency hints, custom wrapper markers, merged findings, complexity estimates, remediation lanes, and JSON, CSV, HTML, and CBOM-style reporting.

[https://markbwarner.github.io/warnerscorner/scanner/pqc/how-the-pqc-scanner-works.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/how-the-pqc-scanner-works.html)

### Why Use the Application PQC Readiness Scanner?

_PQC customer handout · `scanner/pqc/pqc-scanner-customer-positioning-handout.html`

[Why Use the Application PQC Readiness Scanner?](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-customer-positioning-handout.html) — Positions the scanner around likely change targets, ownership, reference filtering, custom wrappers, OpenAPI onboarding, and planning-friendly exports. It focuses on turning discovery into application migration work.

[https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-customer-positioning-handout.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-customer-positioning-handout.html)

### PQC Scanner Competitive Battlecard

_PQC sales battlecard · `scanner/pqc/pqc-scanner-competitive-battlecard.html`

[PQC Scanner Competitive Battlecard](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-competitive-battlecard.html) — Provides sales positioning, differentiators, buyer questions, and guidance on where inventory and discovery tools fit. Its focus is file-level evidence and migration planning; use its comparisons as discussion prompts for a customer-specific evaluation.

[https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-competitive-battlecard.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-competitive-battlecard.html)

### ML-KEM Wrap Blog: Scanner Companion

_PQC business article · `scanner/pqc/ml-kem-wrap-blog.html`

[ML-KEM Wrap Blog: Scanner Companion](https://markbwarner.github.io/warnerscorner/scanner/pqc/ml-kem-wrap-blog.html) — A scanner-folder edition of the envelope-encryption article explaining AES content protection, RSA wrapping versus ML-KEM key establishment, harvest-now-decrypt-later risk, and private-key storage choices.

[https://markbwarner.github.io/warnerscorner/scanner/pqc/ml-kem-wrap-blog.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/ml-kem-wrap-blog.html)

