# Build MT5 Bot Android APK using only an Android phone

This project includes a GitHub Actions workflow to compile the debug APK in the cloud.

## Steps
1. Download and extract `MT5BotAndroid-cloud-build.zip` using a file manager that supports ZIP extraction.
2. In your phone browser, sign in to GitHub and create a new repository named `MT5BotAndroid`. A private repository is fine.
3. Upload the contents of the `MT5BotAndroid` folder into the repository, preserving folders including `.github/workflows/build-apk.yml`. GitHub's web upload may hide dot-folders; if so, upload the workflow separately using Add file → Create new file and use the path `.github/workflows/build-apk.yml`.
4. Open the repository's **Actions** tab. Choose **Build Android APK** and press **Run workflow**. If the workflow does not appear, verify that `.github/workflows/build-apk.yml` exists in the `main` branch.
5. Wait for the run to finish successfully. Open the completed run and find **Artifacts** near the bottom.
6. Download `MT5BotAndroid-debug-apk`, extract the downloaded artifact ZIP, and locate `app-debug.apk`.
7. Tap the APK to install it. Android may ask you to allow installs from your browser or file manager; only enable this for the app you trust, then disable it again after installation.

## Important
- This builds a debug APK, not a Play Store release APK.
- A successful build only means the Android project compiled. The current app is a dashboard prototype and is not yet connected to MT5 or capable of placing trades automatically.
- Do not enter your Exness password or trading credentials into an unverified app. Automatic demo execution needs a separately implemented and secured MT5 bridge/EA connection.
