# Open World Series

An original first-person open-world survival demo for Android, built from scratch.
Walk and explore a procedurally generated low-poly 3D world, chop trees to collect
wood, and craft a campfire to survive.

This project is independent original work. It does not use code or assets from any
other game.

## Download

Get the latest `open-world-series.apk` from the
[Releases](../../releases) page and install it on your Android phone
(allow "install from unknown sources" when prompted). Minimum Android 7.0 (API 24).

## How to play

The game opens on a home screen. Tap **PLAY** to enter the world, or **SETTINGS**
to adjust look sensitivity, invert look, and graphics quality (saved on your device).

- **Move:** left on-screen joystick
- **Look:** drag on the right side of the screen
- **Chop:** CHOP button when facing a nearby tree (3 chops per tree, +3 wood)
- **Craft:** CRAFT button once you have 5 wood to place a campfire

Goal: collect 5 wood and build your campfire.

## Tech

- Native Android `WebView` wrapper (Java, no external app dependencies)
- Game written in HTML5 + WebGL with [Three.js](https://threejs.org/) (MIT),
  bundled locally so the game runs fully offline
- All terrain, trees, clouds, rocks and campfire are generated in code;
  no external art assets

## Build from source

The APK is built without Gradle using the Android SDK command-line tools
(`aapt2`, `javac`, `d8`, `zipalign`, `apksigner`). See `build.sh` for the
full pipeline. Set your own keystore password where `build.sh` indicates.

## Version

- v0.2.0 (versionCode 3) - home screen with PLAY and SETTINGS (look sensitivity,
  invert look, graphics quality). NOTE: v0.2.0 is signed with a new key, so
  uninstall any v0.1.x install before installing v0.2.0.
- v0.1.1 (versionCode 2) - fix: thumb starting on the visible joystick now moves
  the player (joystick visuals no longer swallow touches)
- v0.1.0 (versionCode 1) - first playable prototype
