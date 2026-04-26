---
id: getting-started-clinician-first-hour
title: Clinician first hour
module: getting-started
audience: [clinician]
roles: [nurse, np, md, ma]
type: quickstart
estimated_minutes: 45
last_reviewed: 2026-04-24
app_route: /facility/{facility_uuid}/pm-clinician-dashboard
related:
  - visit-wizard-start-a-visit
  - visit-wizard-wound-assessment
  - visit-wizard-work-offline
  - fleet-calendar-my-day
tags: [onboarding, clinician, nurse]
---

# Clinician first hour

By the end of this hour you will have logged in, reviewed your day, opened a patient, completed a full visit with wound assessment and photos, and signed it off. You can do this on your laptop or your issued tablet.

## Before you start

- Your practice admin has assigned you to at least one facility and one role.
- You have at least one scheduled visit for today (if not, your admin can assign one from **Fleet Calendar**).
- If you're on a tablet, install the Medipyxis Clinician mobile app from your admin's MDM link.

## Step 1 — See your day (5 min)

1. After logging in, click **Patient Management** in the sidebar.
2. The **Clinician Dashboard** shows today's visits, grouped by stop. Each card shows patient name, address, last wound status, and a route-position badge.
3. Click a visit card to see the patient summary before you drive.

<Tip>
Open **Fleet Calendar** (week view) once per Monday to preview the whole week — it makes routing faster on Tuesday.
</Tip>

## Step 2 — Start a visit (10 min)

1. From a visit card, click **Start Visit**. Medipyxis opens the **Visit Wizard**.
2. If you're offline, a yellow **Offline** banner appears — keep going. Everything saves locally.
3. Move through the wizard steps. Skip nothing the wizard flags with a red dot — those are required for billing.

Full step-by-step: [Visit Wizard: Start a visit](../../modules/visit-wizard-ehr/start-a-visit.md)

## Step 3 — Complete the wound assessment (15 min)

1. On the **Wound Assessment** step, tap **+ Add wound** or open an existing wound from the patient's wound list.
2. Confirm the wound type, location, stage, and enter measurements (L × W × D in cm).
3. Tap the camera icon to capture the wound photo. Medipyxis auto-tags the image to the patient + visit + wound.
4. Select tissue types (granulation, slough, eschar) and exudate amount.

Detailed guide: [Wound assessment](../../modules/visit-wizard-ehr/wound-assessment.md)

<Compliance>
The **LCD Navigator™** check runs in real time. If a required CMS criterion for the selected treatment isn't met, the wizard blocks sign-off and shows you exactly which field to fix. This is the difference between a billable note and a denied claim.
</Compliance>

## Step 4 — Order supplies or a graft (5 min)

If this visit requires a graft, DME, or follow-up order:

1. On the **Procedures & Supplies** step, click **Add item from inventory**.
2. Scan or pick the **UIN** (Unique Inventory Number) of the graft being applied — Medipyxis locks that lot to this patient + visit.
3. Add any DME or home health order on the **Care Planning** step.

## Step 5 — Sign off (5 min)

1. On the final step, review the generated narrative. The wizard assembles it from your inputs — you can edit.
2. Click **Sign & Complete**. Your electronic signature, timestamp, and device are stamped.
3. The visit now flows to billing automatically. You're done.

## Step 6 — Housekeeping (5 min)

- Before signing out, check the **Action Items** card on your dashboard. If you have pending addendums or signatures, finish them now.
- Log mileage with the **Mileage & Expenses** cockpit shortcut.

## Result

- One real visit signed, billed-ready, with photos, wound measurements, and narrative.
- You know where to start every day (Patient Management), where your calendar lives (Fleet Calendar), and where to chat your team (Team Chat).

## Next up

- [Work offline](../../modules/visit-wizard-ehr/work-offline.md)
- [Add a photo later (addendum)](../../modules/visit-wizard-ehr/sign-off.md)
- [Keyboard shortcuts](../../quick-reference/nurse-daily.md)
