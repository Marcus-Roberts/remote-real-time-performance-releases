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
