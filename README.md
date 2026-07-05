# Phreesia (phreesia)

Phreesia is a patient intake, registration, scheduling, payments, and engagement platform for healthcare organizations, powering more than 150 million patient visits annually. It delivers digital check-in, mobile intake and consent forms in 20+ languages, logic-driven patient interviews, real-time insurance eligibility verification, and patient payments, and pushes the resulting data back into the provider's systems of record.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/phreesia/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/phreesia/refs/heads/main/apis.yml)

## Access Model — Please Read

Phreesia is **not a self-serve public API product.** It is an enterprise healthcare platform whose integrations are delivered by a dedicated interoperability team. Phreesia is an HL7 Organizational Member and integrates using open healthcare standards — **HL7v2, FHIR, CCD, and CSV** — alongside proprietary APIs and data extracts, providing bidirectional interfaces into EHR/EMR, practice management (PM), HIE, data warehouse, and data lake systems (Epic, athenahealth, eClinicalWorks, NextGen, Oracle Health/Cerner, Veradigm, Meditech, ModMed, Greenway, AdvancedMD, and more).

As of this writing there is **no publicly documented developer portal, API reference, self-service key registration, or published OpenAPI** for Phreesia. Access is arranged through Phreesia's sales and integration teams as part of a platform engagement. Pricing is not published — it is custom/contact-sales (third-party sources suggest entry plans starting around a few hundred dollars per month, escalating with locations and add-on features).

Because there is no public reference surface, the APIs listed below are **modeled** from Phreesia's published product and integration capabilities. Each carries `endpointsModeled: true` in `apis.yml`. They represent logical capability areas and the standards (HL7v2, FHIR, X12) those capabilities are typically delivered over — they are **not** transcribed from a public Phreesia API reference, and no endpoint paths or base URLs have been fabricated.

## Tags

- Healthcare
- Patient Intake
- Patient Registration
- Patient Engagement
- Scheduling
- Payments
- Insurance Eligibility
- HL7
- FHIR
- Interoperability
- EHR Integration
- Partner API

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs (Modeled)

### Phreesia Intake & Forms API

Digital intake, consent, and clinical questionnaire capture — logic-driven interviews customized per patient and delivered as mobile intake in 20+ languages. Completed intake, consent, and patient-reported outcome data flow into the EHR via HL7v2, FHIR (e.g. `QuestionnaireResponse` / `DocumentReference`), CCD, or CSV.

- **Human URL:** [https://www.phreesia.com/products/patient-engagement/](https://www.phreesia.com/products/patient-engagement/)
- **Endpoints:** Modeled from published product capability (not public reference docs)

### Phreesia Registration & Demographics API

Bidirectional patient registration and demographic data exchange — verify and update patient identity, contact, and demographic fields and write them back to the EHR/PM system of record. Modeled on HL7v2 ADT and FHIR `Patient`/`Coverage` resource flows.

- **Human URL:** [https://www.phreesia.com/solutions/health-systems/](https://www.phreesia.com/solutions/health-systems/)

### Phreesia Scheduling & Appointments API

Appointment scheduling, reminders, and contactless mobile/kiosk check-in, driving arrival status back into the practice management system. Modeled on HL7v2 SIU and FHIR `Appointment`/`Schedule`/`Slot` flows.

- **Human URL:** [https://www.phreesia.com/solutions/health-systems/](https://www.phreesia.com/solutions/health-systems/)

### Phreesia Insurance Eligibility Verification API

Real-time insurance eligibility and benefits verification at or before check-in, returning coverage, copay, and patient-responsibility estimates. Modeled on X12 270/271 eligibility and FHIR `Coverage`/`CoverageEligibilityResponse` flows.

- **Human URL:** [https://www.phreesia.com/products/integrations/](https://www.phreesia.com/products/integrations/)

### Phreesia Payments API

Patient payments, card-on-file, copay collection, and payment plans, with real-time payment posting back to the PM/billing system.

- **Human URL:** [https://www.phreesia.com/pricing/](https://www.phreesia.com/pricing/)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/phreesia)
- [Website](https://www.phreesia.com/)
- [Documentation / Integrations](https://www.phreesia.com/products/integrations/)
- [Plans / Pricing](https://www.phreesia.com/pricing/)
- [Company](https://www.phreesia.com/company/about-us/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
