# Warnerscorner Content Guide

[Browse the hosted content](https://markbwarner.github.io/warnerscorner/)

Business briefings, technical guides, assessment resources, and supporting media for Thales data protection, key management, analytics, and post-quantum migration.

Each document includes a summary, a sales use, and a suggested conversation opener.

## Browse by topic

- [Cloud Key Control and Data Governance](#cckm) (`cckm/`)
- [CRDP Design, Implementation, and Operations](#crdp) (`crdp/`)
- [Database, Analytics, and Secure AI](#database) (`database/`)
- [Client-Side End-to-End Data Protection](#end-to-end) (`end-to-end/`)
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

<a id="crdp"></a>

## CRDP Design, Implementation, and Operations

Practical guides for configuring CipherTrust RESTful Data Protection, validating application integration, and operating containerized protection services.

**Suggested conversation path:** Start with the best-practices guide to agree on policy, identity, and ownership, then use the implementation guide to validate deployment, API behavior, performance, and recovery.

### CRDP Best Practices: Design, Deployment, and Operations

_Best-practices guide · `crdp/crdp-best-practices-streamlined.html`_

[CRDP Best Practices: Design, Deployment, and Operations](https://markbwarner.github.io/warnerscorner/crdp/crdp-best-practices-streamlined.html) — Organizes CRDP design and operations around domains, keys, protection policies, UserSets, JWT identity, caching, rotation, monitoring, recovery, and licensing reconciliation. It explains the responsibilities shared by security, application, and platform teams, with deployment workflows and operational examples.

**Sales use:** Align security and platform stakeholders on the controls and operating model needed to take a CRDP deployment into production.

**Suggested opener:** “Who owns protection policy, reveal authorization, rotation, and recovery for your CRDP services, and how are those responsibilities tested?”

[https://markbwarner.github.io/warnerscorner/crdp/crdp-best-practices-streamlined.html](https://markbwarner.github.io/warnerscorner/crdp/crdp-best-practices-streamlined.html)

### CRDP Implementation Guide

_Technical implementation guide · `crdp/crdp-implementation-guide-2026-10-23.html`_

[CRDP Implementation Guide](https://markbwarner.github.io/warnerscorner/crdp/crdp-implementation-guide-2026-10-23.html) — Provides configuration procedures, API requests, workflow diagrams, Docker validation, Kubernetes and Helm deployment templates, and an optional AKS path. It includes JWT authorization tests, bulk-response validation, Prometheus metrics, load-testing examples, autoscaling guidance, and upgrade and recovery procedures.

**Sales use:** Support a hands-on workshop with application engineers and DevOps teams to validate deployment, access controls, service capacity, and acceptance evidence.

**Suggested opener:** “Can we validate one protect-and-reveal workload with your real identity provider, deployment platform, and expected concurrency before production?”

[https://markbwarner.github.io/warnerscorner/crdp/crdp-implementation-guide-2026-10-23.html](https://markbwarner.github.io/warnerscorner/crdp/crdp-implementation-guide-2026-10-23.html)

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

### Thales Databricks Integration Story Video

_Video (WMV) · `database/databricks/thales-databricks-integration-story.wmv`

[Thales Databricks Integration Story Video](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv) — A downloadable WMV video resource for the Databricks integration story. Playback may require a compatible local media player.

**Sales use:** Offer the video as a follow-up resource alongside the Databricks brochure and architecture diagrams.

**Suggested opener:** “Would a video follow-up help your team prepare for the Databricks integration discussion?”

[https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv](https://markbwarner.github.io/warnerscorner/database/databricks/thales-databricks-integration-story.wmv)

### Cloud Database Column Protection Options

_Architecture decision guide · `database/snowflake/thales-cloud-database-column-protection-options.html`_

[Cloud Database Column Protection Options](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-cloud-database-column-protection-options.html) — Compares server-side Snowpark Container Services integration with client-side Snowflake JDBC protection and hybrid approaches. It covers consumer coverage, bypass paths, identity, workload performance, schema and metadata impacts, operational ownership, and managed-database extensibility limits.

**Sales use:** Help architects, DBAs, and delivery leads choose the protection pattern that covers their actual producers, consumers, and operating constraints.

**Suggested opener:** “Which workloads can use a governed server-side path, which require JDBC controls, and how will you govern access that bypasses either path?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-cloud-database-column-protection-options.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-cloud-database-column-protection-options.html)

### JDBC Protection for Snowflake: Database Resource

_Business brochure · `database/snowflake/thales-jdbc-snowflake-brochure.html`_

[JDBC Protection for Snowflake: Database Resource](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-brochure.html) — Presents the Snowflake JDBC wrapper as a policy-aware access layer for familiar SQL tools, BI clients, and applications. It explains configured protected fields, connected-user identity, CRDP or CADP Centralized reveal, policy and metadata choices, datasource overrides, and userset-based allowlist controls.

**Sales use:** Introduce governed read-time access to Snowflake teams evaluating how existing JDBC consumers should handle protected fields.

**Suggested opener:** “Which Snowflake JDBC tools need ciphertext, masked, or revealed results based on the connected user and centrally managed policy?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-brochure.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-brochure.html)

### Snowflake JDBC Technical Overview: Database Resource

_Technical overview · `database/snowflake/thales-jdbc-snowflake-technical-overview.html`_

[Snowflake JDBC Technical Overview: Database Resource](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-technical-overview.html) — Details the wrapper and vendor-driver flow, object-scoped field mappings, identity normalization, bulk reveal, per-row metadata headers, allowlist checks, and credential sources. It also covers DbVisualizer dependency deployment, validation and in-place transformation utilities, and CSV loader modes.

**Sales use:** Plan a technical validation of real queries, external-policy metadata, driver dependencies, datasource configuration, and controlled data conversion.

**Suggested opener:** “Can we test your Snowflake queries, per-row metadata headers, and user identities with the wrapper before rolling it out to analyst tools?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-technical-overview.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-jdbc-snowflake-technical-overview.html)

### Thales Snowflake Customer Security Overview

_Customer overview · `database/snowflake/thales-snowflake-customer-security-overview.html`_

[Thales Snowflake Customer Security Overview](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-snowflake-customer-security-overview.html) — A customer-facing overview for discussing Thales security and data protection in Snowflake environments.

**Sales use:** Use in an initial discussion with Snowflake platform and security teams to identify their data protection priorities.

**Suggested opener:** “What are your top security priorities for the sensitive data you use in Snowflake?”

[https://markbwarner.github.io/warnerscorner/database/snowflake/thales-snowflake-customer-security-overview.html](https://markbwarner.github.io/warnerscorner/database/snowflake/thales-snowflake-customer-security-overview.html)

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

<a id="jdbc"></a>

## JDBC Protection for Cloud Data Access

Business and technical resources for applying Thales policy through JDBC wrappers and drivers used by SQL tools, BI clients, and applications.

**Suggested conversation path:** Start with the database-specific brochure, then use the technical overview to scope configuration, identity, and validation.

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

### PQC Guide for Thales CipherTrust Manager

_Migration planning guide · `pqc/ciphertrust-pqc-cm-guide.html`_

[PQC Guide for Thales CipherTrust Manager](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-guide.html) — Explains how quantum risk affects confidentiality and long-term trust. It covers CipherTrust Manager capabilities and limits, signing in a Zero Trust design, and using a cryptographic bill of materials (CBOM) to prioritize migration work.

**Sales use:** Use in an initial workshop to prioritize long-lived data and signing workflows and identify candidates for a pilot.

**Suggested opener:** “Which data and signed artifacts need to remain trustworthy for years, and where would you start a PQC pilot?”

[https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-guide.html](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-guide.html)

### PQC Implementation Guide for Thales CipherTrust Manager

_Technical implementation guide · `pqc/ciphertrust-pqc-cm-implementation-guide.html`_

[PQC Implementation Guide for Thales CipherTrust Manager](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-implementation-guide.html) — Walks through ML-DSA artifact signing, signing mode selection, external mu, and a GitHub Actions pipeline. It compares CipherTrust Manager and Luna HSM roles and includes inventory examples and acceptance tests.

**Sales use:** Use with platform and application security teams to scope a signing pilot, including verification and rejection tests.

**Suggested opener:** “Which artifact pipeline could you use to test post-quantum signing, verification, and rejection of tampered artifacts?”

[https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-implementation-guide.html](https://markbwarner.github.io/warnerscorner/pqc/ciphertrust-pqc-cm-implementation-guide.html)

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

