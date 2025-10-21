# eDEX-UI (jtan289 fork)

This repository contains my Apple Silicon updates for [eDEX-UI](https://github.com/GitSquared/edex-ui), the sci-fi terminal emulator created by Gabriel "Squared" Saillard. The upstream project is no longer maintained, so this fork refreshes the build tooling and fixes the native modules on macOS arm64.

## Requirements
- macOS with Node.js 18.x
- Xcode Command Line Tools (`xcode-select --install`)

## Run from source
```bash
npm install
cd src && npm install && cd ..
npx @electron/rebuild -f -w node-pty
npm run start
```

## Build (macOS arm64 dmg)
```bash
npm run build-darwin
# output: dist/eDEX-UI-macOS-arm64.dmg
```

## Notes
- Electron upgraded to v28, `node-pty` pulled from the Microsoft repo.
- GPU acceleration kept enabled (see `src/_boot.js`).
- Original assets, license and credits remain under GPLv3.

Thanks again to the upstream author and contributors for the original work.
