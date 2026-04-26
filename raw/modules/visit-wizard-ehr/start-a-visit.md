---
id: visit-wizard-ehr-start-a-visit
title: Start a visit in the Visit Wizard
module: visit-wizard-ehr
audience: [clinician]
roles: [nurse, np, md]
type: how-to
estimated_minutes: 4
last_reviewed: 2026-04-24
app_route: /facility/{facility_uuid}/visit-wizard-v2-page
related:
  - visit-wizard-ehr-overview
  - visit-wizard-ehr-wound-assessment
  - visit-wizard-ehr-work-offline
  - visit-wizard-ehr-sign-off
prerequisites:
  - visit-wizard-ehr-overview
tags: [visit-wizard, start, fleet-calendar, GPS, timer, patient-context]
---

# Start a visit in the Visit Wizard

Open the Visit Wizard from the Fleet Calendar or a patient detail page, confirm the patient context, and begin the Visit Timer before documenting the encounter.

## Before you start

- Your appointment is in `Scheduled` status on the **Fleet Calendar**.
- Your device has location services enabled (required for the GPS geofence on in-person visits).
- If you are in an area with unreliable internet, review [Work Offline](./work-offline.md) before opening the wizard.

## Steps

### Open from the Fleet Calendar

1. **Navigate to Fleet Calendar.** Click **Fleet Calendar** in the sidebar. The calendar opens in Day view by default, showing swim lanes per provider.

   ![Fleet Calendar patient header showing the scheduled appointment](../../assets/visit-wizard/01_patient_header.png)

   *The patient header card on the Fleet Calendar appointment tile, showing name, appointment type, and time slot.*

2. **Tap the appointment tile.** A detail popover appears with the patient name, appointment type, date, and time.

3. **Click Start Visit.** The Visit Wizard opens to step 1, **Consent & Attestation**. The **Visit Timer** starts automatically and appears in the top toolbar.

   ![Wound Cockpit view accessible from the patient tile](../../assets/visit-wizard/02_wound_cockpit.png)

   *The Wound Cockpit panel, accessible from the patient appointment tile, gives a pre-visit snapshot of active wounds before entering the Visit Wizard.*

### Open from a patient detail page

1. **Locate the patient.** Use the global search (`Ctrl+K` / `Cmd+K`) or navigate to the patient list.
2. **Open the patient detail page.** Click the patient's name.
3. **Click Start Visit** in the patient action bar. The Visit Wizard opens and binds to today's date of service.

---

### Step 1 — Consent & Attestation

4. **Present the HIPAA notice to the patient.** The full HIPAA privacy notice is displayed on screen.
5. **Toggle Telehealth Consent** if the visit is being conducted via telehealth.
6. **Collect patient e-signature.** Hand the device to the patient or use the signature pad. Click **Confirm Signature**.

---

### Step 2 — Patient Context

7. **Select the Visit Type.** Choose one of: `Initial`, `Follow-up`, `Post-op`, or `Re-eval`.

   ![Visit Wizard step list — top half showing steps 1 through 8](../../assets/visit-wizard/05_visit_wizard_steps_top.png)

   *The Visit Wizard step navigator. The active step is highlighted; completed steps show a checkmark.*

8. **Enter the Reason for Visit.** Type a brief clinical summary (for example, "Evaluation and treatment of right heel diabetic foot ulcer").
9. **Click Next** to proceed to step 3, **Review of Systems**.

   ![Visit Wizard step list — bottom half showing steps 9 through 17](../../assets/visit-wizard/04_visit_wizard_steps_bottom.png)

   *The lower portion of the step navigator, showing steps 9–17 including LCD Audit & Review and Provider Attestation.*

---

## Result

The Visit Wizard is open, the **Visit Timer** is running, and you are in the 17-step documentation flow. The step navigator on the left shows your current position. You can return to any previously completed step by clicking it in the navigator, but you cannot skip ahead to an uncompleted step.

<Note>
The Visit Timer timestamp and GPS coordinates are captured at the moment you click **Start Visit**. If you open the wizard significantly before arriving on-site, the geofence check may log a mismatch. Open the wizard when you are at or near the service address.
</Note>

<Tip>
If you need to pause and resume a visit, click **Save Draft** and close the wizard. The appointment status updates to `Draft Saved` on the Fleet Calendar. Reopen the wizard from the same appointment tile to resume where you left off.
</Tip>

## Troubleshooting

| Symptom | Likely cause | What to do |
|---|---|---|
| **Start Visit** button is grayed out | Appointment is in `Canceled` or `No Show` status | Update the appointment status to `Scheduled` before starting |
| Visit Timer shows "GPS unavailable" | Location services are disabled on the device | Enable location permissions for the browser or the Medipyxis app in device settings |
| Wizard opens but shows the wrong patient | Tapped the wrong appointment tile | Close the wizard (**Save Draft** if prompted), then reopen from the correct tile |
| Step 1 signature pad is unresponsive | Touch input not supported in the current browser | Switch to a supported mobile browser or use the Medipyxis mobile app |

## Related

Auto-rendered from `related:` in frontmatter.
