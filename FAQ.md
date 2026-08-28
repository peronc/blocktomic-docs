---
permalink: /FAQ.md
---


# Blocktomic — FAQ

> Frequently asked questions about Blocktomic.

---

## General

### What is Blocktomic?
Blocktomic is a Tabata, HIIT, and interval training timer for Android. It works fully offline, requires no account, and supports GPS tracking for running and cycling intervals.

### Is Blocktomic free?
Yes. Blocktomic is completely free. There is an optional Supporter program where you can watch a rewarded ad or make a PayPal donation to support development — but all features are available without paying.

### Do I need an account?
No. Blocktomic requires **no account, no registration, no email**. Download and start training.

### Does Blocktomic work offline?
Yes. 100% offline. Your data stays on your device. Internet is only needed for optional features: rewarded ads (Supporter badge) and anonymous analytics (if you opt in).

### Is Blocktomic available on iOS?
Not yet. Blocktomic is currently Android-only. iOS support is planned for a future release.

### What languages are supported?
English, Italian, Spanish, French, German, Portuguese, Japanese, Korean, Chinese, and Hindi. The app follows your system language by default, but you can change it in Settings.

---

## Privacy & Data

### Where is my data stored?
All your workout data, GPS tracks, profile information, and settings are stored **only on your device** (using Hive CE local database).

### Is my GPS data uploaded?
**No.** GPS data is used to track distance during workouts and is saved locally. It is never uploaded, shared, or sent to any server.

### Does Blocktomic collect personal data?
Blocktomic collects **nothing by default**. If you **opt in**, anonymous usage data and crash reports are sent via Firebase Analytics and Crashlytics. This is off by default and can be toggled in Settings > Privacy.

### Does Blocktomic share data with third parties?
Only these services are used:
- **Firebase** (Analytics + Crashlytics): only if you opt in, anonymous only.
- **Cloud Firestore**: stores feature votes/proposals and — when you choose to share a workout online — the anonymous workout payload behind the short link. No personal data is ever included.
- **AdMob** (rewarded ads): only when you choose to watch an ad for the Supporter badge.
- **PayPal.Me**: only when you choose to donate (external link).

### Why does Blocktomic need location permission?
Only for **GPS distance tracking** during workouts with distance-based intervals (running, cycling). You can decline location permission and enter distance manually instead.

### Why does Blocktomic need notification permission?
For two purposes:
1. **Weekly Supporter reminder**: optional notification every Monday at 10 AM (if your Supporter badge is expired).
2. **Foreground service notification**: keeps GPS active when the app is in background during a distance workout.

---

## Workouts

### How do I create a custom workout?
Go to Workouts > My Workouts, tap the + button. Add blocks (intervals) with the activity, duration, type, and rest. Reorder blocks by dragging. Save.

### What block types are available?
- **Time**: countdown timer (e.g., 20s work).
- **Distance**: GPS or manual distance tracking (e.g., 400m run).
- **Reps**: sets and repetitions for gym exercises.
- **Open-ended**: stopwatch-style, complete when you're ready.

### What activities are available?
Over 100 activities across 6 families: Endurance, HIIT, Gym, Calisthenics, Flexibility, and Other. Includes running, cycling, bench press, squats, pull-ups, burpees, stretching, and more.

### Can I use Blocktomic for gym workouts?
Yes. Create reps-based blocks with target weight, sets, and rest between sets. Track your progress for each exercise.

### Can I use Blocktomic for running?
Yes. Set distance-based blocks, enable GPS, and track each interval's distance automatically. The timer shows a progress bar and speed readout.

### How many rounds can I set?
You can set any number of rounds from 1 to 999.

### Can I reorder blocks?
Yes. Drag the handle (≡) on any block in the editor to reorder.

### How do I share a workout?
Tap the share icon on any workout card or preview. Send the **link** with any app, or let a friend scan the **QR code** with their camera. Online, a short anonymous link is generated; fully offline, the entire workout is encoded inside the link itself. The recipient sees a preview and imports a copy into their library.

### Why do pre-built workouts have two names?
Each pre-built workout has a classic name (*Classic Tabata*) and a catchy one (*Phoenix Protocol*). Cards show the catchy title by default — turn it off in Settings → Fun workout names (or from the last onboarding page) if you prefer plain titles.

### Why did some interval names change when I switched languages?
Default block names (Warm-up, Rest, "Activity 1", sport names) are auto-generated and follow your current app language. Names you typed yourself never change.

---

## Timer

### Can I pause a workout?
Yes. Tap the pause button during any block. Tap play to resume.

### Can I skip rest?
Yes. During a rest block, tap **Skip Rest** to move to the next block immediately.

### Can I skip a work block too?
Yes. During a work block, tap **Skip**: you move on right away, and the partial time or distance you already completed is still recorded in the session.

### What happens if I stop a workout early?
The session is saved to History with all completed blocks (and any partial work-block data). Your streak and statistics are updated with partial progress.

### Does the timer work in background?
Yes. A foreground service keeps the workout running when you switch apps or lock the screen: beeps keep sounding and the notification shows that the session is active. GPS tracking continues as well while the workout runs.

### Can I change the start delay?
Yes. Settings > Start Delay (0 to 15 seconds). This is the countdown before your workout begins.

### Can I turn off beeps or vibration?
Yes. Settings > Audio (sounds/beeps) and Settings > Vibration. Toggle each on or off.

---

## GPS

### How accurate is the GPS tracking?
Blocktomic uses high-accuracy location (`LocationAccuracy.best`). Accuracy depends on your device. Positions with accuracy worse than 50m are filtered out.

### Can I use the app without GPS?
Yes. For distance-based blocks, you can enter distance manually by tapping the distance readout.

### Does GPS drain my battery?
GPS is only active during distance-based blocks. It's turned off during rest periods and non-distance blocks. Typical GPS battery usage is similar to other fitness tracking apps.

### Is GPS used in the background?
Yes — a persistent notification keeps the GPS service alive so distance is tracked even if you switch apps or lock the screen.

---

## Progress & Badges

### How are streaks calculated?
A streak counts consecutive calendar days with at least one completed workout. The streak resets if you skip a day.

### How do I unlock badges?
Badges are checked automatically after each workout. When you unlock one, an animation plays on the completion screen.

### What happens if I clear app data?
All progress, history, settings, and profile data are lost. This cannot be undone. Consider this before clearing data.

### Can I export my history?
Not yet. This is a planned feature for a future release.

---

## Support

### What is the Supporter badge?
A visible badge that shows you support Blocktomic's development. It appears in the Progress tab and on your profile.

### How do I become a Supporter?
Two ways:
1. **Watch a rewarded ad** (Supporter for 15 days or 30 workouts).
2. **Make a PayPal donation** (Supporter for 30 days).

### How long does the Supporter badge last?
- After watching an ad: **15 days** or **30 workouts**, whichever comes first.
- After a donation: **30 days** (fixed).

### Can I get a refund for my donation?
Donations are voluntary support and are non-refundable. If you have a specific issue, contact us at blocktomic@gmail.com.

### Will there be subscriptions?
There are no current plans for mandatory subscriptions. Optional subscription tiers may be considered in the future to support ongoing development, but the free version will always remain functional.

---

## Technical

### What is the minimum Android version?
Blocktomic requires Android 5.0 (API 21) or higher.

### How do I update Blocktomic?
Updates are distributed through the Google Play Store. Enable auto-updates in the Play Store for seamless upgrades.

### How do I report a bug?
Email us at blocktomic@gmail.com with a description of the bug, your device model, and Android version. If possible, include steps to reproduce.

### How do I suggest a feature?
Open the Feedback & Ideas screen in the Support tab. Vote on existing ideas or submit a new one. You can also email us.

---

## Contact

- **Email**: blocktomic@gmail.com
- **Developer**: Carlo Peron
- **Documentation**: https://peronc.github.io/blocktomic-docs
- **Privacy Policy**: https://peronc.github.io/blocktomic-docs/PRIVACY_POLICY.md