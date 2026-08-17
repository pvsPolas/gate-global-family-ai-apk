# Gate Global Family AI — Android APK wrapper v1.0

Android WebView wrapper for:

**https://gateglobalfamily.ai/**

## App details

- App name: Gate Global Family AI
- Package ID: `ai.gateglobalfamily.app`
- Version: `1.0`
- minSdk: 24
- targetSdk: 35
- compileSdk: 35
- Start URL: `https://gateglobalfamily.ai/`

## Features

- Standalone Android application
- Secure HTTPS-only WebView
- JavaScript and DOM storage for modern web apps
- Cookies / session support
- Back button navigates web history
- File chooser support
- External-domain links open in the system browser
- Downloads hand off to the browser
- Loading progress indicator
- Temporary original GGF AI launcher icon
- GitHub Actions APK build workflow

## Build with GitHub Actions

1. Create a GitHub repository.
2. Upload/push this project to the repository root.
3. Open the **Actions** tab.
4. Select **Build Android APK**.
5. Select **Run workflow**.
6. When it finishes, download the artifact named:

   `gate-global-family-ai-apk`

Inside it will be:

`app-debug.apk`

## Build locally

Requirements:

- Android Studio with Android SDK 35
- Java 17

Open the project in Android Studio and use:

**Build > Build Bundle(s) / APK(s) > Build APK(s)**

Or from a terminal with Gradle 8.9 available:

```bash
gradle :app:assembleDebug
```

Result:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## Production release

The debug APK is suitable for testing and direct installation.

Before Play Store distribution, create a release signing key and configure a signed release build. Do not publish the debug signing key as a production credential.

## Branding

The included icon is a temporary original placeholder marked **GGF AI**. Replace it with official Gate Global Family artwork if you own or have permission to use the official brand artwork.

## Important WebView note

Some identity providers intentionally block authentication inside embedded WebViews. If the website uses Google/Microsoft/social OAuth and login fails, the authentication flow should be switched to Custom Tabs/App Links or the project should be migrated to a Trusted Web Activity after the website's PWA and Digital Asset Links are live.
