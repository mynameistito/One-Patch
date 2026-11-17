# Changelog

All notable changes to DeadZone will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

## [1.1.1] - 2026-11-18

### Fixed
- Blocking and the floating shortcut stay active when the app is swiped away from recent apps.
- Android can restart an active blocking service after reclaiming its process, restoring manual pause state.
- Stopping from the app or notification clears restart intent. Android Force stop remains respected.

## [1.1.0] - 2026-11-18

### Added
- English interface, permission guidance, accessibility labels, and notifications.
- Chinese localization retained for Chinese-language devices.
- Blocking areas as thin as 1 pixel, with nearest-corner resize handles.
- Floating shortcut can tuck off-screen, leaving a 4dp edge to grab.

### Fixed
- Fullscreen editor accounts for camera cutouts and screen coordinates when loading and saving areas.
- Floating shortcut finishes docking when released partly off-screen and cannot disappear into a corner.
- Existing notification channels refresh their localized names.

### Release
- Fork releases require a dedicated signing key instead of falling back to debug signing.
- Accessibility remains optional. The exported Quick Toggle can trigger the saved gesture;
  leave Accessibility disabled if you do not need gesture replay.

## [1.0.0] - 2026-04-28

### Added
- Single rectangular dead zone with drag/resize directly on real fullscreen
- `TYPE_APPLICATION_OVERLAY` runtime overlay (12% blue tint + red border)
- Optional `TYPE_ACCESSIBILITY_OVERLAY` trusted-window mode (immune to Xiaomi one-handed transform)
- Foreground service with `specialUse` type (Android 14 compliant)
- Persistent notification with one-tap stop action
- Material You dynamic colors
- Xiaomi/HyperOS permission guide (background popup, autostart, battery)
- Fullscreen edit activity for direct on-screen rectangle drawing

### Security
- No `INTERNET` permission declared
- No third-party SDK / analytics / telemetry
- Accessibility service does not read screen content or listen to events
