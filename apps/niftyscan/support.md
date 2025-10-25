---
layout: minimal
title: Privacy Policy
nav_exclude: true
search_exclude: true
hide_search_bar: true
---

# NiftyScan / Support

Welcome to the help hub for **NiftyScan**. This page answers common questions and shows quick fixes. If you’re stuck, email me anytime at **[niftyscan@hypothetical.ink](mailto:niftyscan@hypothetical.ink)**.

## Frequently Asked Questions

1. **What does NiftyScan do?**
    - Scans QR codes and barcodes, shows the raw data, and – for supported payment QR types – displays a simple, readable breakdown.
2. **What payment QR types are supported?**
    - **SGQR/PayNow, DuitNow, and UPI** (read-only parsing; no payments processed). Support for more RTP (real-time payments) QRs will be added in the future.
3. **Where is my data stored?**
    - **On your iPhone only.** No accounts, no server sync, no analytics, no tracking.
4. **What’s in Pro?**
    - **Unlimited history** (limited to most recent 10 scans in free), **App Lock** (Face ID / Touch ID), and **Pin** scans so they’re not removed during bulk clear. I will keep adding new Pro features in the future.
5. **How do I request a refund?**
    - Purchases are handled by Apple. Request refunds via Apple’s **[Report a Problem](https://support.apple.com/en-us/118223)** site using your Apple ID.

## Getting Started

1. **Open NiftyScan** and allow **Camera** access.
2. Point at a QR or barcode; scanning happens automatically.
3. For supported payment QRs, you'll see a **friendly breakdown** of fields.
4. Copy or share the result as needed.
5. Your scans are saved in **History** (on device).

**Tip:** For small or glossy codes, move the phone back a little and tilt to reduce glare.

## Payment QR Parsing

For supported codes, NiftyScan renders common fields in plain language, such as:

- Merchant / Payee name (when present)
- Account identifier (e.g., **VPA** for UPI)
- Amount / Currency (if encoded)
- Reference / Purpose / Notes (if present)
- Network / Scheme metadata

**Note:**

1. Not all issuers include every field. If data is missing, it likely isn’t in the QR.
2. **NiftyScan does not process payments.** It only reads the content of the code.

## History & Privacy

- **On-device storage:** All scans live locally on your iPhone.
- **Clear history:** History → **Clear History**; Settings → **Clear History** (irreversible).
- **Bulk clear respects pins (Pro):** Pinned scans stay when you bulk-clear.

We don’t collect personal data, analytics, or usage statistics. See our [Privacy Policy](privacy) for details.

## Pro Features

One-time purchase. No subscriptions. Buy once and use all current and future pro features forever.

- **Unlimited History:** Keep as many scans as you like.
- **App Lock (Face ID / Touch ID):** Require biometric unlock to open the app.
- **Pin Scans:** Mark important scans so they **survive bulk clear**.
- **More coming soon!**

### Buy / Restore

- Purchase from **Settings → Upgrade to Pro**.
- Restoring on a new device? Use the same Apple ID, then **Settings → Upgrade to Pro → Restore Purchases**.

## Troubleshooting

### Camera isn’t working / black view

- Go to iOS **Settings → Privacy & Security → Camera → NiftyScan** and allow access.
- Force-quit and reopen the app.

### Code won’t scan / too blurry

- Step back 10–20 cm; let the camera autofocus.
- Avoid glare; angle slightly.
- Ensure the full code fits within the frame.

### Payment QR shows raw data but no breakdown

- The code may be unsupported or missing required fields.
- Try another known SGQR/PayNow, DuitNow, or UPI code to compare.

### History disappeared

- History is local. If you cleared it (or reinstalled the app), it cannot be recovered.
- <!-- Update when iCloud sync and/or csv download is available. -->
- **Pins (Pro)** are preserved only during **bulk clear** — not across app delete/reinstall.

### Pro not recognised after reinstall

- Open **Settings → Upgrade to Pro → Restore Purchases** using the same Apple ID used to buy Pro or restore on a new device/after reinstall.
- Still stuck? [Email us](mailto:niftyscan@hypothetical.ink) with your **App Store receipt**.

## Purchases, Pricing & Refunds

- **Pricing:** Pro is a one-time purchase. Final local price is shown by Apple at checkout.
- **Refunds:** Managed by Apple via your Apple ID (**[Report a Problem](https://support.apple.com/en-us/118223)** site). We can’t issue or approve refunds directly.

## Compatibility & permissions

- **iPhone:** iOS **18** or later
- **Permissions:**
  - **Camera** (required for scanning)
  - **Photos** (optional: for upload)
- No background tracking, no analytics, no third-party ad frameworks.

## Accessibility

We’re improving support for assistive technologies. Today, NiftyScan uses standard iOS controls but some areas may not be fully optimised for **VoiceOver**, **Dynamic Type**, or **high-contrast** use. If you rely on these features and hit an issue, please email **[niftyscan@hypothetical.ink](mailto:niftyscan@hypothetical.ink)** with details so I can prioritise fixes.

## Contact me

Most issues are solved when we get the right details. When you write to **[niftyscan@hypothetical.ink](mailto:niftyscan@hypothetical.ink)**, please include:

- App version (Settings → About)
- iPhone model and iOS version
- Steps to reproduce (1-2-3)
- A sample code (text content or a redacted screenshot), if possible
- Whether the issue happens with **all** codes or specific ones

I am one person, with a day job. I will not be able to acknowledge or reply all mails.

## Legal

- [Terms of Use](terms)
- [Privacy Policy](privacy)
