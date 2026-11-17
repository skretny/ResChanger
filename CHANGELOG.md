# Changelog

All notable user-facing changes to ResChanger are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-11-17

### Added

- Initial public release.
- Up to 9 display profiles with per-profile monitor, resolution, and refresh rate.
- Global hotkeys for showing the window, restoring initial modes, and applying profiles.
- In-app hotkey capture with conflict detection.
- Tray menu with profiles, restore, and exit actions.
- Restore of the initial display modes captured at startup.
- Autostart, start minimized, close to tray, notifications, language, theme, hotkeys, and reset.
- 11 interface languages.
- Light, dark, and system themes.
- Single-instance activation.

### Changed

- Disconnected monitors no longer silently retarget a profile to the primary display. The profile keeps its binding and shows a warning until the monitor returns.
- Refresh-rate lists now match the available display modes.
- The main window now fits the available screen work area on smaller displays and higher DPI scales.

### Fixed

- Display mode changes could fail when a refresh rate was available only at a lower color depth.
- The active-profile marker ignored the configured refresh rate.

[1.0.0]: ../../releases/tag/v1.0.0
