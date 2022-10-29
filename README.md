# Vikunja desktop

[![Build Status](https://drone.kolaente.de/api/badges/vikunja/desktop/status.svg)](https://drone.kolaente.de/vikunja/desktop)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](LICENSE)
[![Download](https://img.shields.io/badge/download-v0.20.0-brightgreen.svg)](https://dl.vikunja.io)

The Vikunja frontend all repackaged as a tauri app to run as a desktop app!

## Dev

As this repo does not contain any code, only a thin wrapper around tauri, you will need to do this to get the 
actual frontend bundle and build the app:

```bash
rm -rf frontend vikunja-frontend-master.zip 
wget https://dl.vikunja.io/frontend/vikunja-frontend-0.20.0.zip
unzip vikunja-frontend-0.20.0.zip -d frontend
sed -i 's/\/api\/v1//g' frontend/index.html # Make sure to trigger the "enter the Vikunja url" prompt
```

## Building for release

1. Make sure that you have `cargo` installed
2. Run the snippet from above, but with a valid frontend version instead of `master`
3. Change the version in `src-tauri/tauri.conf.json` (That's the one that will be used by tauri`
4. `cargo install tauri-cli`
5. `cargo tauri build`

## Sponsors

[![Relm](https://vikunja.io/images/sponsors/relm.png)](https://relm.us)

