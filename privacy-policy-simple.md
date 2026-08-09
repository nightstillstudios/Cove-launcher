# Cove Launcher — Privacy, in Plain Words

**Last updated: August 2, 2026**

This is the friendly version of our [Privacy Policy](https://nightstillstudios.github.io/Cove-launcher/privacy-policy). If anything here ever disagrees with the full policy, the full policy wins — but they say the same thing.

## The short version

Cove Launcher is made by one person, and it's built so that your stuff stays on your phone. There's no account, no login, no ads, and no cross-app tracking. **I will never sell your data or share it for advertising.**

## What actually leaves your phone

Cove sends two kinds of service data. It also makes ordinary requests to download optional wallpapers and fonts; those requests do not include your launcher content.

**1. Error reports and product-improvement signals.** Google Firebase can receive crash reports, performance measurements, and simple categories such as which feature was used. It says things like "the app crashed on a Pixel 8 running Android 16" — it never includes what you typed, searched, or looked at, or the names of your apps. Firebase uses pseudonymous installation identifiers and derives an approximate country from the connection IP address, but Cove does not link this data to your identity.

There are two independent controls in Settings → Security & Privacy. **Automatic Error Reports** controls crash and ANR reporting. **Product Improvement** controls feature-usage and performance signals. Both are on by default, and you can turn either one off at any time. Turning off Automatic Error Reports also deletes unsent crash reports; turning off Product Improvement resets on-device Analytics identifiers and data.

**2. Purchase info, if you buy premium.** Google Play handles the payment — I never see your card, name, or email. A billing service (RevenueCat) gets a random pseudonymous installation ID and "this installation bought premium" so the app knows to unlock it. If you get a new phone, Google Play restores your purchase. This is required for premium to work and is not controlled by the two optional Firebase switches.

That's it. Nothing else.

## What stays on your phone

Everything else the launcher does, happens entirely on your device:

- **Your app list** — needed to show your apps. The names of your apps are never sent anywhere.
- **Which apps you use most** — if you allow Usage Access, it's used to suggest apps to you. Never sent anywhere.
- **Your notifications and music** — if you allow Notification Access, the launcher shows notification dots and music controls. It only keeps this in memory while running; nothing is saved to storage or sent anywhere.
- **Your calendar** — if you allow it, the clock shows your next event. Read live, never stored, never sent.
- **Your searches in the launcher** — remembered on your phone only, so better results come up first next time.
- **Your setup** — hidden apps, folders, favorites, and settings all live on your phone.

Your launcher data is even excluded from Android's cloud backup — it genuinely never leaves the device.

## What the app never touches

- Your device location (Cove does not request location permission; enabled Firebase services derive an approximate country from the connection IP address)
- Your contacts
- Your camera or microphone
- Your name, email, or any account info (there are no accounts!)

## About the permissions you'll see

A launcher needs a few permissions just to be a home screen: seeing your installed apps, setting wallpapers, vibrating for haptics, and opening the notification panel when you swipe. A few optional ones (calendar, Bluetooth status, Usage Access, Notification Access) are only asked for when you turn on the feature that needs them — say no and everything else still works.

One that deserves a plain explanation: the **accessibility service**. Cove uses it for exactly one thing — performing actions you ask for with gestures, like locking the screen. It's set up so it *cannot* read what's on your screen. Android just requires the accessibility route for these actions.

## Deleting your data

Uninstall the app (or clear its data in Android settings) and all local launcher data is gone. Firebase and RevenueCat may retain data already sent under their retention rules, using pseudonymous identifiers rather than a Cove identity. You can stop future optional Firebase collection at any time with the two controls above.

## Questions?

Email me at **nightstillstudios@gmail.com**. I'm a solo developer and I read every email personally.
