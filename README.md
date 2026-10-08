<div align="center">

**English** · [العربية](README.ar.md)

# Complaints Management System

**An Arabic-first complaints system for Saudi online stores.**
It covers a complaint from the first call to the final report, and food-safety cases can't get lost along the way.

[**Open the live demo →**](https://complaints-saas-demo.vercel.app)  ·  [Watch the 42-second tour](media/features-42s.mp4)

<a href="media/features-42s.mp4"><img src="media/teaser-preview.gif" width="260" alt="Short preview of the app" /></a>

</div>

**Try it:** open the demo and pick a role on the login screen: owner, quality manager, factory manager or customer service. Each role sees only its own part of the work. Every name, phone number and order in the demo is made up.

Built and designed end to end by **Mohammed Altounsi**, [LinkedIn](https://www.linkedin.com/in/mohammed-altounsi/).

---

## Screens

<table>
<tr>
<td align="center"><img src="screenshots/02-dashboard.png" width="200" alt="Dashboard" /><br/><sub>Dashboard</sub></td>
<td align="center"><img src="screenshots/03-new-found.png" width="200" alt="New complaint" /><br/><sub>New complaint</sub></td>
<td align="center"><img src="screenshots/04-detail-C39.png" width="200" alt="Emergency complaint" /><br/><sub>Emergency case</sub></td>
<td align="center"><img src="screenshots/06-quality-emergency.png" width="200" alt="Quality queue" /><br/><sub>Quality queue</sub></td>
</tr>
<tr>
<td align="center"><img src="screenshots/08-compensation.png" width="200" alt="Compensation" /><br/><sub>Compensation</sub></td>
<td align="center"><img src="screenshots/09-reports.png" width="200" alt="Reports" /><br/><sub>Reports</sub></td>
<td align="center"><img src="screenshots/10-lot.png" width="200" alt="Batch lookup" /><br/><sub>Batch (LOT) lookup</sub></td>
<td align="center"><img src="screenshots/13-security-log.png" width="200" alt="Security log" /><br/><sub>Security log</sub></td>
</tr>
</table>

## What it does

**Logging a complaint takes a minute.** Customer service types the customer's phone, order number or email, and the online-store order fills itself in. One complaint can cover several products, each with its own issues and batch number. Photos, videos and voice notes upload straight from the phone. Complaints from a branch or any other channel are logged the same way.

**It reaches the right person.** Each complaint goes to the quality team or the factory based on what went wrong. The responsible manager gets an email with the complaint number.

**Food-safety cases come first.** An emergency always goes to the quality manager and sits at the top of every screen in red. Collecting a sample needs a yes from two people, and that record can't be edited afterwards.

**Compensation is on record.** Every resolution stores the compensation type, amount and a note. Compensations still to be paid have their own list. A cost report breaks spending down by month, product and batch.

**Reports a manager can use.** It shows trends and splits by product, city and channel. You can trace every complaint linked to one production batch and see response times. You choose which sheets go into the Excel export.

**Replying to the customer is one tap.** A ready WhatsApp message names the product and the order.

**Made for phones and for Arabic.** Right-to-left throughout, built for the phone first, with a dark mode. The Arabic is written for Saudi staff, not translated.

**Safe by default.**
- The owner manages staff accounts inside the app.
- The last person in a role can't be switched off by mistake.
- Every destructive action asks for confirmation.
- Sign-ins are logged, and an account pauses after repeated wrong passwords.

**Connected to Salla.** Orders arrive live from the store, and a nightly job fills any gaps. A health check reports whether the connection, the nightly job and storage are working.

## Built with

`Next.js 16` · `React 19` · `TypeScript` · `Supabase (Postgres, Auth, Storage)` · `Tailwind CSS 4` · `Vercel` · `PostHog (EU)`

## Security

- Each store's data is isolated inside the database itself (row-level security). Staff only ever see their own store.
- Customer photos and videos sit in private storage behind short-lived links. Nothing is public.
- The Salla connection keys are encrypted at rest.
- A strict content security policy blocks other sites from loading or framing the app.

---

> The source code is private. This repository is a showcase. For a walkthrough, or a demo set up for your own store, reach me on [LinkedIn](https://www.linkedin.com/in/mohammed-altounsi/).
