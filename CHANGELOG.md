# Changelog

All notable user-facing changes to ResChanger are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.3] - 2026-11-20

### Changed

- Removed legacy attribution and comparison text from the documentation.
- Updated application metadata and the tray tooltip to generic display-resolution wording.
- No functional changes.

## [1.0.2] - 2026-11-17

### Changed

- Switched the application runtime from .NET 9 to .NET Framework 4.8, which is included in Windows 10/11. The executable is now about 270 KB instead of about 68 MB.
- Enabled software rendering to remove GPU/D3D memory growth and keep background memory stable.
- Removed the portable/lite split and the .NET 9 Desktop Runtime requirement.
- Removed runtime extraction to `%TEMP%`.

### Fixed

- Background memory growth over time.
- Excessive download size and memory usage.

## [1.0.1] - 2026-11-17

### Changed

- Portable single-file build now extracts bundled runtime files on first launch. Download size stays the same, but background RAM usage is significantly lower.
- Added a lite framework-dependent build (`ResChanger-lite.exe`, about 0.5 MB) that requires the .NET 9 Desktop Runtime x64.
- Both builds are published in the same release with separate SHA-256 checksums.

### Fixed

- High background memory usage of the compressed portable build.

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

[1.0.3]: https://github.com/skretny/ResChanger/releases/tag/v1.0.3
[1.0.2]: https://github.com/skretny/ResChanger/releases/tag/v1.0.2
[1.0.1]: https://github.com/skretny/ResChanger/releases/tag/v1.0.1
[1.0.0]: https://github.com/skretny/ResChanger/releases/tag/v1.0.0
