# Roulette MVP

Browser-first roulette MVP built as a single static page.

## Run locally

Open `index.html` in a browser.

## Deploy

This repository is ready for GitHub Pages.

1. Push this repository to GitHub.
2. Open repository `Settings`.
3. Go to `Pages`.
4. Set source to `Deploy from a branch`.
5. Select branch `main` and folder `/root`.

The game will be available at:

`https://<github-username>.github.io/<repository-name>/`

## Android offline app

The `android/` folder packages the same static game into a native Android WebView app.
It loads `android/app/src/main/assets/www/index.html`, so it works without network access.

Build a debug APK from Android Studio:

1. Open the `android/` folder.
2. Select `Build` > `Build APK(s)`.

Or build from PowerShell if Gradle is available:

```powershell
$env:JAVA_HOME='C:\Program Files\Android\Android Studio\jbr'
gradle -p android assembleDebug --offline
```

The debug APK is generated at:

`android/app/build/outputs/apk/debug/app-debug.apk`

Install on a connected test phone:

```powershell
adb install -r android/app/build/outputs/apk/debug/app-debug.apk
```
