<div align="center">

**English** · [العربية](README.ar.md)

# Complaints Management System

A web app for logging and handling customer complaints for online stores on Salla. Arabic, right to left.

[Live demo](https://complaints-saas-demo.vercel.app) · [42-second video tour](media/features-42s.mp4)

<a href="media/features-42s.mp4"><img src="media/teaser-preview.gif" width="260" alt="Preview of the app" /></a>

</div>

To try it, open the demo and pick a role on the login screen: owner, quality manager, factory manager or customer service. Each role sees different screens. All names, phone numbers and orders in the demo are made up.

Built by **Mohammed Altounsi**, [LinkedIn](https://www.linkedin.com/in/mohammed-altounsi/).

---

## Screens

<table>
<tr>
<td align="center"><img src="screenshots/02-dashboard.png" width="200" alt="Dashboard" /><br/><sub>Dashboard</sub></td>
<td align="center"><img src="screenshots/03-new-found.png" width="200" alt="New complaint" /><br/><sub>New complaint</sub></td>
<td align="center"><img src="screenshots/04-detail-C39.png" width="200" alt="Emergency complaint" /><br/><sub>Emergency complaint</sub></td>
<td align="center"><img src="screenshots/06-quality-emergency.png" width="200" alt="Quality queue" /><br/><sub>Quality queue</sub></td>
</tr>
<tr>
<td align="center"><img src="screenshots/08-compensation.png" width="200" alt="Compensation" /><br/><sub>Compensation</sub></td>
<td align="center"><img src="screenshots/09-reports.png" width="200" alt="Reports" /><br/><sub>Reports</sub></td>
<td align="center"><img src="screenshots/10-lot.png" width="200" alt="Batch lookup" /><br/><sub>Batch lookup</sub></td>
<td align="center"><img src="screenshots/13-security-log.png" width="200" alt="Security log" /><br/><sub>Security log</sub></td>
</tr>
</table>

## Features

### Logging a complaint
- Search by the customer's phone number, order number or email. The Salla order fills in automatically.
- One complaint can cover several products. Each product gets its own issues and batch number.
- Attach photos, videos and voice notes from the phone.
- Complaints from a branch or another channel are logged without an order.

### Routing
- Each complaint is assigned to the quality team or the factory based on the issue type.
- The assigned manager gets an email with the complaint number.

### Emergencies
- Emergency complaints always go to the quality manager and are shown in red at the top of each screen.
- Collecting a product sample needs approval from two people. The approval record can't be edited.

### Compensation
- Each complaint records the compensation type, amount and a note.
- A list shows compensation that hasn't been paid yet.
- A cost report breaks compensation down by month, product and batch.

### Reports
- Complaint trends, and breakdowns by product, city and channel.
- Batch lookup: every complaint linked to one production batch.
- Response times per team.
- Excel export, with a choice of sheets.

### Other
- A ready WhatsApp message to the customer, with the product name and order number.
- The owner adds staff, changes roles and resets passwords. The last active person in a role can't be deactivated.
- Deleting or changing important data asks for confirmation first.
- Sign-ins are logged. An account is paused after repeated wrong passwords.
- Orders arrive from Salla through webhooks, and a nightly job pulls any that were missed.
- A health check reports the state of the Salla connection, the nightly job and storage use.
- Built for phones first. Dark mode.

## Tech

Next.js 16, React 19, TypeScript, Supabase (Postgres, Auth, Storage), Tailwind CSS 4, Vercel, PostHog (EU).

## Security

- Each store's data is separated with Postgres row-level security.
- Customer photos and videos are in private storage and open through links that expire.
- Salla access tokens are encrypted in the database.
- A content security policy stops other sites from embedding the app.

---

The source code is private. This repository holds screenshots and a short video. For a walkthrough or a demo for your store, message me on [LinkedIn](https://www.linkedin.com/in/mohammed-altounsi/).
