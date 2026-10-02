# My App

A native desktop app: double-click it and a window opens running your code.
Your code lives in `app/index.html` (HTML/CSS/JavaScript, as much as you want).

## Easiest: build it in the cloud (nothing to install)
1. Create a free GitHub account and a new repository.
2. Upload everything in this folder (including the hidden `.github` folder).
3. Open the repo's **Actions** tab. Wait for "Build apps" to finish (a few minutes).
4. Open the finished run and download from **Artifacts**:
   - `app-windows-latest`  ->  `MyApp.exe` (single file, double-click to run)
   - `app-macos-latest`    ->  zip containing `My App.app`
   - `app-ubuntu-latest`   ->  `.AppImage` (double-click to run)

## Or build on your own computer
1. Install Node.js LTS from https://nodejs.org
2. In this folder: `npm install`
3. Test: `npm start`
4. Build: `npm run build`  -> result is in `dist/`
(You build the Windows .exe on Windows, the Mac app on a Mac.)

## Put it on your website
Upload the file and link to it:

    <a href="/downloads/MyApp.exe" download>Download for Windows</a>

Mac users should get the .zip (unzip, then open the app).

## Notes
- Unsigned apps trigger "unknown publisher" warnings: Windows SmartScreen ("More info" -> "Run anyway") and Mac Gatekeeper (right-click -> Open). Removing the warnings requires paid code-signing certificates.
- App name / ID: `productName` and `appId` in `package.json`
- Icon: put `build/icon.ico` (Windows), `build/icon.icns` (Mac), `build/icon.png` (Linux, 512x512) in a `build` folder
- Window size and title: `main.js`
