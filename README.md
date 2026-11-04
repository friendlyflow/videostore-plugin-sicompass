# videostore-plugin-sicompass

*The Sicompass video store: your videos as a grid, played inside the window.*

This plugin is part of [Sicompass](https://github.com/friendlyflow/sicompass), a
keyboard-first, accessibility-first way to use your entire computer.

It shows a folder of videos as a grid of three columns, each with its first picture and its
file name. Subfolders are rows you enter with Right. Moving onto the grid, your screen reader
says how many videos it holds. Press i to go to the first one and a to go to the last, move
with the arrows, and press Enter or d to play one. Enter again pauses, Escape goes back. Nothing
opens in another program.

It only reads. It never changes, moves or deletes a file. It lists MP4, M4V, WebM, MKV, MOV,
AVI, MPEG and Ogg video files, and skips everything else.

## Settings

- **video folder**: the folder to show. A relative path is under your home folder, and the
  default is `Videos`.
- **sort order**: by name, or by date with the newest first.

## Install

In Sicompass, open store, then programs, and press Enter on install next to video store.
The Store checks the release's signature before installing it, and keeps it up to date.

To install a build of your own instead, copy `plugin.json`, the built `plugin` program
(`plugin.exe` on Windows) and `locales/` into a folder named `videostore` in the Sicompass
plugins folder (`~/.config/sicompass/plugins/` on Linux, `~/Library/Application
Support/sicompass/plugins/` on macOS) and restart Sicompass.

## Building from source

```bash
nix develop -c cargo build
nix develop -c cargo test
```

## License

GPL-3.0-only. See [LICENSE](LICENSE).
