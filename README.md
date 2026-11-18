<p align="center">
  <img src="assets/logo.png" alt="PinConsole logo" width="160">
</p>

<h1 align="center">PinConsole</h1>

https://github.com/user-attachments/assets/7c21e48d-1ad7-4950-9240-427cebbe687b


PinConsole is a free, instant image & GIF search bar for Windows, macOS and Linux.

Press **Ctrl+Shift+R** anywhere, type, and pick a result with its number and it's copied to your clipboard, or pasted into your chat (and sent).

Search Pinterest, Bing, Tenor GIFs, Wallhaven, Openverse and Google.

### How is this better than discord's gif search?

- It's personalized, following your account's algorithm
- Supports images
- Can be bound to any shortcut
- Built with speed as its priority
- Supports 6 sources that are not Klipy
- Works on any app, including image and video editing apps
- Customizable appearance, grid, and usability wise
- Has history, more filters, and supports saving gifs and images locally
- Supports multiple favorites folders


note: PinConsole is not meant to replace Discord’s GIF search. This section is only a simple comparison


**[⬇ Download the latest release](https://github.com/mosasomo/PinConsole/releases/latest)**
  
Supports Windows 10/11, macOS 12+ and Linux (x64 and arm64). Updates are free and install automatically.

(Linux and macOS builds are not as thoroughly tested. Expect some bugs, and please [report](https://github.com/mosasomo/PinConsole/issues) if you meet any.)

PinConsole is free of bloatware and contains no malware. It does not collect any telemetry or usage data.


### More guides below ⬇️

---

## Contents

- [Install](#install)
  - [Windows](#windows)
  - [macOS](#macos)
  - [Linux](#linux)
- [How to use](#how-to-use)
- [Services](#services)
- [GIFs](#gifs)
- [Copy, paste and send](#copy-paste-and-send)
- [Pro customizations](#pro-customizations)
- [Uninstall](#uninstall)
- [Notes](#notes)

---

## Install

On the [latest release](https://github.com/mosasomo/PinConsole/releases/latest) page, download the **Setup** zip for your system:

| System | Download |
|---|---|
| Windows 10 / 11 | `PinConsole-Setup-Windows.zip` |
| macOS, Apple Silicon (M1, M2, M3…) | `PinConsole-Setup-macOS-arm64.zip` |
| macOS, Intel | `PinConsole-Setup-macOS-x64.zip` |
| Linux, most PCs | `PinConsole-Setup-Linux-x64.zip` |
| Linux, ARM (e.g. Raspberry Pi) | `PinConsole-Setup-Linux-arm64.zip` |

### Windows

1. Unzip `PinConsole-Setup-Windows.zip`. Unzip the **whole folder**, so `PinConsole.exe` is next to `Install.bat`.
2. Double-click **`Install.bat`**.
3. Press **Ctrl+Shift+R** anywhere to search.

- It installs to `%LOCALAPPDATA%\PinConsole` and starts when you log in.
- Windows may say **"Windows protected your PC"** because the app isn't signed. Click **More info → Run anyway**.
- It replaces PinConsole 1.x and the old PinterestConsole, and keeps your settings, license and linked account.

### macOS

Needs macOS 12 Monterey or newer.

1. Unzip the zip for your Mac (`arm64` for Apple Silicon, `x64` for Intel).
2. Double-click **`Install.command`**.
   If macOS refuses to open it: **right-click it → Open → Open**.
3. Press **Cmd+Shift+R** anywhere to search.

- It installs `PinConsole.app` into your Applications folder and starts it.
- There's **no Dock icon**. It waits in the background for Cmd+Shift+R.
- **Auto-paste** needs permission: allow PinConsole in **System Settings → Privacy & Security → Accessibility**. PinConsole opens that page the first time it tries to paste. macOS may ask again after an update.

### Linux

1. Unzip the zip for your PC (`x64` for most PCs, `arm64` for ARM).
2. In a terminal, inside the unzipped folder, run:
   ```sh
   sh install.sh
   ```
3. Press **Ctrl+Shift+R** anywhere to search (X11).

- It installs to `~/.local/share/pinconsole`, adds a menu entry and starts at login.
- **Wayland** doesn't let apps set global shortcuts. In your system's keyboard settings, add a custom shortcut that runs:
  ```
  ~/.local/share/pinconsole/PinConsole --toggle
  ```
- **Auto-paste** needs `xdotool` (X11) or `wtype` / `ydotool` (Wayland). Copying images is most reliable with `xclip` (X11) or `wl-clipboard` (Wayland). For example:
  ```sh
  sudo apt install xdotool xclip
  ```

---

## How to use

Shortcuts are written for Windows and Linux. **On a Mac, read Ctrl as Cmd and Alt as Option.**

| Key | Action |
|---|---|
| **Ctrl+Shift+R** | Open / close the search bar |
| *Type* | Results show up as you type |
| **Ctrl+1 … 0** | Copy one of the 10 results on screen |
| **↓ / ↑** | Scroll the results one row |
| **PageDown / PageUp** | Scroll a page |
| **Enter** | Open the search in your browser |
| **Tab / Shift+Tab** | Next / previous service |
| **Ctrl+G** | GIF search on / off |
| **Ctrl+H** | Show every shortcut |
| **Ctrl+,** | Settings |
| **Esc** | Close |

**Mouse:** left-click an image to copy it, right-click to open its page.

> [!TIP]
> **Ctrl+H** always lists your current shortcuts, so you don't need to memorize these.

---

## Services

| Service | Notes |
|---|---|
| **Pinterest** | The default. Pro can personalize it with your Pinterest account. |
| **Google** | Needs a free Google API key (100 searches a day): **Settings → Services**. Without a key, Enter still opens Google Images. |
| **Bing** | Works out of the box, including GIFs. |
| **Tenor GIFs** | GIFs only. |
| **Wallhaven** | Wallpapers. No GIFs. |
| **Openverse** | Openly licensed (Creative Commons) images. |

Choose which services **Tab** cycles through in **Settings → Services**.

---

## GIFs

- **Ctrl+G** switches the current service to GIF results (Tenor is always GIFs).
- GIFs play in the grid. Turn off **Autoplay GIFs** to play only the one under your mouse.
- A copied GIF goes on the clipboard as a `.gif` **file**, so it stays animated when you paste it into Discord, Slack, Teams, Finder, Explorer and so on. You can switch to **Copy GIFs as: Link** in settings.

---

## Copy, paste and send

| Key | Action |
|---|---|
| **Ctrl+S** | Switch between **Copy** and **Save** (saves the full-size image to `Pictures/PinConsole`) |
| **Ctrl+P** | **Auto-paste**: after copying, pastes into the window you were in |
| **Ctrl+E** | **Auto-send**: pastes, then presses Enter (the delay is adjustable in settings) |
| **Ctrl+N** | Number keys work **without Ctrl** (you can't type digits while results are showing) |
| **Ctrl+O** | **Original size**: show whole images instead of cropped tiles |

The current mode is shown, dimmed, at the top right of the bar. Click it to open settings.

---

## Pro customizations

**Everything above is free.** Pro is a one-time purchase in **Settings → Pro**, and works on up to 3 computers on any mix of Windows, macOS and Linux.

Pro adds:

- **Personalized Pinterest results** by linking your Pinterest account
- **History** (Ctrl+Y) and **favorites** (Alt+1 … 0 or middle-click to star, Ctrl+B to show). Favorites keep a copy on your computer, so they work offline.
- **Customizable grid**: columns, rows, tile sizes
- **15 themes** (Dracula, Nord, Catppuccin, Tokyo Night, Gruvbox, Rosé Pine…), your own custom theme, accent colors and fonts
- **Several save folders** (Ctrl+J switches between them)
- **Saved searches**, shape and size **filters**, **custom shortcuts** and a supporter badge

---

## Uninstall

| System | How |
|---|---|
| Windows | Run `Uninstall.bat` from the zip |
| macOS | Run `Uninstall.command` from the zip |
| Linux | Run `sh uninstall.sh` from the zip |

Each one asks whether to also delete your settings, saved searches, linked account and license. Images you saved are always kept.

Settings, history and favorites live in:

- **Windows:** `%APPDATA%\PinConsole`
- **macOS:** `~/Library/Application Support/PinConsole`
- **Linux:** `~/.config/pinconsole`

---

## Notes

- While PinConsole is running, Ctrl+Shift+R no longer does a "hard refresh" in browsers. Pro can change the shortcut.
- On Windows, auto-paste can't paste into programs running as administrator. The image is still on your clipboard.
- Pinterest, Bing and Tenor results come from their websites, not official APIs. If one of them changes its site, that service may stop showing results. Enter (open in browser) still works.
- Questions, bugs or ideas: [open an issue](https://github.com/mosasomo/PinConsole/issues), or use **Contact me** in Settings.
