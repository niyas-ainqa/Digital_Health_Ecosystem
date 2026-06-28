# Clinical Systems Landscape

The national digital health ecosystem must support a broad portfolio of clinical, diagnostic, administrative, imaging, and shared repository platforms. These systems must operate as interoperable domain platforms connected through a canonical HL7 FHIR exchange model, with legacy HL7 v2, X12, DICOM, and proprietary interfaces normalized at the boundary integration layer.

Semantic consistency across all clinical workflows must be enforced through a national terminology service supporting SNOMED CT, LOINC, ICD-10/ICD-11, and RxNorm.

## Core Clinical and Operational Systems

- **HIE (Health Information Exchange):** National interoperability fabric for cross-organizational exchange of patient, encounter, order, result, document, and claims-related data.
- **HIS (Hospital Information System):** Enterprise platform coordinating inpatient, outpatient, emergency, theatre, ward, clinical documentation, billing, and hospital operations.
- **EHR/EMR (Electronic Health Record / Electronic Medical Record):** Longitudinal patient record system used by clinicians for documentation, orders, results review, and care continuity.
- **PAS (Patient Administration System):** Registration, scheduling, admissions, discharge, transfer, encounter management, visit numbering, bed management, and demographic administration.
- **LIS (Laboratory Information System):** End-to-end pathology and laboratory workflow management including orders, specimen accessioning, analyzer integration, quality controls, and results reporting.
- **RIS (Radiology Information System):** Imaging order management, modality scheduling, protocoling, workflow orchestration, radiologist worklists, and structured reporting.
- **PACS (Picture Archiving and Communication System):** Diagnostic image storage, retrieval, viewing, and radiology distribution platform.
- **VNA (Vendor Neutral Archive):** Enterprise archive for long-term storage of DICOM and non-DICOM imaging assets, decoupled from individual PACS vendors.
- **CPOE (Computerized Provider Order Entry):** Structured clinician ordering for laboratory, imaging, medication, and procedures.
- **CDSS (Clinical Decision Support System):** Rules, alerts, pathways, order sets, medication safety checks, and evidence-based care interventions embedded into clinical workflows.
- **ePrescribing / Medication Management:** Medication ordering, formulary alignment, dispensing integration, medication reconciliation, and pharmacy interoperability.
- **Pharmacy Information System:** Medication stock, dispensing, verification, compounding, formulary, and medication administration support.
- **Nursing / Clinical Documentation Systems:** Flowsheets, triage, assessments, vitals, care plans, and bedside clinical workflows.
- **Emergency Department Information System (EDIS):** ED triage, tracking boards, emergency documentation, and acute care throughput management.
- **Operating Theatre / Surgical Management System:** Procedure scheduling, perioperative workflow, implant tracking, and operative documentation.
- **ICU / Critical Care System:** High-acuity documentation, device feeds, ventilator observations, and critical care monitoring.
- **Maternity / Neonatal Systems:** Antenatal, labour, delivery, neonatal, and maternal-child longitudinal workflows.
- **Oncology Information System:** Cancer pathway tracking, chemotherapy protocols, treatment plans, and oncology outcomes management.
- **Dialysis, Rehab, Mental Health, and Specialty Systems:** Domain-specific specialty workflows that should expose standard FHIR resources rather than remain siloed.

## Diagnostic, Imaging, and Ancillary Systems

- **Pathology Systems:** Histopathology, microbiology, cytology, molecular diagnostics, and blood sciences workflows.
- **Cardiology Information System (CVIS):** Cardiology diagnostics, ECG/echo/cath lab workflows, waveforms, measurements, and reporting.
- **Endoscopy Information System:** Procedure planning, image capture, reporting, and outcomes documentation.
- **Digital Pathology / Slide Management:** Whole-slide image archives and pathology interpretation workflows.
- **Waveform and Physiologic Monitoring Repositories:** ECG, EEG, bedside monitor streams, and physiological device output repositories.
- **Blood Bank / Transfusion System:** Blood product inventory, compatibility testing, traceability, and transfusion safety.
- **Device Integration Platforms:** Integration of analyzers, bedside devices, infusion pumps, ventilators, and IoT medical equipment into normalized clinical records.

## Shared National Repositories and Registries

- **MPI / EMPI (Master Patient Index / Enterprise MPI):** National person identity resolution layer linking all patient identities across providers and care settings.
- **Provider Registry:** Master data repository for physicians, nurses, allied health professionals, and professional roles.
- **Facility Registry:** Master registry of hospitals, clinics, laboratories, pharmacies, imaging centres, and points of service.
- **Terminology Service:** National terminology authority managing SNOMED CT, LOINC, ICD, RxNorm, local code sets, value sets, concept maps, and terminology versioning.
- **Clinical Data Repository (CDR):** Longitudinal normalized clinical repository for cross-facility patient history, summaries, observations, medications, allergies, and care plans.
- **Document Repository / XDS-style Content Services:** Storage and retrieval of discharge summaries, referral letters, clinical attachments, operative notes, and other shared documents.
- **VNA / Enterprise Imaging Repository:** Central imaging archive for national imaging retention and cross-enterprise access.
- **Population Health Management (PHM) Platform:** Cohorting, disease surveillance, quality measurement, risk stratification, outreach, and preventive analytics.
- **Consent and Privacy Repository:** Consent directives, purpose-of-use controls, patient sharing preferences, and disclosure governance.
- **Coverage / Benefits Registry:** Payer entitlements, insurance plans, member coverage, exclusions, and benefit plan logic.
- **Clinical Quality and Outcomes Repository:** Quality indicators, registries, performance benchmarking, and public health reporting datasets.

## National Administrative and Financial Platforms

- **Claims Management System:** Claim creation, submission, tracking, correction, and status monitoring.
- **Adjudication Platform:** Pricing, benefit checks, co-pay/co-insurance allocation, payment calculation, and remittance generation.
- **Pre-Authorization / Utilization Management:** Medical necessity review, eligibility checks, clinical rules, and approval workflows.
- **Fraud, Waste, and Abuse (FWA) Engine:** Pattern detection, anomaly scoring, provider utilization surveillance, and suspicious claims review.
- **Revenue Cycle / Billing System:** Charge capture, coding workflows, invoice generation, denials, and collections.
- **Payer and Regulator Portals:** Operational portals for claims submission, eligibility, payment advice, audit, compliance, and performance oversight.

## Patient, Provider, and Care Coordination Platforms

- **Patient Portal / Citizen App:** Appointments, results, medications, immunizations, documents, consent, and communication.
- **Provider Portal:** Cross-facility clinical access, referrals, shared summaries, and transaction dashboards.
- **Referral Management System:** Referral initiation, triage, scheduling, response tracking, and closure feedback.
- **Care Coordination Platform:** Shared care plans, case management, transition-of-care workflows, and multidisciplinary coordination.
- **Telehealth / Virtual Care Platform:** Remote consultation, virtual follow-up, home monitoring, and digital encounter capture.
- **CRM / Patient Engagement Platform:** Notifications, reminders, outreach campaigns, education, and follow-up communications.
