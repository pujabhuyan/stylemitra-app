# StyleMitra — phone-only APK build kit

This package contains the current StyleMitra professional fashion-studio web prototype and a GitHub Actions workflow that builds an installable **debug APK** in the cloud. It does not contain a prebuilt APK; this environment does not have the Android SDK or Gradle installed, so the APK must be compiled by the cloud workflow.

## Build from an Android phone

You can do this in Chrome. A free GitHub account is required.

1. Download and extract `stylemitra-apk-build-kit.zip` on your phone.
2. Open https://github.com and sign in or create an account.
3. Create a new repository named `stylemitra-app`. For a first try, choose **Public** so GitHub Actions availability is straightforward. Do not upload passwords or API keys.
4. Upload the *contents* of this extracted folder to the repository, keeping the `.github/workflows/build-apk.yml` path. In GitHub mobile web, you may need to use the browser's **Desktop site** option. Make sure the `.github` folder and `www/index.html` are included.
5. Open the repository's **Actions** tab. If GitHub asks, enable Actions.
6. Choose **Build StyleMitra Android APK** on the left, tap **Run workflow**, then tap the green **Run workflow** button.
7. Wait for the workflow to finish with a green check mark. Open that run and find **Artifacts** near the bottom.
8. Download `StyleMitra-debug-APK`, extract the downloaded artifact ZIP, and locate `app-debug.apk`.
9. Tap the APK to install. Android may ask you to allow Chrome or Files to install unknown apps. Only allow this for the file you just built, then turn the permission off again if desired.

## Important

- This produces a **debug/test APK** for your own phone, not a Play Store release bundle.
- The prototype currently uses bundled web content. Its AI generation is not connected, and it is not yet a fully featured layer-based fashion editor.
- Keep the repository and build artifacts private if you later add personal content. Never put AI-provider API keys in the app or repository.
- If the workflow fails, open the run and copy the first red error message; it can be used to troubleshoot.
