# Core Architectural Guidelines

## Interoperability and Data Exchange Principles

All clinical and operational source systems must publish and consume standardized APIs and events using HL7 FHIR as the canonical interoperability model. Legacy transactions such as HL7 v2 ADT/ORM/ORU, DICOM imaging exchanges, X12 EDI, CSV feeds, and vendor-specific interfaces must be transformed only at the boundary layer through the national integration engine.

The ecosystem should standardize on core FHIR resources such as `Patient`, `Encounter`, `Observation`, `Condition`, `Procedure`, `MedicationRequest`, `DiagnosticReport`, `ImagingStudy`, `DocumentReference`, `Coverage`, `Claim`, and `ExplanationOfBenefit`.

## Terminology and Data Normalization Principles

All incoming and outgoing clinical content must be normalized through a governed terminology service.
- **SNOMED CT:** Use for clinical concepts and problem lists.
- **LOINC:** Use for laboratory tests and observations.
- **ICD-10/ICD-11:** Use for classification and reporting.
- **RxNorm:** Use for medications.

Concept mapping, value set governance, code validation, deprecation handling, and terminology version alignment must be centrally managed to ensure semantic interoperability across the ecosystem.

## Recommended Architectural Positioning

For national architecture purposes, group systems into the following tiers:

1. **Systems of Capture:** HIS, PAS, EHR, LIS, RIS, PACS, pharmacy, specialty systems.
2. **Systems of Exchange:** HIE, API Gateway, Integration Engine, messaging/event broker, document exchange.
3. **Systems of Record / National Truth:** MPI, provider registry, facility registry, terminology service, coverage registry, consent repository, VNA, CDR.
4. **Systems of Intelligence and Oversight:** PHM, analytics platforms, FWA engine, quality measurement, AI/RAG services, regulatory reporting.

This separation ensures that local provider systems remain operationally autonomous while national services enforce interoperability, identity integrity, terminology normalization, longitudinal record availability, and ecosystem-wide governance.

## Key Implementation Domains

### Microservices & Workflow Orchestration
Architect asynchronous microservices for decentralized clinical workflows. Design specific synchronization solutions for Command Center, Referral, and Appointment routing, utilizing PostgreSQL persistence for high-availability transactional integrity.

### Identity Management & Zero-Trust Access
Architect complex Identity Provider (IdP) frameworks. Implement non-standard authentication flows by building custom Keycloak Java Authenticator SPIs tightly integrated with Identity Management systems. Oversee rigorous technical security scans across public infrastructure.

### Financial Clearinghouse Operations
Design high-throughput rules engines for claims validation, Fraud, Waste, and Abuse (FWA) detection, and automated adjudication. Implement native multicurrency support directly into business claim forms.

### Enterprise AI Stack & Platform Engineering
Direct the development of integrated AI platforms that host AI agents, manage independent repository folders securely, and handle custom documentation tasks. Drive architectural strategies using Retrieval-Augmented Generation (RAG). Deploy vector databases including pgvector and Chroma DB. Embed RAG pipelines directly inside Model Context Protocol (MCP) servers to expose clinical data safely to AI agents without compromising patient privacy.

### Infrastructure Automation & Administration
Orchestrate cloud infrastructure utilizing Docker volume mapping, Ansible playbooks, and AI-driven automation within GitLab-based CI/CD pipelines. Enforce strict Linux server administration protocols. Verify that all administrative access utilizes the `sudo` group, and establish secure remote credentials using the exact `ssh-copy-id` command syntax.
