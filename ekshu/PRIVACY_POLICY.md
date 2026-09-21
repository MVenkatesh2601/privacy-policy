# Ekshu Privacy Policy

**Effective Date:** September 21, 2026

---

## 1. Privacy Policy

Ekshu ("we", "us", or "our") operates Ekshu, a personal finance tracking application for Android. This Privacy Policy explains how Ekshu handles your information when you use the app.

Ekshu is designed with privacy in mind. Your financial data is processed and stored on your device. Ekshu does not operate servers that receive or store your financial information.

By using Ekshu, you agree to the practices described in this Privacy Policy.

---

## 2. Who We Are

Ekshu is developed and published by Ekshu. For privacy-related questions, you can contact us at:

- **Email:** ekshu.app.dev@gmail.com

---

## 3. Information We Store

Ekshu stores the following categories of information locally on your device:

**Financial information you enter or that is detected automatically:**
- Transactions (amounts, dates, merchant names, categories)
- Bank accounts and balances
- Credit card details (name, last four digits, limits, outstanding amounts)
- Bills and payment due dates
- Loans and EMI details
- Investments and contribution history
- User-defined tags and notes
- Merchant classification rules

**Information detected automatically (with your permission):**
- When you grant SMS permission or notification access, Ekshu can detect transaction information from incoming bank and financial SMS messages to automatically identify and record financial activity.

**Application settings:**
- Display name (optional, stored encrypted)
- App lock PIN (stored as an encrypted hash)
- Backup password (stored encrypted)
- Theme and display preferences

---

## 4. Automatic Transaction Detection

With your explicit permission, Ekshu can automatically detect and record transactions, bills, and credit card activity from incoming financial SMS messages without requiring manual entry.

Ekshu supports two complementary detection sources:
- **SMS permission (RECEIVE_SMS):** Ekshu receives incoming SMS messages from your bank and processes them to detect financial transactions.
- **Notification access:** Ekshu reads transaction alert notifications from your SMS app (for example, Google Messages or SMS Organizer) to detect financial activity.

You can enable either or both sources. Automatic tracking works when at least one supported source is enabled. Both sources use the same on-device processing pipeline, and duplicate detection prevents the same transaction from being recorded twice.

How this works:
- Only incoming financial SMS messages and notifications from trusted SMS applications are processed
- Non-financial messages such as OTPs, personal messages, and promotional texts are ignored
- All parsing and financial data extraction happens entirely on your device
- You can grant or revoke SMS permission and notification access at any time from your device settings
- Ekshu continues to work with manual entry and pasted SMS if you choose not to enable automatic detection

**Parsed transaction information may be stored locally on your device as part of your transaction records.**

**Ekshu does not transmit SMS content or notification text to Ekshu servers or third-party servers.**

---

## 5. Manual Transaction Entry and SMS Paste

You can add transactions to Ekshu manually or by pasting SMS text into the app. When you paste SMS text, it is processed on your device to extract transaction details.

If you paste SMS text, the resulting transaction record may retain the original text locally on your device for reference purposes.

Ekshu does not read your existing SMS inbox or message history. The SMS permission (RECEIVE_SMS) is used only to receive incoming SMS messages for automatic transaction detection. Ekshu does not request READ_SMS, which would be required to access stored messages.

---

## 6. How We Use Your Information

Ekshu uses your information solely to provide the app's features:

- **Transaction tracking** — recording and categorising your financial activity
- **Bill management** — tracking due dates and payment status
- **Loan monitoring** — tracking EMI payments and loan balances
- **Credit card management** — tracking statements and outstanding amounts
- **Financial insights** — generating spending summaries and reports (computed entirely on your device)

Ekshu does not use your financial information for advertising, marketing, profiling, or any purpose other than providing the app's features to you.

---

## 7. Local Storage and Security

All of your financial data is stored in a local database on your device. Ekshu does not require you to create an account and does not sync your financial data to any cloud service.

Security measures include:
- **Encrypted sensitive settings** — your display name, backup password, and app lock PIN are encrypted using AES-256-GCM encryption with keys stored in Android Keystore
- **Optional app lock** — you can protect access to Ekshu with biometric authentication (fingerprint or face) or a 4-digit PIN
- **Screenshot protection** — an optional setting to prevent screen capture of your financial data
- **Balance hiding** — an option to conceal account balances in the app interface
- **Android cloud backup disabled** — your financial data is not automatically copied to Google's cloud backup servers

No security system can provide absolute protection. While we design Ekshu to protect your data through local storage and encryption, we cannot guarantee that your data will never be accessed by unauthorised parties.

---

## 8. Backup and Restore

Ekshu lets you create encrypted backups of your data at any time. Backups include all locally stored information, which may include the original notification/SMS text associated with your transactions and bills.

Key details about backups:
- **Encrypted with your password** — backups are encrypted using industry-standard AES-256-GCM encryption before being saved to your device
- **Stored locally on your device** — you choose where to save backup files (such as your Downloads folder)
- **Ekshu does not upload backups** — backup files are never sent to Ekshu servers or any cloud service by the app
- **Auto-backup** — Ekshu can create daily encrypted backups on your device. This can be turned off at any time in Settings. Older auto-backups are deleted automatically based on the retention period you choose.
- **Restoring requires your backup password** — if you lose your password, your encrypted backups cannot be recovered. Ekshu does not have access to your backup password and cannot decrypt your backups without it.
- **Sharing and exporting is controlled by you** — if you choose to share or move a backup file, that action is performed entirely by you outside of Ekshu.

---

## 9. Crash Reporting and Analytics

Ekshu uses Google Firebase services to improve the app's reliability and understand how it is used. These services are provided by Google.

### Crash Reporting (Firebase Crashlytics)

When the app encounters an error or crash, diagnostic information may be sent to Firebase Crashlytics. This includes:
- Device type, operating system version, and app version
- Crash stack traces and error details
- Normalised diagnostic templates for parser diagnostics

**Parser diagnostic templates** are generated by replacing specific financial values in notification text with generic placeholders. For example, monetary amounts, account numbers, bank names, dates, phone numbers, email addresses, and web addresses are replaced with placeholders such as `{AMOUNT}`, `{ACCOUNT}`, `{BANK}`, `{DATE}`, `{PHONE}`, `{EMAIL}`, and `{URL}`.

These normalised templates may retain generic words describing the type of transaction context (such as "debited", "credited", "payment", "purchase", or "transfer"), but they do not contain specific financial values, account numbers, or bank names.

**The original notification/SMS text and specific financial values are never included in crash or diagnostic data transmitted to Firebase.**

### Usage Analytics (Firebase Analytics)

Ekshu uses Firebase Analytics to understand how the app is used. Usage events such as parser success, parser errors, and feature interactions may be transmitted to Google Firebase. These events do not contain financial details, transaction amounts, or message content.

### Remote Configuration (Firebase Remote Config)

Ekshu uses Firebase Remote Config to receive configuration updates such as parsing rules and feature flags. This service does not transmit personal or financial data.

Google's privacy practices are described at: https://policies.google.com/privacy

---

## 10. Third-Party Services

Ekshu integrates with the following Google Firebase services:

| Service | Purpose |
|---------|---------|
| Firebase Analytics | Understanding how the app is used to improve it |
| Firebase Crashlytics | Identifying and fixing bugs and crashes |
| Firebase Remote Config | Updating parser rules and feature settings without requiring a new app release |

These services are operated by Google. Google's privacy practices are described at: https://policies.google.com/privacy

Ekshu does not use any other third-party services that process your data. Ekshu does not use advertising SDKs, social media SDKs, or any other third-party service that accesses your financial information.

---

## 11. Data Sharing

**Ekshu does not sell, rent, or trade your financial data.**

Financial data and original notification/SMS text are not transmitted by Ekshu to third-party servers.

Limited crash, diagnostic, analytics, and configuration data is transmitted to Google Firebase as described in this policy. This data does not contain your financial information, transaction details, or original notification/SMS text.

If you choose to create and share a backup file, that sharing is performed entirely by you and is outside Ekshu's control.

---

## 12. Data Retention and Deletion

**Local financial data:** Retained on your device as long as you use the app. This includes transactions, accounts, bills, loans, credit card data, investments, and any locally stored notification/SMS text.

**User-created backups:** Retained as long as you keep them on your device. Auto-backup retention is configurable (3, 7, 30 days, or unlimited). Ekshu does not store your backups on any server.

**Firebase analytics and crash data:** Retained according to Google's standard retention policies. Ekshu does not control Google's data retention for Firebase services.

**How to delete your data:**
- Delete individual records (transactions, accounts, bills, loans) from within the app
- Clear all app data through your device's Android Settings, or uninstall Ekshu to remove all local data
- Delete backup files manually from your device's file storage

Uninstalling Ekshu removes all local data from your device. Backup files you created remain wherever you stored them.

---

## 13. Your Choices and Controls

You have the following choices when using Ekshu:

- **SMS permission** — grant or revoke SMS permission at any time. When granted, Ekshu receives incoming SMS messages for automatic transaction detection.
- **Notification access** — grant or revoke notification access at any time. When granted, Ekshu reads transaction notifications from your SMS app for automatic detection.
- Automatic tracking works when at least one of these sources is enabled. Ekshu continues to work with manual entry and pasted SMS if neither is enabled.
- **App lock** — enable or disable biometric/PIN protection in Settings
- **Screenshot protection** — enable or disable screen capture prevention in Settings
- **Balance hiding** — hide or show account balances in the app interface
- **Auto-backup** — enable, disable, or configure the retention period for automatic backups
- **Backup password** — change your backup password at any time in Settings
- **Data deletion** — delete individual records or clear all data as described above
- **Theme** — choose between light, dark, or system default themes

---

## 14. Children's Privacy

Ekshu is not directed to children under the age of 13. We do not knowingly collect personal information from children under 13. If you are a parent or guardian and believe your child has provided personal information through Ekshu, please contact us at ekshu.app.dev@gmail.com.

---

## 15. Changes to This Privacy Policy

We may update this Privacy Policy from time to time as the app evolves. The current version is always available in the app under Settings > About Ekshu > Privacy Policy. The effective date at the top of this policy indicates when it was last updated.

Continued use of Ekshu after changes take effect constitutes acceptance of the updated policy.

---

## 16. Contact Us

If you have questions about this Privacy Policy or your data, please contact us at:

- **Email:** ekshu.app.dev@gmail.com
