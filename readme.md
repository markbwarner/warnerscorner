# Warnerscorner Content Guide

[Browse the hosted content](https://markbwarner.github.io/warnerscorner/)

Business briefings, technical guides, assessment resources, and supporting media for Thales data protection, key management, analytics, and post-quantum migration.

Each document includes a summary, a sales use, and a suggested conversation opener. Supporting diagrams and media include context for using them in the same discussion.

## Browse by topic

- [Cloud Key Control and Data Governance](#cckm) (`cckm/`)
- [Database, Analytics, and Secure AI](#database) (`database/`)
- [Client-Side End-to-End Data Protection](#end-to-end) (`end-to-end/`)
- [Shared Key Protection Diagrams](#images) (`images/`)
- [JDBC Protection for Cloud Data Access](#jdbc) (`jdbc/`)
- [CipherTrust Integration Operations](#misc) (`misc/`)
- [Luna & PQC Key Wrapping Basics and Value](#pqc) (`pqc/`)
- [Application Assessment: PII and PQC Migration](#scanner) (`scanner/`)

<a id="cckm"></a>

## Cloud Key Control and Data Governance

Cloud key custody, shared responsibility, and the practical differences between Bring Your Own Key (BYOK) and Hold Your Own Key (HYOK).

**Suggested conversation path:** Start with sensitive-data ownership, compare BYOK and HYOK, then scope a pilot that tests access, caching, availability, and audit evidence.

### When the Cloud Gets a Subpoena: Who Holds Your Keys?

_Business and architecture article · `cckm/protecting-subpoena-in-csp.html`

[When the Cloud Gets a Subpoena: Who Holds Your Keys?](https://markbwarner.github.io/warnerscorner/cckm/protecting-subpoena-in-csp.html) — Examines cloud disclosure requests through the lens of key custody. It explains BYOK, HYOK, CCKM, AWS XKS, Google Cloud EKM, and Microsoft Double Key Encryption, including the limits created by plaintext copies, cached keys, and service-specific behavior. It also outlines a coordinated legal and security response.

**Sales use:** Open a cloud sovereignty and governance discussion with security, privacy, cloud operations, and legal stakeholders. Use the article to clarify technical control boundaries and response ownership.

**Suggested opener:** “Which sensitive cloud workloads require independent key custody, and have you tested what your provider can still access when an external key operation is denied?”

[https://markbwarner.github.io/warnerscorner/cckm/protecting-subpoena-in-csp.html](https://markbwarner.github.io/warnerscorner/cckm/protecting-subpoena-in-csp.html)

<a id="database"></a>

## Database, Analytics, and Secure AI

Databricks and Snowflake materials connect governed data protection to analytics, streaming, SQL access, and retrieval augmented generation (RAG).

**Suggested conversation path:** Lead with the platform-specific business outcome, use the architecture materials to identify the integration path, then discuss policies, identity, and a representative workload pilot.

### Thales CRDP for Databricks

_Platform brochure · `database/databricks/thales-databricks-crdp-brochure.html`

[Thales CRDP for Databricks](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-crdp-brochure.html) — Introduces governed protect and reveal patterns across Databricks SQL Warehouse, compute clusters, Structured Streaming, and Lakeflow Declarative Pipelines. It compares Unity Catalog functions, Java UDFs, Python helpers, and Pandas approaches while keeping key and policy governance in Thales.

**Sales use:** Bring security and data-platform teams together around reusable controls across SQL, engineering, and streaming workloads.

**Suggested opener:** “How are you applying the same sensitive-data policies across Databricks SQL, Spark jobs, and streaming pipelines?”

[https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-crdp-brochure.html](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-crdp-brochure.html)

### Snowflake and Thales: Reduce Risk and Accelerate Value

_Business-value article · `database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html`

[Snowflake and Thales: Reduce Risk and Accelerate Value](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html) — Presents the business case for combining Snowflake discovery and governance with Thales policy-based protection and customer key control. It connects sensitive-data visibility, compliance evidence, sovereignty, and analytics usability.

**Sales use:** Start with business sponsors who want analytics and AI value while reducing sensitive-data exposure and operational friction.

**Suggested opener:** “Where does sensitive-data risk slow your Snowflake analytics or AI programs today?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_BUSINESS_VALUE_SNOWFLAKE_THALES.html)

### Snowflake Cortex and Thales: From Discovery to Protection

_Workflow article · `database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html`

[Snowflake Cortex and Thales: From Discovery to Protection](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html) — Walks through identifying sensitive columns, applying classification and governance tags, reviewing proposed transformations, and using Thales CRDP for protection and authorized reveal. It turns discovery into a repeatable protection workflow.

**Sales use:** Move a classification conversation toward actionable protection, governance review, and controlled access.

**Suggested opener:** “Once your team classifies a sensitive Snowflake column, how does that finding become an approved protection policy?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_CORTEX_THALES_SNOWFLAKE.html)

### Secure RAG for Enterprise Knowledge

_Business-value article · `database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html`

[Secure RAG for Enterprise Knowledge](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html) — Explains the value of using Snowflake Cortex Search with Thales CRDP to make internal knowledge useful while limiting exposure of sensitive values. It discusses protected retrieval context, user-specific access, and authorized reveal.

**Sales use:** Engage AI sponsors, privacy teams, and knowledge-platform owners who need useful enterprise answers with controlled access to sensitive details.

**Suggested opener:** “Which internal documents would you like AI to use, and which values should remain protected in retrieved context and answers?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_BUSINESS_VALUE_SNOWFLAKE_THALES.html)

### Building Secure RAG with Snowflake Cortex Search and Thales CRDP

_Technical architecture · `database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html`

[Building Secure RAG with Snowflake Cortex Search and Thales CRDP](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html) — Details a pipeline that parses staged documents, detects and validates sensitive entities, protects them through CRDP, and indexes sanitized text in Cortex Search. Answers remain protected by default, with reveal handled through a separate authorized path.

**Sales use:** Use with AI architects and application security teams to map ingestion, retrieval, model context, and reveal trust boundaries.

**Suggested opener:** “Can we trace a sensitive value from document ingestion through retrieval and answer generation, including who can authorize its reveal?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html](https://markbwarner.github.io/warnerscorner/database/snowflake/BLOG_RAG_TECHNICAL_SNOWFLAKE_THALES.html)

### Thales CRDP on Snowpark Container Services: Business Value

_Business briefing · `database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html`

[Thales CRDP on Snowpark Container Services: Business Value](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html) — Explains why a Snowflake-hosted container integration can bring SQL-accessible encryption and tokenization closer to the data while preserving centralized Thales policy and key management. It covers operational ownership and the distinction from external-function deployments.

**Sales use:** Discuss deployment strategy with Snowflake platform owners who want governed protection within their existing service operations.

**Suggested opener:** “Would running the protection integration within Snowflake simplify your operating model and data-governance requirements?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SNOWFLAKE_SPCS_BUSINESS_VALUE.html)

### Thales CRDP on Snowpark Container Services: Technical Overview

_Technical overview · `database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html`

[Thales CRDP on Snowpark Container Services: Technical Overview](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html) — Describes SQL service functions, a Java/Spring Boot adapter, private CRDP service endpoints, and CipherTrust Manager. It covers image repositories, compute pools, role grants, secrets, TLS, network controls, telemetry, and rollout considerations.

**Sales use:** Support a technical workshop on container deployment, private connectivity, service authorization, and production readiness.

**Suggested opener:** “Who will own the Snowflake services, network paths, secrets, and capacity for a production protect-and-reveal integration?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html](https://markbwarner.github.io/warnerscorner/database/snowflake/THALES_SPCS_TECHNICAL_OVERVIEW.html)

### Databricks Execution Model Matrix

_Diagram · `database/databricks/execution-model-matrix.png`

[Databricks Execution Model Matrix](https://markbwarner.github.io/warnerscorner/database/databricks/execution-model-matrix.png) — Compares Java Spark UDFs, the Python Helper API, the Pandas API, and Unity Catalog Python UDFs by runtime and best-fit workload.

**Sales use:** Help a data engineering team choose the appropriate SQL or Spark integration path.

**Suggested opener:** “Is this workload primarily governed SQL access or high-throughput Spark processing?”

[https://markbwarner.github.io/warnerscorner/database/databricks/execution-model-matrix.png](https://markbwarner.github.io/warnerscorner/database/databricks/execution-model-matrix.png)

### Databricks and Thales CRDP Architecture

_Diagram · `database/databricks/CUSTOMER_ARCHITECTURE.png`

[Databricks and Thales CRDP Architecture](https://markbwarner.github.io/warnerscorner/database/databricks/CUSTOMER_ARCHITECTURE.png) — Shows Databricks users and tools reaching SQL Warehouse or compute-cluster functions, which call CRDP backed by CipherTrust Manager.

**Sales use:** Establish the service boundaries and policy flow before detailed design.

**Suggested opener:** “Where should the CRDP service sit relative to your Databricks access layers?”

[https://markbwarner.github.io/warnerscorner/database/databricks/CUSTOMER_ARCHITECTURE.png](https://markbwarner.github.io/warnerscorner/database/databricks/CUSTOMER_ARCHITECTURE.png)

### Databricks Solution Integration Map

_Diagram · `database/databricks/Databrickssolutions.png`

[Databricks Solution Integration Map](https://markbwarner.github.io/warnerscorner/database/databricks/Databrickssolutions.png) — Maps compute clusters, SQL Warehouses, Lakeflow and streaming, JDBC clients, and Thales integration components across cloud and customer domains.

**Sales use:** Explain the available integration choices to a mixed platform and security audience.

**Suggested opener:** “Which Databricks execution paths and client tools need protection in your environment?”

[https://markbwarner.github.io/warnerscorner/database/databricks/Databrickssolutions.png](https://markbwarner.github.io/warnerscorner/database/databricks/Databrickssolutions.png)

### Thales Databricks Integration Story Video

_Video (WMV) · `database/databricks/thales-databricks-integration-story.wmv`

[Thales Databricks Integration Story Video](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv) — A downloadable WMV video resource for the Databricks integration story. Playback may require a compatible local media player.

**Sales use:** Offer the video as a follow-up resource alongside the Databricks brochure and architecture diagrams.

**Suggested opener:** “Would a video follow-up help your team prepare for the Databricks integration discussion?”

[https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv)

### Cortex and Thales Protection Workflow

_Diagram · `database/snowflake/assets/cortex-thales-protection-workflow.png`

[Cortex and Thales Protection Workflow](https://markbwarner.github.io/warnerscorner/database/snowflake/assets/cortex-thales-protection-workflow.png) — Illustrates discovery, column-level PII tags, a review step, Snowpark Container Services, CRDP protection, and governed reveal backed by CipherTrust Manager.

**Sales use:** Walk stakeholders from discovery to enforcement using a single visual.

**Suggested opener:** “Where is the approval step between identifying sensitive columns and transforming their values?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/assets/cortex-thales-protection-workflow.png](https://markbwarner.github.io/warnerscorner/database/snowflake/assets/cortex-thales-protection-workflow.png)

### Protected Data, Governed Access

_Diagram · `database/snowflake/assets/governed-data-access.png`

[Protected Data, Governed Access](https://markbwarner.github.io/warnerscorner/database/snowflake/assets/governed-data-access.png) — Contrasts protected or masked query results with authorized cleartext access through a governed view or JDBC driver and Thales policy.

**Sales use:** Explain why the same protected dataset can support different access outcomes.

**Suggested opener:** “Which users should see protected values, and which should be allowed to reveal them?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/assets/governed-data-access.png](https://markbwarner.github.io/warnerscorner/database/snowflake/assets/governed-data-access.png)

### Secure RAG for Sensitive Knowledge Diagram

_Diagram · `database/snowflake/assets/secure-rag-cortex-search-thales.png`

[Secure RAG for Sensitive Knowledge Diagram](https://markbwarner.github.io/warnerscorner/database/snowflake/assets/secure-rag-cortex-search-thales.png) — Shows sensitive source documents becoming sanitized Cortex Search content, with Thales policy and key controls supporting protected and authorized answer outcomes.

**Sales use:** Explain the secure RAG story to AI and business stakeholders.

**Suggested opener:** “What sensitive content should remain protected even when a document is searchable?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/assets/secure-rag-cortex-search-thales.png](https://markbwarner.github.io/warnerscorner/database/snowflake/assets/secure-rag-cortex-search-thales.png)

<a id="end-to-end"></a>

## Client-Side End-to-End Data Protection

A client-side protection pattern that encrypts fields at capture, unwraps keys in a trusted backend, and applies durable Thales protection before storage.

**Suggested conversation path:** Begin with exposure at capture, follow the request through the architecture, then validate backend plaintext boundaries and downstream protection policies.

### Client-Side End-to-End Protection: Business Value

_Business briefing · `end-to-end/thales-client-side-end-to-end-business-value.html`

[Client-Side End-to-End Protection: Business Value](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-business-value.html) — Introduces protection at the browser, mobile, kiosk, or IoT capture point. It explains single-use AES keys, public-key wrapping, cached public-key distribution, a brief trusted-backend plaintext transition, and durable CRDP protection for downstream use.

**Sales use:** Start a discussion about sensitive information passing through front ends, middleware, logs, and databases.

**Suggested opener:** “Where does sensitive data first enter your applications, and how many systems handle it before durable protection is applied?”

[https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-business-value.html](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-business-value.html)

### Client-Side End-to-End Protection: Technical Overview

_Technical overview · `end-to-end/thales-client-side-end-to-end-technical-overview.html`

[Client-Side End-to-End Protection: Technical Overview](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-technical-overview.html) — Describes browser Web Crypto AES-GCM encryption and RSA-OAEP wrapping, backend REST or CADP unwrap paths, CRDP bulk protect and reveal, key versioning, and Redis caching. It distinguishes prototype components from production requirements and identifies the trusted-backend plaintext window.

**Sales use:** Engage application security, backend, and key-management teams in a concrete integration and hardening discussion.

**Suggested opener:** “Can we map client encryption, backend unwrap, transient decryption, and durable protection to your existing service boundaries?”

[https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-technical-overview.html](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end-technical-overview.html)

### Client-Side End-to-End Protection PDF

_PDF companion · `end-to-end/thales-client-side-end-to-end.pdf`

[Client-Side End-to-End Protection PDF](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end.pdf) — The folder's downloadable PDF companion for the client-side end-to-end protection topic.

**Sales use:** Provide a portable companion to the business and technical web pages for meeting follow-up.

**Suggested opener:** “Would a downloadable PDF help your stakeholders review the end-to-end protection discussion?”

[https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end.pdf](https://markbwarner.github.io/warnerscorner/end-to-end/thales-client-side-end-to-end.pdf)

### Transit-to-Storage Re-Wrapping Architecture

_Diagram · `end-to-end/thales-end-to-end.png`

[Transit-to-Storage Re-Wrapping Architecture](https://markbwarner.github.io/warnerscorner/end-to-end/thales-end-to-end.png) — Maps browser encryption, cached public keys, wrapped AES transport, Spring Boot processing, Thales private-key operations, CRDP re-protection, and protected storage.

**Sales use:** Use a single diagram to discuss capture, transport, backend processing, and storage boundaries.

**Suggested opener:** “Where should the trusted transition from transit encryption to storage protection occur?”

[https://markbwarner.github.io/warnerscorner/end-to-end/thales-end-to-end.png](https://markbwarner.github.io/warnerscorner/end-to-end/thales-end-to-end.png)

<a id="images"></a>

## Shared Key Protection Diagrams

Reusable visuals for envelope encryption, key custody, and Java keystore discussions.

**Suggested conversation path:** Use the AES diagram to explain the encryption model, the storage diagram to discuss custody, and the RSA diagram to explore Java implementation choices.

### Protecting an AES-256 Key: RSA vs ML-KEM

_Diagram · `images/aes-key-protection-rsa-vs-mlkem.png`

[Protecting an AES-256 Key: RSA vs ML-KEM](https://markbwarner.github.io/warnerscorner/images/aes-key-protection-rsa-vs-mlkem.png) — Compares generating and wrapping an AES key with RSA against ML-KEM encapsulation and shared-secret-based key establishment. Both paths use AES-GCM for content encryption.

**Sales use:** Make the PQC transition understandable while keeping content encryption and key establishment distinct.

**Suggested opener:** “How are AES content keys protected when they cross your service or partner boundaries?”

[https://markbwarner.github.io/warnerscorner/images/aes-key-protection-rsa-vs-mlkem.png](https://markbwarner.github.io/warnerscorner/images/aes-key-protection-rsa-vs-mlkem.png)

### Key Storage Architecture: Flat Files to HSM

_Diagram · `images/key-storage-architecture-flat-files-to-hsm.png`

[Key Storage Architecture: Flat Files to HSM](https://markbwarner.github.io/warnerscorner/images/key-storage-architecture-flat-files-to-hsm.png) — Compares flat files and PEM, Java software keystores, managed KMS or secrets services, and customer-controlled HSMs by custody and control boundary.

**Sales use:** Structure a discovery discussion around where private keys live and who can use or copy them.

**Suggested opener:** “Which high-value private keys are still stored in files, software keystores, or application configuration?”

[https://markbwarner.github.io/warnerscorner/images/key-storage-architecture-flat-files-to-hsm.png](https://markbwarner.github.io/warnerscorner/images/key-storage-architecture-flat-files-to-hsm.png)

### RSA Keystore Models: Raw Bytes vs PrivateKeyEntry

_Diagram · `images/rsa-keystore-models-comparison.png`

[RSA Keystore Models: Raw Bytes vs PrivateKeyEntry](https://markbwarner.github.io/warnerscorner/images/rsa-keystore-models-comparison.png) — Contrasts a software demo that exports and reconstructs RSA key bytes with a certificate-backed Java PrivateKeyEntry and provider-backed key references.

**Sales use:** Help Java and HSM teams distinguish a teaching demo from an HSM-aligned persistence design.

**Suggested opener:** “Does your application retrieve a provider-backed private key, or reconstruct one from exported bytes?”

[https://markbwarner.github.io/warnerscorner/images/rsa-keystore-models-comparison.png](https://markbwarner.github.io/warnerscorner/images/rsa-keystore-models-comparison.png)

<a id="jdbc"></a>

## JDBC Protection for Cloud Data Access

Business and technical resources for applying Thales policy through JDBC wrappers and drivers used by SQL tools, BI clients, and applications.

**Suggested conversation path:** Start with the database-specific brochure, move to the technical overview, then use the process and architecture diagrams to scope configuration, identity, and validation.

### JDBC Protection for Cloud Databases

_Solution brochure · `jdbc/thales-jdbc-cloud-databases-brochure.html`

[JDBC Protection for Cloud Databases](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-cloud-databases-brochure.html) — Introduces JDBC-based field protection and reveal for PostgreSQL, MySQL, and MariaDB across AWS, Google Cloud, and Microsoft Azure database services. It explains CRDP and CADP Centralized policy paths, configured protected columns, and familiar SQL and BI workflows.

**Sales use:** Explore a reusable protection approach across managed relational databases and existing JDBC tools.

**Suggested opener:** “Which JDBC-connected cloud databases need consistent protection without separate integrations in every consuming tool?”

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-cloud-databases-brochure.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-cloud-databases-brochure.html)

### JDBC Protection for Databricks

_Business brochure · `jdbc/thales-jdbc-databricks-brochure.html`

[JDBC Protection for Databricks](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-brochure.html) — Presents client-side policy-aware protect and reveal for Databricks JDBC consumers. It connects pre-protected data, centrally defined policy, and read-time ciphertext, masked, or cleartext outcomes in familiar SQL workflows.

**Sales use:** Discuss governed access with Databricks analytics teams and owners of shared BI and JDBC applications.

**Suggested opener:** “How do your Databricks JDBC users receive policy-appropriate results from protected data today?”

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-brochure.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-brochure.html)

### Databricks JDBC Technical Overview: Developer Preview/Beta

_Technical overview / preview · `jdbc/thales-jdbc-databricks-technical-overview.html`

[Databricks JDBC Technical Overview: Developer Preview/Beta](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-technical-overview.html) — Explains the wrapper-plus-delegate-driver design, object-scoped mappings, tag aliases, result-set interception, SQL session identity, batching, and CRDP or CADP Centralized enforcement. The source labels this implementation a developer preview/beta.

**Sales use:** Use with engineers to evaluate compatibility, configuration, identity resolution, and a controlled proof of concept.

**Suggested opener:** “Can we test one Databricks SQL Warehouse workload with your real field mappings and token-based session identity?”

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-technical-overview.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-databricks-technical-overview.html)

### JDBC Protection for Snowflake

_Business brochure · `jdbc/thales-jdbc-snowflake-brochure.html`

[JDBC Protection for Snowflake](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-brochure.html) — Explains how a Snowflake JDBC wrapper adds configured field detection, identity-aware reveal, policy options, batching, and optional userset checks while delegating SQL execution and connectivity to Snowflake.

**Sales use:** Introduce consistent protected-data access across Snowflake SQL editors, BI clients, and Java applications.

**Suggested opener:** “Which Snowflake JDBC consumers need different protected, masked, or revealed results based on the connected user?”

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-brochure.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-brochure.html)

### Snowflake JDBC Technical Overview

_Technical overview · `jdbc/thales-jdbc-snowflake-technical-overview.html`

[Snowflake JDBC Technical Overview](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-technical-overview.html) — Details JDBC connection, statement, and result-set proxies; object and default field mappings; identity normalization; bulk reveal; policy types; credential sources; and fail-closed allowlist behavior. It also distinguishes result handling from limitations on automatic protected-predicate rewriting.

**Sales use:** Validate the wrapper against real query patterns, datasource settings, authentication, and reveal policy.

**Suggested opener:** “Which queries, identity rules, and protected-column predicates should we include in a Snowflake JDBC validation?”

[https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-technical-overview.html](https://markbwarner.github.io/warnerscorner/jdbc/thales-jdbc-snowflake-technical-overview.html)

### Thales JDBC Wrapper Architecture

_Diagram · `jdbc/architecture.png`

[Thales JDBC Wrapper Architecture](https://markbwarner.github.io/warnerscorner/jdbc/architecture.png) — Shows an AWS Advanced JDBC Wrapper plugin with SQL parsing, metadata interception, protected-predicate rewriting, and result-field reveal through Thales services, using PostgreSQL as the illustrated database.

**Sales use:** Clarify the division of work between client, wrapper, vendor driver, database, and protection service.

**Suggested opener:** “Which controls belong in the JDBC wrapper, and which remain with the database and vendor driver?”

[https://markbwarner.github.io/warnerscorner/jdbc/architecture.png](https://markbwarner.github.io/warnerscorner/jdbc/architecture.png)

### Customer JDBC Protection Process

_Diagram · `jdbc/overall-process.png`

[Customer JDBC Protection Process](https://markbwarner.github.io/warnerscorner/jdbc/overall-process.png) — Maps discovery, protection policy, usersets, data transformation, driver setup, field mappings, and runtime policy-based query results.

**Sales use:** Turn a JDBC demo into a scoped onboarding and rollout discussion.

**Suggested opener:** “Have you assigned owners for protected tables, field mappings, user policy, and driver deployment?”

[https://markbwarner.github.io/warnerscorner/jdbc/overall-process.png](https://markbwarner.github.io/warnerscorner/jdbc/overall-process.png)

### JDBC Runtime Swimlane

_Diagram · `jdbc/swimlane.png`

[JDBC Runtime Swimlane](https://markbwarner.github.io/warnerscorner/jdbc/swimlane.png) — Breaks down connection setup, SQL interception, protected predicates, query execution, result metadata, batching, reveal calls, and returned values across the client, wrapper, database, and Thales service.

**Sales use:** Trace an actual query with technical stakeholders and identify integration checkpoints.

**Suggested opener:** “Can we walk one protected query through the driver and identify where each policy decision occurs?”

[https://markbwarner.github.io/warnerscorner/jdbc/swimlane.png](https://markbwarner.github.io/warnerscorner/jdbc/swimlane.png)

<a id="misc"></a>

## CipherTrust Integration Operations

An operational pattern for keeping long-running CipherTrust REST integrations working across token expiry.

**Suggested conversation path:** Use the token lifecycle discussion when moving a successful short demo into a batch, streaming, or long-running service workload.

### CipherTrust REST Token Refresh Pattern

_Operational guide · `misc/ciphertrust-rest-token-refresh-pattern.html`

[CipherTrust REST Token Refresh Pattern](https://markbwarner.github.io/warnerscorner/misc/ciphertrust-rest-token-refresh-pattern.html) — Explains a reusable Java helper that refreshes JWTs before expiry and refreshes and retries once when an unauthorized or token-expired response still occurs. It covers batch jobs, stream consumers, backend services, thick clients, and packaging as a utility or library.

**Sales use:** Surface production-readiness needs with integration owners whose proof of concept works only for short sessions.

**Suggested opener:** “What happens when your CipherTrust authentication token expires halfway through a batch job or a long-running consumer?”

[https://markbwarner.github.io/warnerscorner/misc/ciphertrust-rest-token-refresh-pattern.html](https://markbwarner.github.io/warnerscorner/misc/ciphertrust-rest-token-refresh-pattern.html)

<a id="pqc"></a>

## Luna & PQC Key Wrapping Basics and Value

A progression from the business risk of legacy key transport to project planning, Luna-native implementation, and stronger private-key custody.

**Suggested conversation path:** Start with the ML-KEM wrap blog, move to the project-manager briefing, then offer the Luna implementation discussion. Use the persistence note and custody guide to address key lifecycle and operational controls.

### ML-KEM Wrap Blog

_Business article · `pqc/ml-kem-wrap-blog.html`

[ML-KEM Wrap Blog](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-wrap-blog.html) — Explains envelope encryption in business-friendly language: AES protects the content, while RSA wrapping or ML-KEM key establishment protects the key exchange between systems. It frames ML-KEM as a practical response to harvest-now-decrypt-later risk and connects algorithm choices to private-key custody.

**Sales use:** Start a conversation about long-lived sensitive data, partner data exchange, and encrypted payloads crossing trust boundaries.

**Suggested opener:** “Where do encryption keys travel between your applications, partners, or cloud environments, and how long must the protected data remain confidential?”

[https://markbwarner.github.io/warnerscorner/pqc/ml-kem-wrap-blog.html](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-wrap-blog.html)

### PQC Key-Wrapping Project Briefing

_Project-manager briefing · `pqc/pqc-key-wrapping-project-briefing.html`

[PQC Key-Wrapping Project Briefing](https://markbwarner.github.io/warnerscorner/pqc/pqc-key-wrapping-project-briefing.html) — Turns cryptography into a delivery discussion: what changes from RSA wrapping to ML-KEM key establishment, what remains stable with AES-GCM, where Luna fits, and how discovery, dependencies, compatibility, and phased rollout shape the project.

**Sales use:** Bring in security architects, program managers, and crypto owners who need a migration plan.

**Suggested opener:** “If PQC migration is on your roadmap, do you have an inventory of key-transport use cases and a phased plan for the highest-value data paths?”

[https://markbwarner.github.io/warnerscorner/pqc/pqc-key-wrapping-project-briefing.html](https://markbwarner.github.io/warnerscorner/pqc/pqc-key-wrapping-project-briefing.html)

### ML-KEM Luna Implementation Guide

_Implementation guide · `pqc/ml-kem-luna-implementation-guide.html`

[ML-KEM Luna Implementation Guide](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-luna-implementation-guide.html) — Provides the technical story for Luna-native RSA-OAEP wrapping and ML-KEM encapsulation and decapsulation with AES-GCM field protection. It explains the transport envelope, Luna-backed private-key operations, and provider compatibility considerations; the RSA example creates its AES key separately from Luna.

**Sales use:** Support technical discovery with application security, platform engineering, and HSM teams once a prospect wants an implementable design.

**Suggested opener:** “Would it help to walk through a Luna-native pattern where private keys remain HSM-backed while applications protect and recover encrypted JSON fields?”

[https://markbwarner.github.io/warnerscorner/pqc/ml-kem-luna-implementation-guide.html](https://markbwarner.github.io/warnerscorner/pqc/ml-kem-luna-implementation-guide.html)

### Luna Key Persistence Patterns

_Technical note (Markdown) · `pqc/luna-key-persistence-patterns.md`

[Luna Key Persistence Patterns](https://markbwarner.github.io/warnerscorner/pqc/luna-key-persistence-patterns.md) — Collects Java persistence patterns for AES secret keys, RSA private-key entries with certificate chains, and ML-KEM recipient keypairs. It emphasizes provider-native persistence and keeping private keys on Luna; the ML-KEM example is conceptual and provider-dependent.

**Sales use:** Address key lifecycle and Java keystore questions with developers preparing an HSM-backed implementation.

**Suggested opener:** “How will your application persist and retrieve AES, RSA, and ML-KEM keys without exporting private-key bytes?”

[https://markbwarner.github.io/warnerscorner/pqc/luna-key-persistence-patterns.md](https://markbwarner.github.io/warnerscorner/pqc/luna-key-persistence-patterns.md)

### Defense in Depth: Protecting Keys Beyond the File System

_Security architecture guide · `pqc/defense-in-depth-key-custody.html`

[Defense in Depth: Protecting Keys Beyond the File System](https://markbwarner.github.io/warnerscorner/pqc/defense-in-depth-key-custody.html) — Places HSM custody within a layered design covering people, identity, networks, applications, and data. It compares storage models and uses incident lessons to distinguish reduced key-copy risk from the continuing need to govern authorized cryptographic operations.

**Sales use:** Expand an HSM discussion into a security architecture conversation about extraction, misuse, monitoring, and recovery.

**Suggested opener:** “If an application is compromised, what prevents an attacker from copying a private key or misusing an authorized cryptographic operation?”

[https://markbwarner.github.io/warnerscorner/pqc/defense-in-depth-key-custody.html](https://markbwarner.github.io/warnerscorner/pqc/defense-in-depth-key-custody.html)

### Protecting an AES-256 Key: RSA vs ML-KEM

_Diagram · `pqc/images/aes-key-protection-rsa-vs-mlkem.png`

[Protecting an AES-256 Key: RSA vs ML-KEM](https://markbwarner.github.io/warnerscorner/pqc/images/aes-key-protection-rsa-vs-mlkem.png) — Compares generating and wrapping an AES key with RSA against ML-KEM encapsulation and shared-secret-based key establishment. Both paths use AES-GCM for content encryption.

**Sales use:** Make the PQC transition understandable while keeping content encryption and key establishment distinct.

**Suggested opener:** “How are AES content keys protected when they cross your service or partner boundaries?”

[https://markbwarner.github.io/warnerscorner/pqc/images/aes-key-protection-rsa-vs-mlkem.png](https://markbwarner.github.io/warnerscorner/pqc/images/aes-key-protection-rsa-vs-mlkem.png)

### Key Storage Architecture: Flat Files to HSM

_Diagram · `pqc/images/key-storage-architecture-flat-files-to-hsm.png`

[Key Storage Architecture: Flat Files to HSM](https://markbwarner.github.io/warnerscorner/pqc/images/key-storage-architecture-flat-files-to-hsm.png) — Compares flat files and PEM, Java software keystores, managed KMS or secrets services, and customer-controlled HSMs by custody and control boundary.

**Sales use:** Structure a discovery discussion around where private keys live and who can use or copy them.

**Suggested opener:** “Which high-value private keys are still stored in files, software keystores, or application configuration?”

[https://markbwarner.github.io/warnerscorner/pqc/images/key-storage-architecture-flat-files-to-hsm.png](https://markbwarner.github.io/warnerscorner/pqc/images/key-storage-architecture-flat-files-to-hsm.png)

### RSA Keystore Models: Raw Bytes vs PrivateKeyEntry

_Diagram · `pqc/images/rsa-keystore-models-comparison.png`

[RSA Keystore Models: Raw Bytes vs PrivateKeyEntry](https://markbwarner.github.io/warnerscorner/pqc/images/rsa-keystore-models-comparison.png) — Contrasts a software demo that exports and reconstructs RSA key bytes with a certificate-backed Java PrivateKeyEntry and provider-backed key references.

**Sales use:** Help Java and HSM teams distinguish a teaching demo from an HSM-aligned persistence design.

**Suggested opener:** “Does your application retrieve a provider-backed private key, or reconstruct one from exported bytes?”

[https://markbwarner.github.io/warnerscorner/pqc/images/rsa-keystore-models-comparison.png](https://markbwarner.github.io/warnerscorner/pqc/images/rsa-keystore-models-comparison.png)

### Defense-in-Depth Key Custody Layers

_Diagram · `pqc/images/defense-in-depth-key-custody-layers.png`

[Defense-in-Depth Key Custody Layers](https://markbwarner.github.io/warnerscorner/pqc/images/defense-in-depth-key-custody-layers.png) — An illustration of concentric protective layers around a central key and hardware custody boundary, accompanying the defense-in-depth guide.

**Sales use:** Introduce layered protection before discussing individual security controls.

**Suggested opener:** “Which surrounding controls protect access to your most valuable cryptographic keys?”

[https://markbwarner.github.io/warnerscorner/pqc/images/defense-in-depth-key-custody-layers.png](https://markbwarner.github.io/warnerscorner/pqc/images/defense-in-depth-key-custody-layers.png)

<a id="scanner"></a>

## Application Assessment: PII and PQC Migration

Source-code assessment materials for finding sensitive-data and cryptography touchpoints, identifying likely change owners, and planning migration work. These are guides and positioning resources for the scanners.

**Suggested conversation path:** Lead with the relevant scanner brochure, explain the evidence and ownership model, then review a representative repository with the customer. Use the PII decision guides or PQC handouts to turn findings into work packages.

### Application Code Sensitive Data Scanner

_PII assessment brochure · `scanner/pii/code-impact-scanner-brochure.html`

[Application Code Sensitive Data Scanner](https://markbwarner.github.io/warnerscorner/scanner/pii/code-impact-scanner-brochure.html) — Introduces source-code scanning for sensitive field references, likely backend and data-access owners, JDBC candidates, complexity, and planning exports. It looks for code evidence such as field names and integration patterns rather than scanning production data values.

**Sales use:** Scope a data-protection assessment and identify where CRDP integration or JDBC substitution may reduce delivery effort.

**Suggested opener:** “Do you know which files actually own sensitive-data handling, rather than simply displaying or referencing those fields?”

[https://markbwarner.github.io/warnerscorner/scanner/pii/code-impact-scanner-brochure.html](https://markbwarner.github.io/warnerscorner/scanner/pii/code-impact-scanner-brochure.html)

### How the PII Scanner Works

_PII technical explainer · `scanner/pii/how-the-pii-scanner-works.html`

[How the PII Scanner Works](https://markbwarner.github.io/warnerscorner/scanner/pii/how-the-pii-scanner-works.html) — Explains file classification, identifier normalization, built-in and custom rules, optional literal matching, API and SQL clues, ownership correlation, complexity scoring, and JSON, CSV, and DBA-planning outputs. It shows how findings become candidate CRDP, JDBC, or data-access work.

**Sales use:** Explain assessment evidence and assumptions to architects, developers, delivery leads, and DBAs.

**Suggested opener:** “Which customer-specific field names, APIs, and database tables should an assessment recognize in your codebase?”

[https://markbwarner.github.io/warnerscorner/scanner/pii/how-the-pii-scanner-works.html](https://markbwarner.github.io/warnerscorner/scanner/pii/how-the-pii-scanner-works.html)

### Application Protection Decision Guide

_PII customer handout · `scanner/pii/application-protection-customer-handout.html`

[Application Protection Decision Guide](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-customer-handout.html) — Explains why shared backend services are often the best protect-and-reveal integration point, when direct clients are valid exceptions, and how scanner correlations help identify likely owners. It includes useful report filters and DBA handoff fields.

**Sales use:** Align application and security owners on where controls should be implemented and how to interpret assessment findings.

**Suggested opener:** “Which layer owns the data-handling decision and could enforce protection consistently for all your client channels?”

[https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-customer-handout.html](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-customer-handout.html)

### Application Protection Decision Matrix

_PII architecture matrix · `scanner/pii/application-protection-decision-matrix.html`

[Application Protection Decision Matrix](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-decision-matrix.html) — Compares integration points for multi-tier applications, direct clients, batch services, Kafka flows, JDBC-heavy services, and shared APIs. A criteria matrix connects reuse, business logic, audit needs, and existing boundaries to the architecture choice.

**Sales use:** Run a focused workshop to choose a protection control point and assign implementation ownership.

**Suggested opener:** “Does this application have a reusable service layer, or does its client already own the enterprise integration?”

[https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-decision-matrix.html](https://markbwarner.github.io/warnerscorner/scanner/pii/application-protection-decision-matrix.html)

### PII Likely Change Targets Report Snapshot

_Report screenshot · `scanner/pii/assets/change_candidates.PNG`

[PII Likely Change Targets Report Snapshot](https://markbwarner.github.io/warnerscorner/scanner/pii/assets/change_candidates.PNG) — A report screenshot with likely change targets, recommended actions, ownership indicators, JDBC candidates, and complexity fields.

**Sales use:** Show how scan results can become a filtered implementation review list.

**Suggested opener:** “Which report columns would your delivery team need to assign and prioritize migration work?”

[https://markbwarner.github.io/warnerscorner/scanner/pii/assets/change_candidates.PNG](https://markbwarner.github.io/warnerscorner/scanner/pii/assets/change_candidates.PNG)

### Application PQC Readiness Scanner

_PQC assessment brochure · `scanner/pqc/pqc-readiness-scanner-brochure.html`

[Application PQC Readiness Scanner](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-readiness-scanner-brochure.html) — Introduces source and dependency assessment for RSA, ECC, TLS, JWT, certificates, SSH, KMS, and signing touchpoints. It distinguishes implementation owners from references and describes migration worklists and CBOM-style outputs.

**Sales use:** Start a PQC scoping engagement with evidence tied to application files, likely owners, and remediation lanes.

**Suggested opener:** “Beyond your crypto inventory, do you know which application files and teams are likely to drive PQC migration effort?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-readiness-scanner-brochure.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-readiness-scanner-brochure.html)

### How the PQC Scanner Works

_PQC technical explainer · `scanner/pqc/how-the-pqc-scanner-works.html`

[How the PQC Scanner Works](https://markbwarner.github.io/warnerscorner/scanner/pqc/how-the-pqc-scanner-works.html) — Explains file classification, configurable cryptography rules, dependency hints, custom wrapper markers, merged findings, complexity estimates, remediation lanes, and JSON, CSV, HTML, and CBOM-style reporting.

**Sales use:** Help technical stakeholders understand how findings are produced and where human validation is needed.

**Suggested opener:** “Which shared libraries, custom wrappers, and generated clients must an assessment recognize to identify your real crypto owners?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/how-the-pqc-scanner-works.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/how-the-pqc-scanner-works.html)

### Why Use the Application PQC Readiness Scanner?

_PQC customer handout · `scanner/pqc/pqc-scanner-customer-positioning-handout.html`

[Why Use the Application PQC Readiness Scanner?](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-customer-positioning-handout.html) — Positions the scanner around likely change targets, ownership, reference filtering, custom wrappers, OpenAPI onboarding, and planning-friendly exports. It focuses on turning discovery into application migration work.

**Sales use:** Explain the assessment outcome to customers who already have inventory but need a delivery plan.

**Suggested opener:** “Can your current discovery output tell you what changes first, who owns it, and how to package the work?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-customer-positioning-handout.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-customer-positioning-handout.html)

### PQC Scanner Competitive Battlecard

_PQC sales battlecard · `scanner/pqc/pqc-scanner-competitive-battlecard.html`

[PQC Scanner Competitive Battlecard](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-competitive-battlecard.html) — Provides sales positioning, differentiators, buyer questions, and guidance on where inventory and discovery tools fit. Its focus is file-level evidence and migration planning; use its comparisons as discussion prompts for a customer-specific evaluation.

**Sales use:** Prepare a discovery or competitive evaluation conversation grounded in the customer's required outcomes.

**Suggested opener:** “In your evaluation, how will you test ownership accuracy and migration usefulness as well as discovery coverage?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-competitive-battlecard.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/pqc-scanner-competitive-battlecard.html)

### ML-KEM Wrap Blog: Scanner Companion

_PQC business article · `scanner/pqc/ml-kem-wrap-blog.html`

[ML-KEM Wrap Blog: Scanner Companion](https://markbwarner.github.io/warnerscorner/scanner/pqc/ml-kem-wrap-blog.html) — A scanner-folder edition of the envelope-encryption article explaining AES content protection, RSA wrapping versus ML-KEM key establishment, harvest-now-decrypt-later risk, and private-key storage choices.

**Sales use:** Connect scanner findings about legacy cryptography to a concrete key-transport use case and business risk.

**Suggested opener:** “Which RSA key-transport findings protect data whose confidentiality must last for many years?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/ml-kem-wrap-blog.html](https://markbwarner.github.io/warnerscorner/scanner/pqc/ml-kem-wrap-blog.html)

### Protecting an AES-256 Key: RSA vs ML-KEM

_Diagram · `scanner/pqc/images/aes-key-protection-rsa-vs-mlkem.png`

[Protecting an AES-256 Key: RSA vs ML-KEM](https://markbwarner.github.io/warnerscorner/scanner/pqc/images/aes-key-protection-rsa-vs-mlkem.png) — Compares generating and wrapping an AES key with RSA against ML-KEM encapsulation and shared-secret-based key establishment. Both paths use AES-GCM for content encryption.

**Sales use:** Make the PQC transition understandable while keeping content encryption and key establishment distinct.

**Suggested opener:** “How are AES content keys protected when they cross your service or partner boundaries?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/images/aes-key-protection-rsa-vs-mlkem.png](https://markbwarner.github.io/warnerscorner/scanner/pqc/images/aes-key-protection-rsa-vs-mlkem.png)

### Key Storage Architecture: Flat Files to HSM

_Diagram · `scanner/pqc/images/key-storage-architecture-flat-files-to-hsm.png`

[Key Storage Architecture: Flat Files to HSM](https://markbwarner.github.io/warnerscorner/scanner/pqc/images/key-storage-architecture-flat-files-to-hsm.png) — Compares flat files and PEM, Java software keystores, managed KMS or secrets services, and customer-controlled HSMs by custody and control boundary.

**Sales use:** Structure a discovery discussion around where private keys live and who can use or copy them.

**Suggested opener:** “Which high-value private keys are still stored in files, software keystores, or application configuration?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/images/key-storage-architecture-flat-files-to-hsm.png](https://markbwarner.github.io/warnerscorner/scanner/pqc/images/key-storage-architecture-flat-files-to-hsm.png)

### RSA Keystore Models: Raw Bytes vs PrivateKeyEntry

_Diagram · `scanner/pqc/images/rsa-keystore-models-comparison.png`

[RSA Keystore Models: Raw Bytes vs PrivateKeyEntry](https://markbwarner.github.io/warnerscorner/scanner/pqc/images/rsa-keystore-models-comparison.png) — Contrasts a software demo that exports and reconstructs RSA key bytes with a certificate-backed Java PrivateKeyEntry and provider-backed key references.

**Sales use:** Help Java and HSM teams distinguish a teaching demo from an HSM-aligned persistence design.

**Suggested opener:** “Does your application retrieve a provider-backed private key, or reconstruct one from exported bytes?”

[https://markbwarner.github.io/warnerscorner/scanner/pqc/images/rsa-keystore-models-comparison.png](https://markbwarner.github.io/warnerscorner/scanner/pqc/images/rsa-keystore-models-comparison.png)
