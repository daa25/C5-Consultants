# C5 Website Measurement System

## What is measured now

C5's website already sits behind Cloudflare. The site now routes high-value actions through dedicated first-party conversion pages so each action creates a distinct request/page path that can be counted in Cloudflare.

### Conversion paths

| Business action | Tracking path |
|---|---|
| Main website phone call | /track-call-home.html |
| Main website email | /track-email-home.html |
| Employment email | /track-employment-email.html |
| Church Security phone call | /track-call-church.html |
| Church Security email | /track-email-church.html |
| Church appointment request | /track-church-appointment.html |
| Event Security phone call | /track-call-event.html |
| Event Security email | /track-email-event.html |

The normal landing pages remain:
- / — main website
- /church-security.html — Church Security campaign/landing page
- /event-security.html — Event Security campaign/landing page

## KPI definitions

- Visitors = unique people/devices reaching the site (Cloudflare estimate).
- Requests = all files/resources requested from the site; this is not the same as leads.
- Landing-page views = visits/page views to a specific C5 service page.
- Call intent = a visit/request to a track-call-*.html page.
- Email intent = a visit/request to a track-email-*.html page.
- Appointment request = a visit/request to /track-church-appointment.html.
- Lead conversion rate = total lead-intent conversions / landing-page visitors × 100.
- Appointment conversion rate = church appointment requests / church-security landing-page visitors × 100.

## Cloudflare reporting

In Cloudflare, use Security Analytics / Traffic and filter by URI Path for any tracking path above. Zone-level Security Analytics is available on all plans. Free-plan retention is up to 7 days and the maximum query window is 24 hours, so record weekly KPI totals if longer-term trend reporting is needed.

For privacy-first page analytics, Cloudflare Web Analytics can also be enabled for the hostname. It reports visits and page views but does not currently support custom events, which is why this site uses distinct first-party conversion paths.

## Weekly scorecard

Record:
1. Unique visitors
2. Main-page views
3. Church Security page views
4. Event Security page views
5. Main call intents
6. Main email intents
7. Church call intents
8. Church email intents
9. Church appointment requests
10. Event call intents
11. Event email intents
12. Total lead intents
13. Lead conversion rate
14. Appointment conversion rate

## Important interpretation

A tracking-page hit means the visitor clicked/took the action far enough to launch the phone or email workflow. It does not prove a completed phone conversation, sent email, signed contract, or collected revenue. Those should be reconciled against actual calls, inbox messages, booked appointments, and closed deals.
