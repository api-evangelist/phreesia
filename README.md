# Phreesia (phreesia)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
