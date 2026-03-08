# Xune

A modern desktop client for the Zune media ecosystem.

Download the latest build from [Releases](https://github.com/magicisinthehole/xune-releases/releases).

---

## macOS

### Apple Silicon (arm64)
- **DMG** — Drag to Applications to install.
- **Portable ZIP** — Self-contained, runs from any directory. Data stored alongside the app.

### Intel (x64)
- **DMG** — Drag to Applications to install.
- **Portable ZIP** — Self-contained, runs from any directory. Data stored alongside the app.

### Data Locations
- **Installed:** `~/Library/Application Support/xune`
- **Portable:** `Xune.app/Contents/MacOS/Data/`

---

## Linux

### x86_64 (x64)
- **AppImage** — Portable, runs on most Linux distributions. Make executable and run.
- **.deb** — For Debian/Ubuntu. Install with `sudo dpkg -i xune_<version>_amd64.deb && sudo apt-get install -f`
- **Flatpak** — Install with `flatpak install Xune-<version>-x64.flatpak`
- **Portable tar.gz** — Self-contained, runs from any directory. Data stored alongside the app.

### ARM64 (aarch64)
- **AppImage** — Portable, runs on ARM64 Linux distributions. Make executable and run.
- **.deb** — For Debian/Ubuntu on ARM64. Install with `sudo dpkg -i xune_<version>_arm64.deb && sudo apt-get install -f`
- **Flatpak** — Install with `flatpak install Xune-<version>-arm64.flatpak`
- **Portable tar.gz** — Self-contained, runs from any directory. Data stored alongside the app.

### Flatpak Setup
The Flatpak bundle requires the Freedesktop Platform runtime. If not already configured:
```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.freedesktop.Platform//24.08
```

### USB Device Setup
The .deb package installs udev rules automatically. For AppImage and Flatpak, use **Settings > General > Device Connection** to install USB rules from within the app.

Alternatively, from the command line:
```bash
# AppImage:
./Xune-*.AppImage --appimage-extract-and-run usr/bin/xune-install-udev-rules

# Flatpak:
flatpak run --command=xune-install-udev-rules com.xune.app
```

### Data Locations
- **Installed:** `~/.local/share/xune` (data), `~/.cache/xune` (cache)
- **Portable:** Data stored alongside the executable
