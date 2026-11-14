# Kasa Authenticator Privacy Policy

**Last updated:** November 14, 2026

Kasa Authenticator is an offline-first two-factor authentication (2FA) app for Android.

This Privacy Policy explains how Kasa Authenticator handles data. The app is designed to keep your authenticator data on your device and under your control.

## Summary

Kasa Authenticator:

- Does not require an account
- Does not use cloud sync
- Does not contain ads
- Does not use analytics
- Does not use tracking technologies
- Does not collect personal data
- Does not share user data with third parties
- Does not send your 2FA secrets or codes to any server
- Does not request the Android INTERNET permission

## Data Collection

Kasa Authenticator does not collect personal data for KASA-operated servers, analytics, advertising, or tracking. You can enter account labels and other information into the app; this information is processed and stored locally on your device, rather than collected by KASA.

KASA does not receive, sell, or share your locally stored:

- Name
- Email address
- Phone number
- Location
- Contacts
- Photos or videos
- Device identifiers for tracking
- App usage analytics
- Crash analytics
- Advertising identifiers
- 2FA secrets
- TOTP codes
- Backup passwords
- Master passwords
- Pattern unlock data

## Authenticator Data

When you add a 2FA account to Kasa Authenticator, the app may store information such as:

- Issuer or service name
- Account label
- TOTP secret
- Algorithm
- Number of digits
- Time period
- Optional note or local metadata

This data is stored locally on your device.

Kasa Authenticator does not upload this data to any KASA server, cloud service, analytics service, advertising network, or third party.

## Local Storage and Encryption

Kasa Authenticator stores authenticator data locally on your device.

Sensitive authenticator data is stored in encrypted form. The app is designed so that your 2FA data remains under your control on your own device.

## Internet Access

Kasa Authenticator does not request the Android INTERNET permission.

The app does not initiate internet transfers of authenticator data, usage data, analytics data, or tracking data. If you choose a folder or document supplied by another app or a cloud-backed Android document provider, that provider may handle or synchronize your selected encrypted backup file under its own terms. Kasa Authenticator does not control that provider or run its own cloud synchronization.

## Backup and Export

Kasa Authenticator supports manual and optional automatic encrypted backups. Backup files use password-based key derivation and authenticated encryption. You choose the backup password; its strength affects the protection of the file. A strong, unique password or passphrase is recommended but is not mandatory.

**Manual backups:** When you request a manual backup, Android's document picker lets you choose where to save the encrypted file. The manual backup password is used for that operation and is not stored by the app.

**Automatic backups:** Automatic Backup is optional and off by default. To enable it, you select a destination folder, grant access through Android's folder picker, set a backup password, and choose a daily, weekly, or monthly schedule. Android may delay scheduled work. The app creates encrypted backup files only in the folder you selected. It verifies new automatic backups and then removes older automatic backup copies in that folder when the configured retention limit is exceeded (default: three copies), while protecting the latest verified backup.

**Automatic backup password on your device:** To allow scheduled backups without asking for your password each time, the app stores the automatic backup password locally in encrypted form using an Android Keystore-protected key. This password is not uploaded to KASA. Turning Automatic Backup off does **not** erase the locally stored password; it remains until you replace it or remove the app's data. The app does not provide server-side password recovery.

**Your choice of storage:** The app does not upload backup files to KASA servers. You may select a local folder or a folder made available by an Android document provider, including a provider that synchronizes files to your own cloud account. If you select such a provider, its handling of the files is outside KASA's control. Backup files stored outside the app remain your responsibility, including their safe storage and deletion.

Keep the backup password and relevant account recovery methods safe. Without the correct backup password, an encrypted backup may not be recoverable. Unlocking the app with a fingerprint or pattern does not decrypt a backup file. The separate, optional quick backup open feature described below can open a backup file with a fingerprint on the same phone.

**Quick backup open with fingerprint (optional):** After a manual backup the app may ask whether this backup should open faster; the feature can also be turned on or off in Settings. While it is on, new manual and automatic backups made on this phone are prepared for it. For each prepared backup the app stores a local record in its private storage on this phone: the SHA-256 hash of the encrypted file (used to recognize the file by its content), whether the backup was manual or automatic, the creation time, the name of an Android Keystore key, and the file's decryption key wrapped (encrypted) with that Keystore key. The backup password and the unwrapped key are never written to the record. Nothing in the record is sent to KASA or any third party. The Keystore key can be used only after a new fingerprint check on this phone, every time; if the phone's fingerprints change, the key may become unusable and the backup password is used instead. Quick open works only on the phone where the record was made, and only when this phone has a valid quick-open record that matches the file's content. In every other case (on another phone, after reinstalling the app, for a file with no matching record, or when the fingerprint does not work) the backup password is needed; it always remains valid.

Records are matched to files by content, not by name or location: a copied, moved, or renamed file still matches on this phone as long as its content is identical to the recorded file, even if it came from another place. A file whose content differs does not match and needs the backup password. Deleting a backup file, or the automatic removal of old automatic backups, does not delete its record. Choosing "Delete saved quick open records" in Settings deletes only the quick-open records and their Keystore keys; backup files, the stored automatic backup password, and your accounts are not touched, and those backups open with their password again. Clearing the app's data or uninstalling the app deletes far more: the quick-open records and keys together with the stored automatic backup password and all other app data on this phone. Backup files saved outside the app are not removed by this.

**Automatic backups and quick open:** Automatic backups are prepared for quick open only while it is turned on. Preparing one needs no fingerprint, but opening it later always does. This does not change how the automatic backup password is stored (described above), and quick open does not make automatic backups more secure; it only makes opening them on this phone easier.

## Import

When you choose a backup file through Android's document picker, Kasa Authenticator reads and processes it locally on your device. The app does not upload imported backup data to KASA servers.

The encrypted file is checked for supported format and integrity, and the correct backup password is required (or, when this phone has a valid quick-open record that matches the selected backup file's content, a successful fingerprint check instead; see Backup and Export). An incorrect password, tampered or damaged file, or unsupported format is rejected. Import is designed not to silently overwrite existing authenticator accounts or partially replace the vault when validation fails.

After the correct backup password is entered, or the fingerprint check succeeds, the app imports the accounts directly: there is no separate preview or second confirmation step. When the import has finished, the app shows how many accounts were added and how many were skipped.

## Master Password, Biometric Unlock, and Pattern Unlock

Kasa Authenticator may use a local master password to protect access to the app.

Optional biometric unlock and pattern unlock features are local quick-unlock methods. App biometric unlock uses the Android system's biometric prompt.

The separate quick backup open feature (see Backup and Export) uses only the fingerprint sensor, through Android's fingerprint service, and opens a backup file only when this phone has a valid quick-open record that matches the selected file's content; the file's name or location does not decide this.

Kasa Authenticator does not collect or receive your biometric data. Biometric and fingerprint checks are handled by the Android system on your device.

Your master password, backup password, pattern data, and quick-open records are not sent to KASA or any third party.

## QR Code Scanning

Kasa Authenticator may use the camera to scan 2FA QR codes.

Camera access is used only for scanning QR codes when you choose to use this feature.

QR code contents are processed locally on your device.

Kasa Authenticator does not upload QR code contents or scanned secrets to any server.

## Screenshots and Clipboard

Screenshot and recent-app preview protection is enabled by default on sensitive app screens. If you choose, you can temporarily permit screenshots for 1–10 minutes; protection is restored after that interval or when the app goes into the background.

You can copy a generated TOTP code to the Android clipboard. Copied codes are marked as sensitive on Android 13 and later, and the app attempts to clear them automatically after a configurable 15, 30, or 60 seconds (30 seconds by default). Clipboard clearing is a best-effort protection: Android and other apps may control clipboard behavior, and a copied code may remain if the app process stops before its timer runs. Kasa Authenticator does not copy the underlying TOTP secret to the clipboard.

## Third-Party Services

Kasa Authenticator does not use third-party analytics, advertising SDKs, tracking SDKs, or cloud sync services.

The app may rely on standard Android system components, such as:

- Android Keystore
- Android BiometricPrompt (app biometric unlock)
- Android FingerprintManager (fingerprint-only quick backup open)
- Android camera APIs
- Android file picker / document picker

These are used locally as part of normal Android app functionality.

## Children

Kasa Authenticator is not designed for children.

The app is intended as a security and productivity tool for users who manage two-factor authentication accounts.

## Data Sharing

Kasa Authenticator does not share user data with third parties.

The app does not sell user data.

The app does not use user data for advertising or tracking.

## Data Deletion

Kasa Authenticator stores authenticator data locally. When you delete an account, the app provides a Trash feature with a default retention period of seven days, after which entries may be permanently removed according to the app's retention settings. Permanent deletion and clearing Trash should be treated as irreversible.

Android's automatic cloud backup and device-to-device app-data transfer are disabled for Kasa Authenticator. You can remove locally stored app data by uninstalling the app or clearing its storage through Android settings; doing so can remove stored credentials and local preferences, including the encrypted automatic backup password and any quick-open records and their Keystore keys.

Encrypted backup files saved outside the app, including those in folders you selected for manual or automatic backups, are not necessarily removed when the app is uninstalled or its storage is cleared. You are responsible for managing those files. Automatic Backup removes older automatic copies only within its selected folder and according to the configured retention limit.

## Security Limitations

Kasa Authenticator is designed to protect your authenticator data locally, but no app can guarantee complete protection in every possible situation.

For example, security may be affected if:

- Your device is compromised
- Your operating system is modified
- Malware has access to your device
- You share your secrets, backup files, or passwords with someone else
- You lose access to your master password or backup password

You should keep your device secure and store recovery codes for your online accounts in a safe place.

## Changes to This Privacy Policy

This Privacy Policy may be updated when Kasa Authenticator changes how it handles data.

If the app’s data practices change, this policy and the Google Play Data Safety information will be updated accordingly.

## Contact

If you have questions about this Privacy Policy, you can contact:

**Email:** kasa.passvault@gmail.com