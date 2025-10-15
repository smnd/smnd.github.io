---
layout: default
title: Privacy Policy
nav_exclude: true
published: false
---

# NiftyScan / Support

Welcome to the help hub for **NiftyScan**. This page answers common questions and shows quick fixes. If you’re stuck, email me anytime at **[niftyscan@hypothetical.ink](mailto:niftyscan@hypothetical.ink)**.

## Quick answers (FAQ)

1. **What does NiftyScan do?**  
    - Scans QR codes and barcodes, shows the raw data, and—for supported payment QR types—displays a simple, readable breakdown.
2. **What payment QR types are supported?**  
    - **SGQR/PayNow, DuitNow, and UPI** (read-only parsing; no payments processed).
3. **Where is my data stored?**  
    - **On your iPhone only.** No accounts, no server sync, no analytics, no tracking.
4. **What’s in Pro?**  
    - **Unlimited history**, **App Lock** (Face ID / Touch ID), and **Pin** scans so they’re not removed during bulk clear. I will keep adding new Pro features in the future.
5. **Refunds?**  
    - Purchases are handled by Apple. Request refunds via Apple’s **[Report a Problem](https://support.apple.com/en-us/118223)** site using your Apple ID.
    
## Getting started

1. **Open NiftyScan** and allow **Camera** access.
2. Point at a QR or barcode; scanning happens automatically.
3. For payment QR (SGQR/PayNow, DuitNow, UPI), you'll see a **friendly breakdown** of fields.
4. Copy or share the result as needed.
5. Your scans are saved in **History** (on device).
    
**Tip:** For small or glossy codes, move the phone back a little and tilt to reduce glare.

## Payment QR parsing (what you’ll see)

For supported codes, NiftyScan renders common fields in plain language, such as:
- Merchant / Payee name (when present)
- Account identifier (e.g., **VPA** for UPI)
- Amount / Currency (if encoded)
- Reference / Purpose / Notes (if present)
- Network / Scheme metadata
    
**Note:** 
1. Not all issuers include every field. If data is missing, it likely isn’t in the QR.
2. **NiftyScan does not process payments.** It only reads the content of the code.

## History & privacy

- **On-device storage:** All scans live locally on your iPhone.
- **Clear history:** History → **Clear History**; Settings → **Clear History** (irreversible).
- **Bulk clear respects pins (Pro):** Pinned scans stay when you bulk-clear.
    
We don’t collect personal data, analytics, or usage statistics. See our [Privacy Policy]({{site.baseurl}}/apps/niftyscan/privacy) for details.

## Pro features (one-time purchase)

- **Unlimited History:** Keep as many scans as you like.
- **App Lock (Face ID / Touch ID):** Require biometric unlock to open the app.
- **Pin Scans:** Mark important scans so they **survive bulk clear**.
- **More coming soon!**
    
**Buy / Restore**
- Purchase from **Settings → Go Pro**.
- Restoring on a new device? Use the same Apple ID, then **Settings → Restore Purchases**.

## Troubleshooting

**Camera isn’t working / black view**
- Go to iOS **Settings → Privacy & Security → Camera → NiftyScan** and allow access.
- Force-quit and reopen the app.

**Code won’t scan / too blurry**
- Step back 10–20 cm; let the camera autofocus.
- Avoid glare; angle slightly.
- Ensure the full code fits within the frame.

**Payment QR shows raw data but no breakdown**
- The code may be unsupported or missing required fields.
- Try another known SGQR/PayNow, DuitNow, or UPI code to compare.

**History disappeared**
- History is local. If you cleared it (or reinstalled the app), it cannot be recovered.
- **Pins (Pro)** are preserved only during **bulk clear** — not across delete/reinstall.

**Pro not recognized after reinstall**
- Open **Settings → Restore Purchases** using the same Apple ID used to buy Pro.
- Still stuck? [Email us](mailto:niftyscan@hypothetical.ink) with your **App Store receipt**.

## Purchases, pricing & refunds

- **Pricing:** Pro is a one-time purchase. Final local price is shown by Apple at checkout.
- **Refunds:** Managed by Apple via your Apple ID (**Report a Problem** site). We can’t issue or approve refunds directly.


## Compatibility & permissions

- **iPhone:** iOS **[17]** or later
- **Permissions:** 
    - **Camera** (required for scanning)
    - **Photos** (optional: for upload)
- No background tracking, no analytics, no third-party ad frameworks.

## Accessibility

We’re improving support for assistive technologies. Today, NiftyScan uses standard iOS controls but some areas may not be fully optimized for **VoiceOver**, **Dynamic Type**, or **high-contrast** use. If you rely on these features and hit an issue, please email **[niftyscan@hypothetical.ink](mailto:niftyscan@hypothetical.ink)** with details so I can prioritize fixes.

## Contact us
Most issues are solved within a couple of replies when we get the right details. When you write to **[niftyscan@hypothetical.ink](mailto:niftyscan@hypothetical.ink)**, please include:

- App version (Settings → About)
- iPhone model and iOS version
- Steps to reproduce (1-2-3)
- A sample code (text content or a redacted screenshot), if possible
- Whether the issue happens with **all** codes or specific ones
    
I will not be able to acknowledge or reply all mails.

## Legal

- **Terms of Use:** {{site.baseurl}}/apps/niftyscan/terms
- **Privacy Policy:** {{site.baseurl}}/apps/niftyscan/privacy

Last updated: 15 Oct 2025

<!-- INTERNAL TODO 
— Accessibility baseline checklist for next build 
- VoiceOver: Add accessibilityLabel to scan, copy, share, clear, pin, lock; hide live camera preview (isAccessibilityElement = false); announce detection (“Code detected”). 
- Focus: After successful scan, move VO focus to parsed result container; provide “Dismiss” button with a clear label. 
- Dynamic Type: Use preferredFont APIs in history and details; avoid fixed-height rows; verify no clipping at XL/XXL sizes. 
- Hit targets: Ensure all tappable areas are ≥ 44×44pt; add contentInsets where needed. 
- Contrast & color: Ensure 4.5:1 contrast for text/overlays; avoid text over the live camera feed. 
- Reduce Motion/Haptics: Respect system settings; disable custom animations/haptics when toggles are off. 
- QA pass: Test with VO on; test Zoom, Bold Text, Increase Contrast, Reduce Motion. 
-->
