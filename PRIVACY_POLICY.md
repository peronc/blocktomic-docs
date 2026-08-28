---
layout: default
title: Privacy Policy
---


# Privacy Policy for Blocktomic

**Last updated: August 23, 2026**

This privacy policy explains how the Blocktomic app ("the App") handles your data.

## 1. Data stored on your device

The App is **offline-first**: all your data is stored exclusively on your device and is never uploaded to our servers. This includes:

- workout plans and activities;
- completed sessions and history;
- progress, streaks and badges;
- your profile (name, photo, weight, height, birth date);
- settings and preferences.

The only exception is content you explicitly choose to share (see Section 4).

## 2. GPS location

GPS is used **only during active workouts** to measure distance and speed. The distance covered is saved to your local workout history on your device. The raw GPS stream is **not stored**, and your location data is **never transmitted** to us or to any third party.

You can disable GPS at any time; the App also works with manual distance entry.

## 3. Anonymous analytics and crash reporting (optional, with consent)

Keeping the App free and improving it requires anonymous statistics. We use Google Firebase:

- **Firebase Analytics** — anonymous usage events (workouts started, completed or created).
- **Firebase Crashlytics** — technical crash reports to fix bugs.

This data is **anonymous**: it contains no name, email, or other personal identifier. A random device identifier is generated on your device and is used only to keep data consistent. It cannot be used to identify you.

### Your consent

Nothing is collected until you explicitly consent. On first launch the App asks for your permission; you can change your choice at any time in **Settings → Privacy**. If you decline or later revoke consent, analytics and crash reporting are disabled.

## 4. Cloud Firestore (remote content, feature feedback & shared workouts)

### Remote content catalog

To keep the built-in workout and activity catalog up to date, the App can read public content collections from Google Cloud Firestore (`prebuilt_workouts`, `sports_catalog`). This is an **anonymous, read-only download of app content**: it happens without your analytics consent (it is app content, not data collection), no personal data is involved, and if you are offline the App simply uses its built-in copy.

### Feature feedback

The App includes a feedback area where you can vote on upcoming features and submit ideas. These actions are **user-initiated** and are sent to Google Cloud Firestore (via Firebase) **only if you have given your analytics consent**:

- feature votes (up/down), keyed by the anonymous device identifier;
- feature proposals (the text you write);
- custom activities you create (name, icon, category).

This data is anonymous and tied only to the random device identifier described above. Without consent, none of this data is sent: feature voting and proposals are disabled in the App, and custom activities remain stored locally.

### Shared workouts

When you share a workout while online, the App publishes its structure to Google Cloud Firestore (collection `shared_workouts`) so it can be reached through a short link. Please note:

- only the workout **structure** is uploaded (blocks, names, durations, distances, repetitions) — never profile data, history or GPS traces;
- the payload is stored **anonymously**, with no account and no link to you or to your device identifier;
- documents have **no expiration date**: anyone holding the short link can view that workout until it is removed.

If you are offline — or the publication fails — nothing is uploaded: the entire workout is encoded inside the link itself and stays between you and the recipient.

## 5. Advertising

The App may display rewarded video advertisements provided by Google AdMob. Watching an ad is **always opt-in**: it happens only when you explicitly tap the corresponding button in the App (Support section), in exchange for the Supporter badge. Advertisements are served by Google and are subject to Google's privacy policies.

## 6. Permissions

The App may request the following permissions, used only for the stated purpose:

- **Location**: to track distance during workouts with GPS;
- **Notifications**: to show the workout foreground notification and the optional weekly support reminder (local only);
- **Camera**: optional, to add a photo to your profile (stored locally).

## 7. Third-party services

- **Firebase** (Analytics, Crashlytics, Cloud Firestore) is a service by Google LLC. Data processed by Firebase is handled according to Google's Privacy Policy: <https://policies.google.com/privacy>.
- **Google AdMob** serves advertisements: <https://policies.google.com/privacy>.
- **PayPal** handles donations (Supporter feature): <https://www.paypal.com/privacy>.

## 8. Contact

If you have questions about this policy, contact: **blocktomic@gmail.com**.

---

© 2026 Blocktomic. All rights reserved.
