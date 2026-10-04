# San Jose Prospecting PWA

An Android-first, installable web app that turns the verified 150-lead San Jose prospect package into a one-at-a-time outreach workflow.

## What it automates

- Ranks and queues the next best uncontacted lead.
- Prepares a personalized initial email using current offer settings.
- Pairs every lead with its exact private-preview PNG.
- Uses the Android share sheet to hand the message and graphic to Gmail or another email app when file sharing is supported.
- Opens a prefilled email as a fallback and separately downloads/copies the graphic when Android does not permit attachment handoff.
- Generates seven truthful response branches: interested, price, proof, revision, follow-up, not now, and do not contact.
- Calculates one follow-up due time after a lead is marked sent.
- Tracks sent, replied, interested, paid, not-now, and do-not-contact outcomes on the device.
- Opens a prospect-specific ChatGPT workspace prompt designed to preserve that lead's conversation under its ID.
- Exports a full JSON backup and a progress CSV; imports backups and updated prospect JSON.
- Works offline after assets have been loaded once.

The app does **not** silently send email. Android and Gmail require the user to choose the receiving app, review attachments, and tap Send. This prevents accidental bulk outreach.

## Install on Android

1. Open the deployed site in Chrome on Android.
2. Tap the download icon in the app header, or open Chrome's menu and select **Install app** / **Add to Home screen**.
3. Open **Settings** and confirm the sender, price, payment link, delivery time, and follow-up delay.
4. Start on **Queue**, open the next lead, and tap **Share email + graphic**.
5. After the email is actually sent, return to the app and tap **Sent** so the follow-up timer starts.

## Privacy and storage

- Lead status, activity, settings, and imported data stay in local browser storage.
- No analytics, tracking pixels, remote database, or secret API keys are used.
- Clearing browser data erases progress; use **Export full backup** first.
- Respect every opt-out immediately and never invent results or client claims.

## Validate

```bash
npm test
```

The application is a buildless static PWA. All deployable files are in `dist/`. The GitHub Pages workflow validates and deploys `dist/` from `main`.
