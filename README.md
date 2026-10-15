# Rhythm Link releases

The release feed the app's updater reads (`release.json`) and the
install artifacts humans download. The `latest` release carries:

- `Rhythm Link.dmg` — the macOS FRESH-INSTALL artifact: download, open,
  drag Rhythm Link to Applications, launch. After this first install,
  the app updates itself.
- `Rhythm Link_<version>_x64_en-US.msi` — the Windows fresh-install
  artifact: download and run the installer. After this first install,
  the app updates itself.
- `Rhythm Link.app.tar.gz` + `.sig` and the MSI's `.sig` — the
  updater's own artifacts, fetched and verified by the app. Do
  not download these by hand.

An update applies at the next launch BEFORE sign-in: the splash shows
the download and install, then the app restarts into the new version.

## TUI install

The terminal frontend (the TUI) ships as its own minisign-signed
package per platform — `Rhythm Link.TUI_<version>_<platform>.tar.gz` /
`.zip`, each with a detached `.sig`. The installers below verify the
signature against a public key embedded in the script (the same keypair
the GUI's updater pins) and refuse to install on any mismatch. The
signature is the trust root.

macOS (Terminal) — installs `rhythm-link` + `rhythm-link-helper` into
`~/.local/bin` (no sudo; fetches `minisign` via Homebrew if missing):

```sh
curl -fsSL "https://github.com/Marcus-Roberts/remote-real-time-performance-releases/releases/download/latest/install-tui-macos.sh" | bash
```

Windows 10/11 x64 (PowerShell) — installs the two executables into
`%LOCALAPPDATA%\RhythmLink\bin`, adds it to your user PATH (fetches a
hash-pinned `minisign` to verify):

```powershell
irm "https://github.com/Marcus-Roberts/remote-real-time-performance-releases/releases/download/latest/install-tui-windows.ps1" | iex
```

Start the app with `rhythm-link` (macOS: a new terminal if the PATH line
was needed). Re-running an installer is a safe upgrade. The TUI prints
its version at boot (there is no `--version` flag); the helper beside it
is required for its self-updates. Uninstall by deleting the two files
from the install folder.
