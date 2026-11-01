# Training Portal — Android app (WebView)

Bundles your pages (`index, ST*, SEPCO, RTO`) in `app/src/main/assets/www/` and runs them in a WebView.
Data is still live from your Apps Script Web App (needs internet).

## Build the APK (Android Studio)
1. Install Android Studio → **Open** this folder → wait for Gradle sync.
2. **Build ▸ Build Bundle(s) / APK(s) ▸ Build APK(s)** → `app/build/outputs/apk/debug/app-debug.apk`.
3. Copy the APK to the phone and install (allow "install unknown apps").

## Build without Android Studio
Push this folder to a GitHub repo → **Actions ▸ Build APK ▸ Run workflow** → download the APK artifact.

## Updating the pages
Replace the HTML files in `app/src/main/assets/www/` with the new versions, bump `versionCode`, rebuild.
`Admin.html` and `SFT.html` (linked from index.html) are not bundled — copy them into the same folder to enable those roles.
