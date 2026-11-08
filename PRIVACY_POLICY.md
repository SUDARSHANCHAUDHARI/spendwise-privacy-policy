# SpendWise — Privacy Policy

**Effective Date:** 2026-10-23
**Last Updated:** 2026-11-08
**Version:** 1.2.0

Published by **Sudarshan Tech Labs** | https://sudarshantechlabs.com | sudarshantechlabs@gmail.com

---

SpendWise is a personal expense tracker for Android. All financial data is stored only on your device in an encrypted database. The App has no account, no analytics and no purchases, and it never sends your data over the internet. Google Play lists a network permission because a Google library bundled in the App declares it; no SpendWise feature uses it.

---

## Data Stored on Your Device

| Data | Purpose | Storage |
|---|---|---|
| Transactions (amount, category, account, date, notes) | Core expense tracking | Room database encrypted with SQLCipher |
| Categories, accounts and monthly budgets | Organisation and budget tracking | Room database encrypted with SQLCipher |
| App preferences (notifications, biometric lock) | Personalisation and app lock | App's private storage |

---

## Exports

If you export your data as CSV, the file is created on your device and shared only with the app you choose.

---

## Data Sharing

We do not collect, sell or share your financial data. It never leaves your device unless you export it.

---

## Permissions

The App itself asks for two permissions:

| Permission | Why |
|---|---|
| `POST_NOTIFICATIONS` | Budget alerts, if you turn them on |
| `USE_BIOMETRIC` | Optional fingerprint/face unlock |

Biometric unlock is handled entirely by Android. The App is told only whether authentication succeeded — it never receives your fingerprint or face data, and Android does not make that data available to any app.

### Permissions added by Android libraries

The finished app carries eight more, declared by libraries rather than by the App's own code. They still appear in the permission list you see on the Play Store:

| Permission | Comes from | What it does |
|---|---|---|
| `INTERNET` | `com.google.android.datatransport:transport-backend-cct`, pulled in by Google's ML Kit text-recognition library | **No SpendWise feature uses the network.** The library that declares it is never invoked, so nothing is sent. See the note below |
| `ACCESS_NETWORK_STATE` | the same transport library | Lets a library check whether a network exists; grants no ability to use one |
| `USE_FINGERPRINT` | `androidx.biometric` | The older-Android counterpart of `USE_BIOMETRIC` |
| `WAKE_LOCK`, `RECEIVE_BOOT_COMPLETED`, `FOREGROUND_SERVICE`, `BIND_JOB_SERVICE` | WorkManager | How Android schedules and re-registers the budget-alert checks |
| `DUMP` | a build-time library | Diagnostic permission. Android grants it only to system apps, so it has no effect here |

### Why `INTERNET` is listed but unused

The App bundles Google's ML Kit text-recognition library, intended for scanning a receipt photo. That feature is **not reachable in this build**: its screen is never registered in the navigation graph, nothing navigates to it, and the App declares no camera or photo permission. ML Kit is therefore never invoked, no image is ever processed, and the transport library that would report ML Kit usage to Google never runs.

**The App has no camera access and no access to your photos.** Neither `CAMERA` nor any media permission appears in the finished app.

---

## Data Retention

| Data | Retention |
|---|---|
| All local app data | Until you delete it, clear app data, or uninstall the App |

---

## Your Controls

- **Delete a transaction:** swipe to delete in the App.
- **Delete all data:** uninstall the App, or go to Android Settings > Apps > SpendWise > Storage > Clear Data.

Because your data exists only on your device and we hold no copy, a data access or deletion request to us would return nothing — you already have the only copy.

---

## Children's Privacy

SpendWise is not directed at children under 13. We collect no personal information from anyone.

---

## Changes to This Policy

We will update the date above when this policy changes.

---

## Contact

- **Email:** sudarshantechlabs@gmail.com
- **Developer:** sunny.sudarshan@gmail.com
- **Website:** https://sudarshantechlabs.com

---

## Play Store Data Safety Summary

| Data type | Collected | Shared | Purpose |
|---|---|---|---|
| Financial info (transactions, budgets) | Local only, never collected | No | App functionality |
| Personal info | No | No | — |
| Photos | No — no camera or media permission | No | — |
| Crash logs | No | No | — |
| Device or other IDs | No | No | — |

Declare **"No data collected"** in the Play Console data safety form. The network permission is library-declared and unused, so there is no transfer to disclose.

---

## Recent Updates (Version 1.2.0 - November 8, 2026)

- **Replaced the template text with the policy from the app repository,** keeping its prose verbatim. It was already right about the thing easiest to get wrong here: Google Play lists a network permission because a bundled Google library declares it, and no SpendWise feature uses it.
- **Removed the boilerplate** claiming protection by "the browser, Firebase, Google, GitHub", and the scaffold location sections, for an app that requests no location.
- **Made the network-permission explanation specific.** `INTERNET` arrives with `com.google.android.datatransport:transport-backend-cct`, pulled in by Google's ML Kit text-recognition library. The receipt-scanning feature that would use ML Kit is unreachable in this build — its screen is never registered in the navigation graph and nothing navigates to it — so ML Kit is never invoked and nothing is sent.
- **Stated that the app has no camera and no photo access.** Neither `CAMERA` nor any media permission is in the finished build.
- **Stated that biometric unlock never exposes biometric data.** Android reports only success or failure and does not make fingerprint or face data available to any app.
- **Listed the eight library-merged permissions,** since the app declares two while the Play Store shows ten.
- **Added the scaffolding a published legal document needs** and this copy lacked: effective and updated dates, a version, data retention, and a Play data safety table.

---

## Recent Updates (Version 1.1.0 - May 17, 2026)

- **Aligned policy with the shared privacy-policy structure.**
- **Clarified local financial data, receipts, biometric lock, notifications, and no-cloud behavior.**

---

**This privacy policy complies with:**
- Google Play Store requirements
- GDPR (General Data Protection Regulation)
- CCPA (California Consumer Privacy Act)

**Last reviewed:** 2026-11-08

---

This is the published policy, served at https://sudarshanchaudhari.github.io/spendwise-privacy-policy/ from the `main` branch of this repository. `index.html` carries the same content for the web and must be updated alongside this file. The copy in the [SpendWise app repository](https://github.com/SUDARSHANCHAUDHARI/SpendWise/blob/main/PRIVACY_POLICY.md) is kept identical.
