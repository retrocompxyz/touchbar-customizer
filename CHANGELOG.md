# Changelog

All notable changes to the TouchBar Customizer project.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [0.18.0] — 2026-10-02

### Added
- Bilingual user interface: **Polish** and **English**, switcher in
  Settings → Language (System / Polish / English). Changing the language
  requires a restart.

### Changed
- Language is stored in `config.json` (`settings.language`).

## [0.17.2] — 2026-10-02

### Fixed
- Discord mute/deafen icons could desynchronise; the state is now read with
  a fresh accessibility scan on every poll.

## [0.17.1] — 2026-10-02

### Fixed
- Discord state reader now re-walks the accessibility tree each time; a cached
  element kept stale attributes and never updated.

## [0.17.0] — 2026-10-02

### Added
- Real Discord mute/deafen state on the Touch Bar, read from Discord's
  accessibility tree (button `redGlow` class) instead of guessing locally.
- New state sources: `discordMute`, `discordDeafen`.

## [0.16.1] — 2026-10-02

### Fixed
- Menu commands now work for applications with lazily-built menus
  (e.g. CorelDRAW): each menu level is opened before the target item is clicked.

## [0.16.0] — 2026-10-02

### Added
- CorelDRAW **Object** menu commands: **Order**, **Group** and **Align** —
  both in the popular-shortcuts catalog and as ready buttons.
- Menu-command support in the shortcuts catalog (`menuPath`).
- Seed configuration group "Object" for CorelDRAW.

## [0.15.1] — 2026-10-02

### Fixed
- Verified Apple Notes / Terminal / VS Code shortcuts against the live menus;
  Apple Notes delete is a plain Delete.

## [0.15.0] — 2026-10-02

### Added
- Popular shortcuts for **VS Code**, **Terminal** and **Apple Notes**, plus
  starter sets for **Photoshop** and **CorelDRAW**.
- Apple Notes and Terminal added to the curated apps list.

## [0.14.2] — 2026-10-02

### Fixed
- Icons now scale up to fill the button, so group and app icons match the
  Dock icon size.

## [0.14.1] — 2026-10-02

### Changed
- Unified icon size (28 pt) for all icon-only buttons and status widgets.

## [0.14.0] — 2026-10-02

### Added
- **AirDrop** widget.

### Changed
- Flat status widgets (battery, Wi-Fi, CPU, now playing) without a bezel.
- Vertical battery icon with the percentage shown as plain text.

## [0.13.0] — 2026-10-02

### Added
- **Dock** widget: running applications, with an optional regex filter.

## [0.12.0] — 2026-10-02

### Added
- Status widgets: **Now Playing**, **Battery**, **Wi-Fi** and **CPU**.

## Early development — 0.1.0 – 0.11.2 (2026-09-29 – 2026-10-02)

The initial series of releases built the application from the ground up.
Highlights across these versions:

### Added
- Core menu bar app with **per-application Touch Bar profiles**, JSON
  configuration and hot-reload.
- Actions: keyboard shortcut, system key, shell script, AppleScript, open URL,
  open app, menu command, shortcut-in-app, beep and quit.
- GUI editor (AppKit) with **Settings**, **Apps** and **Profiles** tabs.
- Drag & drop ordering with **Left / Center / Right** zones, plus spacers and
  separators.
- **Groups** with bar-swap navigation.
- **Icon picker**: SF Symbols, application icons and custom image files;
  icon suggestions; Popular / Apps / All modes.
- **"From app menu"** command picker (menu scanning) and the
  **"Popular shortcuts"** catalog.
- **Sliders** panel (brightness, volume, keyboard illumination) and a mute
  control reflecting system state.
- Stateful buttons (on/off images, system mute, local toggle).
- Import and export of presets.
- Launch at login and haptic feedback.
- Stable code signing.
