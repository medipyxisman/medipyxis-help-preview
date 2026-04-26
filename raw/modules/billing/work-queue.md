---
id: billing-work-queue
title: Work the billing work queue
module: billing
audience: [billing]
roles: [biller, practice_admin, super_admin]
type: how-to
estimated_minutes: 5
last_reviewed: 2026-04-24
app_route: /facility/{facility_uuid}/billing/work-queue
related:
  - billing-overview
  - billing-submit-claim
  - billing-denial-management
tags: [billing, work-queue, claims, aging]
---

# Work the billing work queue

Use the **Work Queue** to review, claim, and action the pending billing items assigned to you for the day.

## Before you start

- You have the `biller` role, or `practice_admin` / `super_admin`.
- Claims from completed visits have already been generated (status **Pending** or **Needs Info**).

## Work Queue columns

Navigate to `/facility/{facility_uuid}/billing/work-queue`. The queue displays all actionable claims in a tabular view with the following columns:

| Column | Description |
|---|---|
| **Patient** | Patient name and date of birth. |
| **Payer** | Insurance carrier to which the claim will be submitted. |
| **Date of Service** | The visit date tied to the claim. |
| **Aging Bucket** | Days since the date of service, grouped into 0–30, 31–60, 61–90, 91–120, and 120+ buckets. |
| **Status** | Current claim status (Pending · Needs Info · Approved · Exported · Submitted · Paid). |
| **Denial Reason** | Populated if the claim has a linked denial; blank otherwise. |
| **Assignee** | The biller currently responsible for this claim. |
| **Actions** | Context-sensitive action buttons (e.g., **Review**, **Edit**, **Appeal**). |

![Billing Work Queue showing columns, filters, and a list of claims](../../assets/billing/billing_09_work_queue.png)
*The Work Queue with the **Aging Bucket** filter applied to show 31–60 day items.*

## Filtering the queue

Use the filter bar at the top of the Work Queue to narrow the list to a manageable set:

| Filter | Options |
|---|---|
| **Assignee** | Any biller in your facility, or **Unassigned**. |
| **Payer** | Any payer in the facility's payer list. |
| **Aging Bucket** | 0–30 · 31–60 · 61–90 · 91–120 · 120+. |
| **Denial Reason** | Any denial reason code recorded against a linked denial. |
| **Status** | Pending · Needs Info · Approved · Exported · Submitted · Paid. |

Filters stack — selecting **Aging Bucket: 31–60** and **Status: Needs Info** returns only claims that are both missing information and past 30 days.

## Steps — claim and action pending items for the day

1. **Open the Work Queue.** In the sidebar, click **Billing**, then select the **Work Queue** sub-item, or navigate directly to `/billing/work-queue`.

2. **Filter to your assignment.** In the **Assignee** filter, select your name. If your supervisor assigns work by aging bucket, also set **Aging Bucket** to the priority bucket for the day.

3. **Sort by aging.** Click the **Aging Bucket** column header to sort oldest-first. Address 120+ items before 0–30 items to protect timely-filing deadlines.

4. **Open a claim.** Click **Review** in the **Actions** column for the first claim. The claim detail panel opens.

5. **Resolve Needs Info items.** If the claim status is **Needs Info**, the panel highlights missing or invalid fields in red. Correct each field and click **Save**.

6. **Approve the claim.** Once all required data is present, click **Approve**. The status advances to **Approved** and the claim queues for the next export cycle.

7. **Handle denials.** If a claim shows a **Denial Reason**, click **Appeal** to open the Denial Management workflow. See [Denial Management](./denial-management.md) for the full triage process.

8. **Assign unassigned claims.** For claims with no **Assignee**, click the assignee cell, select a biller from the dropdown, and click **Save**. The claim will appear in that biller's filtered view.

9. **Repeat** for all remaining items in your filtered set.

## Result

At the end of your session, your filtered Work Queue should show no items in **Pending** or **Needs Info** status that fall within your assigned aging bucket. Claims you approved will advance to **Exported** during the next scheduled export run.

<Tip>
Set the **Assignee** filter to **Unassigned** at the start of each day to catch any claims that came in overnight without an owner before they age into a higher bucket.
</Tip>

<Warning>
Claims in the 120+ aging bucket may have passed payer timely-filing limits. Before approving and submitting, verify the payer's timely-filing policy and document the reason for late submission in the claim notes field.
</Warning>

## Troubleshooting

| Symptom | Likely cause | What to do |
|---|---|---|
| Claim not appearing in queue | Claim is assigned to another biller | Clear the **Assignee** filter and search by patient name |
| **Approve** button disabled | One or more required fields still missing | Scroll through the claim detail — red fields indicate what remains |
| Denial Reason column is blank for a denied claim | Denial not yet entered in the Denials tab | Navigate to **Denials** tab and triage the denial first |

## Related

Auto-rendered from `related:` in frontmatter.
