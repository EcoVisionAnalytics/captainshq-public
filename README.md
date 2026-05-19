# CaptainsHQ SaaS Case Study

![CaptainsHQ logo](assets/logo/captainshq-logo.png)

CaptainsHQ is a CRM and operations platform for charter captains. It centralizes booking flows, customer management, automated reminders, revenue and cost tracking, analytics, communications, and public booking workflows.

This repository presents the product, architecture, and workflow design behind CaptainsHQ.

## Product Focus

- CRM for fishing charter captains and small marine service businesses.
- Automated reminders for captains and clients.
- Revenue, cost, and cash-flow analytics.
- Customer management and booking workflows.
- Public trip booking flow designed for mobile users.
- Workspace, communication, and team-oriented settings.

## Product Screenshots

| Analytics dashboard | Workspace settings |
| --- | --- |
| ![Analytics dashboard](assets/screenshots/analytics-dashboard.png) | ![Workspace settings](assets/screenshots/settings-workspace.png) |

| Team workspace | Communications | Public booking |
| --- | --- | --- |
| ![Team workspace](assets/screenshots/team-workspace.png) | ![Communications settings](assets/screenshots/communications-settings.png) | ![Public booking flow](assets/screenshots/public-booking-flow.png) |

| Pricing and packaging |
| --- |
| ![Pricing and packaging](assets/screenshots/pricing-page.png) |

## What This Repo Should Communicate

- Full-stack SaaS architecture.
- Django REST API and Next.js PWA patterns.
- Booking, customer, calendar, and payment workflows.
- Small-business operational software design.
- Mobile-first UX and installable app behavior.

## Architecture Summary

```mermaid
flowchart LR
  PublicBooking["Public booking page"] --> Web["Next.js PWA"]
  Captain["Captain dashboard"] --> Web
  Web --> API["Django REST API"]
  API --> DB[("PostgreSQL")]
  API --> Payments["Payment provider"]
  API --> Messaging["SMS and email reminders"]
  API --> Analytics["Revenue and booking analytics"]
```

## Stack

- Django REST Framework.
- PostgreSQL.
- Next.js with TypeScript.
- Tailwind CSS.
- React Query.
- Stripe.
- Twilio/SMS and email integrations.
- Vercel and Cloud Run style deployment.
