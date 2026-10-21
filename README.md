# Android Rust Notes

Plain text notes for Android, written in Rust. Each note is a file you can read without the app.

Uses little memory, starts fast, asks for as few permissions as it can, and keeps everything on the
phone. See [PRIVACY.md](PRIVACY.md).

## Features

- Search by any words, pin notes to the top
- Autosave while you type
- A 30 day trash with Undo
- Three text sizes; no account, no cloud

## Install

Download the APK from the releases page and follow [docs/INSTALL.md](docs/INSTALL.md).

## Build

Needs Rust with the `aarch64-linux-android` target, `cargo-ndk`, the Android SDK (build-tools 34,
platform 34), NDK r27c and a JDK 17. Then, from `apps/notes` (Windows PowerShell):

```
cargo test
powershell -File build-apk.ps1
```

APKs are signed with your own key, see [docs/SIGNING.md](docs/SIGNING.md).

## Layout

- `apps/notes/` the app
- `crates/heartnet-kit/` code shared with the other apps (exit handling, settings, theme)
- `tools/build/` the shared APK build script

## More apps

- [Android Rust Gallery](https://github.com/HusniHeartnet/android-rust-gallery)
- [Android Rust Files](https://github.com/HusniHeartnet/android-rust-files)
- [Android Rust Home](https://github.com/HusniHeartnet/android-rust-home)

## Licence

Copyright (C) heartnetapps. Licensed under the GNU General Public License, version 3 or (at your
option) any later version. See [LICENSE](LICENSE). The names and logos are not covered by the licence.
