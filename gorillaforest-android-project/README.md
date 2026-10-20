# Gorilla Forest Android APK project

This packages the supplied `Gorilla Forest.html` as a landscape Android app using Android WebView.

## Build an APK in GitHub (no Android SDK needed on your device)
1. Create a GitHub repository and upload the contents of this folder (not the outer folder itself).
2. Open the repository's **Actions** tab and select **Build Gorilla Forest APK**.
3. Press **Run workflow** (or push to `main`) and wait for the green check.
4. Open the completed workflow run, scroll to **Artifacts**, and download **Gorilla-Forest-APK**.
5. Extract the ZIP; `app-debug.apk` is the installable test APK. Android may ask you to allow installs from your browser/files app.

## Important limitations
- The app loads Three.js and other libraries from public CDNs, so it needs an internet connection.
- This WebView wrapper is for the game's non-VR preview; Android WebView does not reliably support WebXR immersive VR. For headset VR, host the HTML on HTTPS and open it in a WebXR-capable browser such as the Quest Browser.
- The supplied HTML's desktop preview uses keyboard controls (WASD, arrows, Space); it does not contain native Android touch controls.
- Multiplayer/voice features in the supplied HTML depend on the external room provider being available; this wrapper does not create or host a multiplayer server.
