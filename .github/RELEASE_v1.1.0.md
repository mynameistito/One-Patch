English interface and more flexible touch blocking.

- English is the default language; Chinese localization is retained.
- Resize blocking areas down to 1 pixel wide or high.
- Drag the floating shortcut partly off-screen and release to tuck it away, leaving a 4dp edge.
- Fullscreen editing uses screen coordinates and supports camera cutouts, fixing the offset between the editor and the saved blocking area.
- Notification text and accessibility descriptions are translated.

Download **one-patch-1.1.0.apk** below. **Display over other apps** permission is required.
Accessibility is optional and enables accessibility overlays and gesture replay.

This release uses the fork's dedicated signing certificate. It cannot update an upstream-signed
installation or the locally installed debug build in place. Uninstalling an old build removes its
local settings; the release package is `com.overbaker.deadzone`, while the local debug build uses
`com.overbaker.deadzone.debug` and can remain installed separately.

Known issue: another installed app can launch the exported Quick Toggle and replay your saved
gesture while blocking and Accessibility are enabled. Leave Accessibility disabled if you do not need it.
Samsung system-panel blocking and OEM one-handed-mode behavior are device dependent.

Checksums and the signing-certificate SHA-256 fingerprint are included in **SHA256SUMS** and
**SIGNING-CERTIFICATE.txt**. The APK was built locally; on-device testing used debug builds.
