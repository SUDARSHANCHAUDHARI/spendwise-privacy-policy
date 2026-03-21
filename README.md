# SpendWise — Privacy Policy

**Effective Date:** 2026-03-21
**Last Updated:** 2026-03-21
**Version:** 1.0.0

Published by **Sudarshan Tech Labs** | https://sudarshantechlabs.com | sudarshantechlabs@gmail.com

---

SpendWise is a personal expense tracking app for Android. It helps you log transactions, set budgets, scan receipts with OCR, and analyse your spending through charts. All financial data is stored exclusively on your device in an AES-256 encrypted database. Sudarshan Tech Labs does not collect or transmit your financial data.

---

## Data Collection

### Data Stored Locally on Your Device

| Data | Purpose | Storage |
|---|---|---|
| Expense transactions (amount, category, date, notes) | Core expense tracking | Room database (SQLCipher AES-256 encrypted) |
| Budget limits per category | Budget tracking | Room database (SQLCipher AES-256 encrypted) |
| Transaction categories and tags | Organisation | Room database (SQLCipher AES-256 encrypted) |
| Receipt photos | OCR scanning and record keeping | App private storage |
| App preferences and security settings | Personalisation | EncryptedSharedPreferences |
| PIN configuration (if set) | App lock | EncryptedSharedPreferences |
| Biometric auth preference | App lock | EncryptedSharedPreferences |

No financial data is transmitted to Sudarshan Tech Labs or any external server.

### OCR Receipt Scanning

When you scan a receipt, SpendWise uses Google ML Kit Text Recognition to extract text. ML Kit processes the image entirely on your device — no image or text is sent to Google or any server.

---

## How We Use Your Data

| Purpose | Data Used |
|---|---|
| Log and display expense transactions | Local encrypted transactions |
| Track budgets and spending limits | Local budget data |
| Scan receipts for automatic amount entry | On-device OCR (ML Kit) |
| Display spending charts and trends | Local transaction history |
| Export transaction history to CSV | Local data (on-device only) |
| Send bill reminder notifications | Local WorkManager schedules |
| Lock the App with biometric or PIN | Android Biometric API / local PIN hash |

---

## Data Storage and Security

- **Database:** AES-256 encrypted via SQLCipher — your financial data is encrypted at rest
- **Preferences:** AES-256 encrypted via Android Security Crypto (EncryptedSharedPreferences)
- **Receipt photos:** Stored in the App's private directory, inaccessible to other apps
- **Biometric:** Managed entirely by Android OS — Sudarshan Tech Labs never accesses biometric data
- **No cloud storage:** Sudarshan Tech Labs operates no backend server
- **Android sandbox:** Additional protection from Android's application isolation
- **CSV exports:** Generated on-device and shared via Android's sharing system at your request

## Data Retention

| Data | Retention |
|---|---|
| All local financial data | Until you delete it or uninstall the App |
| Receipt photos | Until you delete them or uninstall the App |

---

## Data Sharing

We do not sell or share your financial data. SpendWise operates entirely offline. The only external service used is:

- **Google ML Kit Text Recognition** (on-device OCR — no data sent to Google)

---

## Permissions Explained

| Permission | Why It Is Needed |
|---|---|
| `CAMERA` | Capture receipt photos for OCR scanning |
| `READ_EXTERNAL_STORAGE` (Android 12 and below) | Access files on older Android versions |
| `WRITE_EXTERNAL_STORAGE` (Android 9 and below) | Save exported CSV files on older Android |
| `USE_BIOMETRIC` | Enable fingerprint or face unlock to protect financial data |
| `POST_NOTIFICATIONS` | Send bill reminder notifications |

---

## Your Rights and Controls

- **Delete individual transactions:** Use the delete function within the App
- **Delete all data:** Uninstall or go to Android Settings > Apps > SpendWise > Storage > Clear Data
- **Export your data:** Use the CSV export feature in App Settings
- **Change or remove PIN/biometric lock:** Go to App Settings > Security

---

## Children's Privacy

SpendWise is not directed at children under 13. We do not collect any personal information.

---

## Changes to This Policy

We may update this Privacy Policy from time to time. We will notify you of significant changes via:

- In-app notification
- Updated policy date on this page

Continued use of SpendWise after changes become effective constitutes your acceptance of the updated policy.

---

## Contact Us

For privacy questions, data access requests, or account deletion:

- **Email:** sudarshantechlabs@gmail.com
- **Developer:** sunny.sudarshan@gmail.com
- **Website:** https://sudarshantechlabs.com
- **Response Time:** Within 48 hours

---

## Play Store Data Safety Summary

| Data type | Collected | Shared | Purpose |
|---|---|---|---|
| Financial transactions | Local only (AES-256 encrypted) | No | App functionality |
| Receipt photos | Local only | No | OCR scanning |
| Budget data | Local only (AES-256 encrypted) | No | Budget tracking |

---

---

**This privacy policy complies with:**
- Google Play Store requirements
- GDPR (General Data Protection Regulation)
- CCPA (California Consumer Privacy Act)

**Last reviewed:** 2026-03-21
