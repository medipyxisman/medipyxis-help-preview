---
id: visit-wizard-ehr-overview
title: Visit Wizard overview
module: visit-wizard-ehr
audience: [clinician]
roles: [nurse, np, md, medical_director]
type: concept
estimated_minutes: 5
last_reviewed: 2026-04-24
app_route: /facility/{facility_uuid}/visit-wizard-v2-page
related:
  - visit-wizard-ehr-start-a-visit
  - visit-wizard-ehr-wound-assessment
  - visit-wizard-ehr-lcd-navigator
  - visit-wizard-ehr-work-offline
  - visit-wizard-ehr-sign-off
tags: [visit-wizard, EHR, LCD, Medicare, offline, GPS, geofence]
---

# Visit Wizard overview

The Visit Wizard is Medipyxis's step-by-step visit documentation flow. It guides clinicians through 17 sequential steps — from patient consent to provider attestation — enforcing documentation completeness and Medicare compliance before a note can be signed.

![Visit Wizard overview screen showing the 17-step progress bar and patient header](../../assets/visit-wizard/03_visit_wizard_overview.png)

*The Visit Wizard progress bar. Each step must be completed in order; completed steps display a checkmark.*

---

## How the Visit Wizard fits into the workflow

The Visit Wizard opens from the **Fleet Calendar** (tap the appointment) or from the patient detail page. When opened, it locks to the selected patient and date of service. All documentation entered is scoped to that encounter record.

The Visit Wizard route is `/facility/{facility_uuid}/visit-wizard-v2-page`.

---

## The 17 steps

| # | Step | Key fields / notes |
|---|---|---|
| 1 | **Consent & Attestation** | HIPAA notice, telehealth consent toggle, patient e-signature |
| 2 | **Patient Context** | Reason for visit, visit type (`Initial` · `Follow-up` · `Post-op` · `Re-eval`) |
| 3 | **Review of Systems** | 14 body-system checklist |
| 4 | **Objective Assessment** | Vitals: **BP**, **HR**, **Temp**, **SpO₂**, **Respirations**, **Weight**, **Height**, **BMI** |
| 5 | **Functional Status & ADLs** | Ambulation, ADL independence, fall risk |
| 6 | **Comorbidities** | DM, PAD, CVI, CHF, lymphedema, smoking status |
| 7 | **Wound Assessment** | Etiology, staging, measurements, tissue composition, exudate, pain, infection signs, photo upload — see [Wound Assessment](./wound-assessment.md) |
| 8 | **Previous Treatments** | Offloading, compression, debridement history, prior grafts (with UIN lookup) |
| 9 | **Interventions & Treatments** | Debridement type (`sharp` · `mechanical` · `enzymatic` · `autolytic`), dressing selection |
| 10 | **Care Planning** | Goals, frequency, next-visit interval |
| 11 | **Orders & DME** | Links to the Orders & DME module for scripts |
| 12 | **Patient Education** | Handout selection, teach-back documented (`Y/N`) |
| 13 | **Procedure Supplies** | Graft SKU + UIN scanner, wastage calculation |
| 14 | **Current Medication** | Medication reconciliation |
| 15 | **Billing & Documentation** | CPT picker, E/M level, modifiers (`25`, `59`, `KX`, `JW`, `JZ`), POS code |
| 16 | **LCD Audit & Review** | LCD Navigator™ guardrail — see [LCD Navigator](./lcd-navigator.md) |
| 17 | **Provider Attestation** | "I, the rendering provider…" attestation + e-signature with ESIGN/UETA/CMS/HIPAA disclosure — see [Sign Off](./sign-off.md) |

---

## Visit Timer and GPS geofence

When the Visit Wizard opens for an in-person visit, the **Visit Timer** starts automatically. Medipyxis enforces a **25-minute GPS geofence**: the device must remain within 25 miles of the scheduled service address for the duration of in-person CPT codes. If the device leaves the geofence, the system logs the event and displays a warning banner. The timer and geofence data are attached to the encounter record for audit purposes.

<Compliance>
CMS requires that the rendering provider be physically present at the place of service for in-person procedure codes. The GPS geofence log is part of the encounter record and may be requested during a Medicare audit.
</Compliance>

---

## Save Draft and auto-save

The Visit Wizard auto-saves your work every 30 seconds. You can also save manually at any time by clicking **Save Draft** in the top toolbar. A timestamp confirms when the last save occurred. Draft visits appear in the **Fleet Calendar** with the status `Draft Saved`.

<Warning>
Closing the browser tab without saving will lose changes made since the last 30-second auto-save cycle. Use **Save Draft** before navigating away.
</Warning>

---

## Work Offline

The **Work Offline** toggle (top toolbar) lets clinicians document in areas without a reliable internet connection — for example, during a home visit. Completed steps sync automatically when connectivity is restored. See [Work Offline](./work-offline.md) for full details on what is and is not available offline.

---

## LCD Navigator™

Step 16, **LCD Audit & Review**, is powered by the LCD Navigator™ — Medipyxis's embedded Medicare Local Coverage Determination guardrail. It cross-references all documentation entered in steps 1–15 against a 10-item compliance checklist before allowing Provider Attestation. See [LCD Navigator](./lcd-navigator.md).

---

## Provider Attestation

Step 17, **Provider Attestation**, captures the rendering provider's electronic signature under the ESIGN Act, UETA, CMS, and HIPAA disclosure standards. Only users with the `md`, `np`, or `medical_director` role may complete this step. After attestation, the note is locked; changes require an **Addendum** with a documented reason. See [Sign Off](./sign-off.md).

---

## Related

Auto-rendered from `related:` in frontmatter.
