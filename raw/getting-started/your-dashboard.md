---
id: getting-started-your-dashboard
title: Tour of your dashboard
module: getting-started
audience: [clinician, intake, admin, billing, bd]
type: quickstart
estimated_minutes: 3
last_reviewed: 2026-04-24
app_route: /facility/{facility_uuid}/dashboard
related:
  - getting-started-welcome
  - oversight-cockpit-overview
tags: [onboarding, dashboard]
---

# Tour of your dashboard

Your dashboard is the launchpad for everything you do in Medipyxis. It's personalized by role — a clinician sees different widgets than a practice admin.

## Anatomy of the dashboard

![Medipyxis dashboard](../assets/dashboard/home.png)
*The home dashboard with four KPI tiles, Work Cockpits, HR Self-Service, and the Action Items + Recent Activity column.*

### 1. Welcome banner

Your name, role badge ("Licensed Healthcare Professional"), and duty status (**On Duty** / **Off Duty**) live here. The green **HIPAA** badge confirms your session is HIPAA-compliant.

### 2. KPI tiles

Four live tiles at a glance:

| Tile | What it counts | Click action |
|---|---|---|
| **My Compliance Status** | Your completed / total required credentials | Opens **My Credentials & Compliance** |
| **Unread Messages** | Unread Team Chat and patient-level messages | Opens **Team Chat** |
| **Upcoming Events** | Visits, meetings, trainings in the next 7 days | Opens **Fleet Calendar** |
| **Team Kudos** | Recognition received this month | Opens your kudos feed |

### 3. Your Work Cockpits

Role-specific shortcuts to your primary working surfaces. For clinicians: **Patient Management**, **Clinical Workflow**, **Mileage & Expenses**. For admins: replace these with **Oversight Cockpit** and **HR & Compliance**.

### 4. HR Self-Service

Two always-visible cards: **Time Off Requests** (PTO balance and submit button) and **My Credentials & Compliance** (% complete + "Users with Credentials" count).

### 5. Action Items & Recent Activity (right column)

- **Action Items** — tasks assigned to you: pending signatures, credential renewals, stuck visits, unsent faxes. A red "urgent" counter appears if anything needs immediate attention.
- **Recent Activity** — the last 20 things you did in Medipyxis, with deep links.

## Tips

<Tip>
Press ⌘K / Ctrl+K from anywhere to jump to a patient, visit, or page without using the sidebar.
</Tip>

<Tip>
Customize which KPI tiles appear by role: **Administrator → Organization Role Config**.
</Tip>

## Related

- [Oversight Cockpit overview](../modules/oversight-cockpit/overview.md)
- [Action items deep dive](../modules/dashboard/overview.md)
