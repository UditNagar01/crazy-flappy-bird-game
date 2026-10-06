# Flappy Bird — Friend Edition

This is a separate distribution version of the AWS Flappy Bird project. The original AWS submission is not modified.

## Web
Open `web/index.html` in a browser. It supports:
- Android/iPhone touch
- mouse click
- Space / Up Arrow
- R to restart after game over

For a public link, upload the `web` folder to a static host such as GitHub Pages or Netlify.

## Android APK
The `android-wrapper` folder packages the web game as a native Android app using Capacitor.

### Local build
Requires Node.js and Android Studio/Android SDK.

```bash
cd android-wrapper
npm install
npm run android:init
npm run android:open
```

Then build a debug APK from Android Studio, or run:

```bash
cd android
./gradlew assembleDebug
```

### GitHub Actions
The included workflow can build the APK automatically on Ubuntu. Push this folder to a GitHub repository, open Actions, choose **Build Android APK**, run it, then download the APK from the workflow artifacts.

## Gameplay settings
The web version keeps the same tuning as the submitted Pygame game:
- Gravity: 0.32
- Flap velocity: -7.5
- Pipe gap: 200 px
- Pipe speed: 3.5 px/frame
