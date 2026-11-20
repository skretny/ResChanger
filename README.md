# ResChanger

<p align="center">
  <img src="Assets/icon_1024.png" width="120" alt="ResChanger icon">
</p>

<p align="center">
  <b>Portable resolution switcher for CS2 and Deadlock players.</b><br>
  Fast Alt+Tab and clean multi-monitor behaviour at stretched or non-native resolutions.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/.NET%20Framework-4.8-512BD4" alt=".NET Framework 4.8">
  <img src="https://img.shields.io/badge/platform-Windows%2010%2F11%20x64-0078D4" alt="Windows 10/11 x64">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="MIT license">
  <img src="https://img.shields.io/github/v/release/skretny/ResChanger?display_name=tag" alt="Latest release">
</p>

ResChanger is a portable Windows utility that switches display resolution and refresh rate with global hotkeys. It is built with WPF / .NET Framework 4.8.

## Why ResChanger? Fast Alt+Tab in CS2 and Deadlock without display glitches

ResChanger was built for players who run **Counter-Strike 2** and **Deadlock** at a non-native or stretched resolution (4:3, 1440x1080, 1280x960, etc.) and are tired of the display problems that come with it.

### The problem

When a game runs at a resolution different from your desktop resolution, Alt+Tab and multi-monitor setups often misbehave:

- black bars or a black strip appear on the second monitor
- the in-game cursor is offset from the real mouse position
- Alt+Tab is slow, or the picture breaks after returning to the game
- the game does not stretch correctly after switching windows

### How ResChanger helps

Instead of letting the game change the display mode and fight with Windows, you switch the desktop resolution yourself with a global hotkey:

1. Press a hotkey to switch to your gaming resolution before launching the game.
2. Press another hotkey to return to your native resolution, so Alt+Tab, the second monitor, and your desktop behave normally.
3. Use `Ctrl+Alt+Shift+R` at any time to restore the display modes captured at startup.

This is a workaround for these display issues. The exact cause depends on your setup (GPU driver, Windows version, scaling settings, display mode in the game), so results can vary.

### Made for

- Counter-Strike 2 and Deadlock players using stretched or non-native resolutions
- Dual-monitor setups where the second monitor flickers, goes black, or shows black bars
- Anyone who wants a fast Alt+Tab and an instant resolution switch with one key press

### Highlights

- Up to 9 profiles with their own resolution, refresh rate, and target monitor
- Global hotkeys that work while the window is hidden
- Portable, about 270 KB, no installer needed
- Tray icon, autostart, 11 languages

## Download

Get the latest version from [Releases](https://github.com/skretny/ResChanger/releases).

1. Download `ResChanger.exe`.
2. Run the executable. No installer or separate .NET runtime download is required on Windows 10/11.
3. Verify the SHA-256 checksum from `ResChanger.exe.sha256` if needed.
4. Enable **Start with Windows** in Settings if needed.

The executable is about 270 KB and uses the built-in .NET Framework 4.8. Settings are stored per user in `%LOCALAPPDATA%\ResChanger\settings.json`.

The build is not code-signed, so Windows SmartScreen may show a warning on first launch.

## Hotkeys

| Action | Default combination |
|---|---|
| Show window | `Ctrl+Alt+R` |
| Restore initial resolution | `Ctrl+Alt+Shift+R` |
| Apply profile 1–9 | `Ctrl+Alt+1` … `Ctrl+Alt+9` |

All combinations can be changed in the interface. In the capture window, `Del` removes a hotkey; `Esc` cancels.

## Command line

```text
ResChanger.exe              normal launch
ResChanger.exe --minimized  start in the tray (used by autostart)
ResChanger.exe --show       force the window to show
```

## Configuration

```text
%LOCALAPPDATA%\ResChanger\settings.json
```

Unhandled errors are written to:

```text
%LOCALAPPDATA%\ResChanger\error.log
```

Use **Settings → Data → Open folder** to open the configuration directory.

## Troubleshooting

- **The image is lost after changing the mode.** Press `Ctrl+Alt+Shift+R` to restore the modes captured at startup. If that does not help, reboot into Safe Mode and change the resolution manually.
- **A hotkey is not registered.** Another application already uses the combination. Choose another one in Settings or in the profile row.
- **A profile says `Display not found.`** The target monitor is disconnected. Reconnect it or select another monitor in the profile.
- **The app is already running.** ResChanger is single-instance; the existing window is shown instead.

## Support

The **Support** button at the bottom left opens **Tribute (Telegram)** and **Donatex** links.

Report bugs and suggest features via [GitHub Issues](https://github.com/skretny/ResChanger/issues).

## License

MIT. Copyright (c) 2026 skretny. See [LICENSE](LICENSE).

See [CHANGELOG.md](CHANGELOG.md) for version history.
