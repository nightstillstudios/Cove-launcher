# Cove Launcher Privacy Policy

**Night Still Studios**
Effective date: July 26, 2026
Last updated: August 2, 2026

This policy replaces the previous version dated March 2026.

## 1. Introduction

Cove Launcher (the "App") is an Android home screen launcher developed by Night Still Studios ("we", "us"). This policy explains what information the App handles, what stays on your device, what leaves it, and the choices you have. By using the App, you agree to the practices described here.

Cove Launcher is built local-first: almost everything it does happens entirely on your device. The App has no accounts, no login, no advertising, and no cross-app tracking.

## 2. Our commitment

**We will never sell your data. We will never share your data with anyone for advertising, marketing, or profiling.** Information leaves your device only for the online features described below — content downloads, error reporting, product-improvement signals, and purchase processing.

## 3. Information we collect

### Error reports and product improvement

The App uses Google Firebase (Crashlytics, Analytics, and Performance Monitoring) for crash reports, performance measurements, and categorical feature-usage signals. This helps us find crashes, fix problems, and understand which features are useful. This data includes:

- Device model, manufacturer, and Android version
- App version
- Crash traces, with error messages stripped of any personal content (file paths, search text, and similar details are removed before anything is sent)
- Coarse, categorical usage signals (for example, that a feature was used — never what you typed, searched, or looked at)
- Pseudonymous app-instance, Firebase installation, and Crashlytics installation identifiers, plus approximate country derived by Firebase from the connection IP address

This data is not linked to your identity, but the identifiers are pseudonymous rather than identifier-free. Two independent controls in Settings → Security & Privacy are both on by default and can be turned off at any time:

- **Automatic Error Reports** controls Crashlytics crash, ANR, and non-fatal reports. Turning it off also deletes unsent crash reports.
- **Product Improvement** controls categorical Analytics events, adoption properties, and Performance traces. Turning it off also resets on-device Analytics identifiers and data.

Turning either control back on does not upload events from the period when it was off.

### Purchase information

If you buy a premium upgrade, the purchase is processed by Google Play and managed through RevenueCat, our billing provider. RevenueCat receives a randomly generated pseudonymous identifier for your installation, the product you purchased, and the Google Play purchase token needed to validate it. We never see your payment details, name, or email — payment is handled entirely by Google Play. There is no Cove account; purchases are tied to your Google Play account, which is also how they are restored on a new device.

### That's the complete list

Nothing else is collected. The App has no analytics beyond the diagnostics described above, no advertising SDKs, and no data brokers.

## 4. Information processed only on your device

The following features read information on your device to work, and that information **never leaves your device**:

- **Your installed apps.** The App reads the list of installed apps (names, icons, package identifiers) to show your app drawer, home screen, and search. The names of your apps are never transmitted.
- **App usage statistics.** If you grant Usage Access, the App reads Android's app-usage statistics to power usage-based features such as Suggested Apps. This is read from the system, processed locally, and never transmitted.
- **Notifications and media playback.** If you grant Notification Access, the App reads your notifications to show notification indicators and media playback controls (Now Playing). Notification content is held only in memory while the App runs — it is never written to storage, never transmitted, and is discarded when access is revoked.
- **Calendar events.** If you grant calendar permission, the App reads today's and tomorrow's events to show an upcoming-event glance next to the clock. Events are read live from your calendar and are not stored or transmitted.
- **Bluetooth connection status.** If you grant the Bluetooth permission, the App checks whether an audio device is currently connected so it can show a status indicator. It does not scan for devices and does not read device names or addresses.
- **Search activity.** Your searches inside the App, and which results you open, are stored only on your device to improve future result ranking. They are never transmitted (and are excluded from diagnostics).
- **Wallpaper processing.** Depth and visual wallpaper effects are computed on your device using Google ML Kit's on-device image processing. No images or processing results are transmitted.
- **Your customizations.** Hidden apps, folders, favorites, icon and label overrides, and all settings are stored locally.

## 5. Information we do not collect

- **Device location.** The App does not request Android location permission or use a location API. Firebase derives an approximate country from the connection IP address on its servers for enabled error-reporting and product-improvement services.
- **Contacts.** The App does not request or read your contacts.
- **Camera and microphone.** Never requested, never used.
- **Personal identity.** No name, email, phone number, or account of any kind.
- **Cloud backups of your data.** The App explicitly opts out of Android's cloud backup and device-transfer systems, so your launcher data never leaves your device even through backups.

## 6. Network connections the App makes

For transparency, this is the complete list of network connections:

1. **Wallpaper catalog.** When you browse built-in wallpapers, the App downloads the catalog and images from our hosting provider (Cloudflare). Cove adds no launcher content or app-specific identifier to the request; the host receives ordinary connection data such as an IP address.
2. **Fonts.** Some typefaces are fetched once from Google's font provider via Google Play services. Cove requests the font and sends no launcher content; the provider receives ordinary connection data such as an IP address.
3. **Error reports and product improvement.** Crash reports, categorical usage signals, and performance measurements go to Google Firebase while their respective controls are enabled (see Section 3).
4. **Purchases.** Purchase validation with Google Play and RevenueCat (see Section 3).

All connections use encrypted HTTPS; the App refuses unencrypted connections entirely.

## 7. Android permissions

| Permission | Purpose | Required? |
| --- | --- | --- |
| Query installed apps (QUERY_ALL_PACKAGES) | Show your apps in the drawer, home screen, and search — the core function of a launcher. Also used to detect installed icon packs. | Yes |
| Internet | Diagnostics, purchases, wallpaper catalog, fonts (Section 6) | Yes |
| Set wallpaper | Apply the wallpaper you choose | Yes |
| Vibrate | Haptic feedback for taps and gestures | Yes |
| Expand status bar | The "open notification panel / quick settings" gesture | Yes |
| Private Space support (ACCESS_HIDDEN_PROFILES) | Show Android 15+ Private Space apps, as every default launcher does | Yes |
| Request package uninstall | The "uninstall" shortcut in an app's long-press menu; Android shows its own confirmation | Yes |
| Read calendar | Upcoming-event glance next to the clock | No — optional, asked only when you enable the feature |
| Bluetooth connect | Connected-audio-device indicator | No — optional |

"Required" permissions are part of the App's core function and are granted at install; optional ones are requested only when you turn on the related feature, and the App works fine if you decline.

## 8. Special access

Some features use Android's special access screens rather than normal permissions. All are optional, and all are granted and revoked in Android's system settings:

- **Default launcher (Home role).** Makes Cove your home screen. You can switch back to any other launcher at any time.
- **Usage Access.** Powers usage-based features such as Suggested Apps. Processed entirely on-device (Section 4).
- **Notification Access.** Powers notification indicators and media controls. Processed entirely in memory (Section 4).
- **Accessibility service.** Used solely to perform system actions you trigger with gestures — locking the screen and opening the notification panel or quick settings. The service is configured so that it **cannot read screen content**, and it processes no accessibility events. It is a button-press bridge, nothing more.

## 9. Data storage, retention, and deletion

- All launcher data is stored locally in the App's private storage, isolated by Android from other apps.
- The App opts out of cloud backup and device-to-device transfer, so this data is never copied off your device.
- Uninstalling the App, or clearing its data in Android settings, permanently deletes all local data.
- Error reports and product-improvement data already sent to Firebase are retained according to Google's retention policies. They are not linked to your identity, but they carry pseudonymous installation identifiers.
- Purchase records are retained by Google Play and RevenueCat as required to keep your purchase valid.

## 10. Third-party services

These services process data on our behalf, only to operate the App:

- **Google Firebase (Crashlytics, Analytics, and Performance Monitoring)** — error reports, categorical product-usage signals, and performance measurements that are not linked to your identity. Governed by [Google's Privacy Policy](https://policies.google.com/privacy).
- **Google Play** — app distribution and payment processing. Governed by Google's terms and privacy policy.
- **RevenueCat** — purchase management, using a pseudonymous installation identifier. Governed by [RevenueCat's Privacy Policy](https://www.revenuecat.com/privacy).
- **Google ML Kit** — on-device image processing for wallpaper effects. Runs locally; no images are transmitted.
- **Cloudflare** — hosts our wallpaper catalog for download.

We do not share any data with any third party beyond this list, and none of these services are permitted to use your data for their own advertising on our behalf.

## 11. Data security

Local data is protected by Android's application sandboxing. All network traffic is encrypted in transit. No method of storage or transmission is perfectly secure, but the App's design minimizes risk in the simplest way possible: almost nothing ever leaves your device.

## 12. Children's privacy

The App is not directed at children under 13, and we do not knowingly collect personal information from children. If you believe a child has provided personal information to us, contact us at nightstillstudios@gmail.com and we will delete it.

## 13. Your choices and rights

- Turn off **Automatic Error Reports** or **Product Improvement**, independently, at any time in Settings → Security & Privacy. Both are on by default; turning them off also deletes unsent crash reports or resets on-device Analytics identifiers and data, respectively.
- Grant or revoke any permission or special access at any time in Android settings; the App degrades gracefully.
- Clear all local data via Android settings, or by uninstalling the App.
- Contact us about anything in this policy at the address below.

Depending on where you live, you may have additional rights under local data protection law. Because Cove has no user account and its telemetry is not linked to your identity, we may not be able to associate a server-held pseudonymous record with you. You can still delete local data and stop future optional telemetry with the controls above, and you are always welcome to write to us.

## 14. Changes to this policy

When the App gains features that change how data is handled, we will update this policy and revise the "Last updated" date. Continued use of the App after changes constitutes acceptance of the updated policy.

## 15. Contact

**Night Still Studios**
Email: nightstillstudios@gmail.com

I am a solo developer and I read every email personally.

## 16. Governing law

This Privacy Policy is governed by the laws of India.
