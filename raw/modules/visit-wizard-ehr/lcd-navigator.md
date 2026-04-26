---
id: visit-wizard-ehr-lcd-navigator
title: Complete the LCD Navigator check (step 16)
module: visit-wizard-ehr
audience: [clinician]
roles: [nurse, np, md, medical_director]
type: how-to
estimated_minutes: 5
last_reviewed: 2026-04-24
app_route: /facility/{facility_uuid}/visit-wizard-v2-page
related:
  - visit-wizard-ehr-overview
  - visit-wizard-ehr-wound-assessment
  - visit-wizard-ehr-sign-off
prerequisites:
  - visit-wizard-ehr-start-a-visit
  - visit-wizard-ehr-wound-assessment
tags: [LCD, Medicare, compliance, audit, guardrail, LCD-Navigator]
---

# Complete the LCD Navigator check (step 16)

Review and resolve the LCD Navigator™ compliance checklist at step 16 before the rendering provider can attest and sign the encounter note.

## Before you start

- Steps 1–15 of the Visit Wizard are complete for this encounter.
- You understand that the LCD Navigator™ cross-references documentation entered in earlier steps against Medicare Local Coverage Determination requirements. It does not replace clinical judgment or legal compliance review.
- Billing code selections (step 15) are finalized — changing CPT codes after passing the LCD check may invalidate one or more checklist items.

## What is the LCD Navigator™?

The **LCD Navigator™** is Medipyxis's embedded Medicare Local Coverage Determination guardrail. It automatically evaluates data from steps 1–15 and presents a 10-item checklist. Items that are satisfied by existing documentation are pre-checked. Items that require manual attestation or are flagged as incomplete are highlighted for clinician action.

<Compliance>
Passing the LCD Navigator™ checklist does not guarantee Medicare reimbursement. It is a documentation completeness guardrail. Your organization's biller and medical director are responsible for final compliance determinations.
</Compliance>

## Steps

1. **Reach step 16.** Complete steps 1–15 in sequence. Click **LCD Audit & Review** in the step navigator or click **Next** from step 15.

   ![LCD Audit & Review screen showing the Navigator panel and auto-populated checklist items](../../assets/visit-wizard/09_lcd_audit_review.png)

   *Step 16 opens the LCD Navigator™ panel. Items auto-populated from prior steps are pre-checked. Items requiring manual action are highlighted in amber.*

2. **Review the 10-item checklist.** Each item maps to a Medicare LCD requirement. Resolve any item that is not pre-checked.

   ![LCD Navigator checklist with all 10 items and their status indicators](../../assets/visit-wizard/10_lcd_audit_checklist.png)

   *The full LCD Navigator™ checklist. A green checkmark indicates the item is satisfied by existing documentation. An amber indicator requires clinician action.*

   | # | Checklist Item | How it is satisfied |
   |---|---|---|
   | 1 | **Medical necessity statement** | Documented in **Patient Context** (step 2) and **Comorbidities** (step 6) |
   | 2 | **4-week conservative care documented** | Documented in **Previous Treatments** (step 8) |
   | 3 | **Dimensions measured today** | **Length (cm)**, **Width (cm)**, and **Depth (cm)** entered in **Wound Assessment** (step 7) |
   | 4 | **Failed prior therapies listed** | Documented in **Previous Treatments** (step 8) |
   | 5 | **Appropriate HCPCS/CPT** | CPT codes selected in **Billing & Documentation** (step 15) |
   | 6 | **MUE/NCCI edits** | Auto-checked against the CMS edit tables for the selected CPT and modifier combination |
   | 7 | **Modifier validity** | Modifiers (`25`, `59`, `KX`, `JW`, `JZ`) validated against CPT code in step 15 |
   | 8 | **POS match** | Place of Service code in step 15 matches the facility type on record |
   | 9 | **Signature present** | Confirmed when **Provider Attestation** (step 17) is completed — shows as pending until then |
   | 10 | **Plan-of-care dates** | Next-visit interval and goal dates entered in **Care Planning** (step 10) |

3. **Resolve any amber items.** For each item not pre-checked, the Navigator shows a link back to the step where the missing data must be entered. Click the link to jump to that step, add the information, and return to step 16.

   <Note>
   You can jump back to any previously completed step using the step navigator on the left. After correcting the issue, return to step 16 — the Navigator refreshes automatically.
   </Note>

4. **Confirm any items requiring manual attestation.** Some items (for example, **Medical necessity statement**) require you to read and confirm a brief attestation sentence. Click **Confirm** next to each such item.

5. **Click Next** once all 10 items show a green checkmark. This advances to step 17, **Provider Attestation**.

   <Warning>
   If you cannot resolve an amber item during the visit, you may **Save Draft** and return later. The encounter note cannot be signed until all 10 LCD Navigator™ items are satisfied.
   </Warning>

---

## Result

All 10 LCD Navigator™ checklist items show a green checkmark. Step 16 is marked complete in the step navigator and you proceed to **Provider Attestation** (step 17).

The LCD Navigator™ result — including which items were auto-satisfied and which required manual confirmation — is recorded in the encounter audit log and is available to medical directors and billers for review.

## Troubleshooting

| Symptom | Likely cause | What to do |
|---|---|---|
| Item 3 (**Dimensions measured today**) not pre-checked | Wound measurements were not saved in step 7 | Return to step 7, enter Length, Width, and Depth, then save the wound record |
| Item 6 (**MUE/NCCI edits**) flagged | A code/modifier combination triggers a CMS edit | Adjust the CPT or modifier in step 15 per your biller's guidance |
| Item 8 (**POS match**) flagged | Place of Service code does not match the patient's service location type | Correct the POS code in step 15 or contact your billing team |
| **Next** button disabled after confirming all items | Item 9 (**Signature present**) is always pending at this stage | This resolves automatically when Provider Attestation is completed in step 17; proceed |

## Related

Auto-rendered from `related:` in frontmatter.
