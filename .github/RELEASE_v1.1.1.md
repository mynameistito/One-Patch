Touch blocking now keeps running when you close the app.

- Enable blocking, then press Home, switch apps, or swipe One Patch away from recent apps.
- The foreground service keeps the blocking area and floating shortcut active.
- Android can restore an active service after reclaiming its process, preserving manual pause state.
- Stop from the app or notification to end blocking. Android Force stop, Task Manager Stop, and reboot remain respected.
- On Samsung, set App info → Battery → Unrestricted if battery management interrupts the service.

Includes all v1.1.0 improvements: English UI, thin blocking strips, fullscreen alignment fixes, and the tucked floating shortcut.

Download **one-patch-1.1.1.apk**. It is signed with the same fork release certificate as v1.1.0
and can update that release in place. The locally installed debug build remains a separate package.
SHA-256 checksums and the signing certificate fingerprint are attached.

Known issue: the exported Quick Toggle can replay the saved gesture when another app launches it
while blocking and Accessibility are enabled. Accessibility is optional.
