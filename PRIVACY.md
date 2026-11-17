# DeadZone — Privacy Policy

**Last updated**: 2026-11-18

## Summary in one sentence

**One Patch stores settings and gestures you explicitly record locally. No analytics or data transmission is implemented, and the app does not request internet permission.**

## What data does the app access?

| Data | Used? | Where it goes |
|---|---|---|
| Personal identifiers (name, email, phone) | ❌ Never requested | — |
| Location | ❌ Never requested | — |
| Contacts / SMS / Call logs | ❌ Never requested | — |
| Photos / Files / Media | ❌ Never requested | — |
| Microphone / Camera | ❌ Never requested | — |
| Touch coordinates inside the dead zone | ✅ Discarded immediately, never recorded | Black-holed — `onTouchEvent` returns `true` and the event is gone |
| Dead zone rectangle (x, y, width, height) | ✅ Stored locally on your device only | `SharedPreferences` in app's private sandbox |
| Recorded one-handed-mode gesture | ✅ Touch coordinates and timing, only during recording | Private SharedPreferences on your device |
| Crash reports / analytics | ❌ Not implemented | — |

## Permissions explained

| Permission | Why we need it |
|---|---|
| `SYSTEM_ALERT_WINDOW` | Draw the transparent overlay rectangle on top of other apps to absorb touches |
| `FOREGROUND_SERVICE` + `FOREGROUND_SERVICE_SPECIAL_USE` | Keep the overlay alive in the background under aggressive OEM battery policies (Xiaomi HyperOS / MIUI) |
| `POST_NOTIFICATIONS` (Android 13+) | Show the persistent notification with the "Stop blocking" quick action |
| `BIND_ACCESSIBILITY_SERVICE` *(optional, user-enabled)* | Create accessibility overlays and replay your recorded gesture when triggered. Window content retrieval is disabled and accessibility events are ignored. Positioning varies by device. The exported Quick Toggle can also trigger replay when launched by another app while blocking is active. |

## Network usage

The app does **not** declare `INTERNET` permission. No network call is possible.

## Third-party SDKs

**None.** Only Android Jetpack and Material Components — no analytics, no ads, no crash reporting, no telemetry.

## Children's privacy

The app collects no data. It is suitable for users of all ages.

## Open source

Source code is publicly available at [github.com/mynameistito/One-Patch](https://github.com/mynameistito/One-Patch). You can audit every line.

## Contact

Issues / questions → [github.com/mynameistito/One-Patch/issues](https://github.com/mynameistito/One-Patch/issues)
