# StudyFlow — Working Student Planner Web/PWA

This is a complete, responsive, offline-capable student assignment tracker built with plain HTML, CSS and JavaScript. There are **no external frontend dependencies**, no authentication, and no backend; data is saved to the browser's localStorage on the current device. This makes it a practical one-day assignment project.

## Run it locally (Windows + VS Code)
1. Extract this ZIP and open `StudyFlow_Project` in VS Code.
2. Open the VS Code terminal.
3. Run `cd www` then `python -m http.server 8000` (Python installed), **or** use VS Code's Live Server extension on `www/index.html`.
4. Visit `http://localhost:8000` to use the app.
5. Try add, edit, mark complete, delete, search, filter, export and import. Data persists when reloading this browser.

Opening `www/index.html` directly can work for basic use, but the offline/service-worker installation requires `localhost` or HTTPS.

## Publish the web version
For the simplest static deployment, go to https://app.netlify.com/drop and drag the **www directory** into the upload area. This publishes your complete site and provides a URL. You can also publish the `www` folder to other static hosts.

## Android APK with Capacitor (requires internet on your PC + Android Studio)
1. Install current Node.js 22+ and Android Studio, including the Android SDK.
2. Open a terminal in the **project root** (`StudyFlow_Project`), not inside `www`.
3. Run:

```powershell
npm install @capacitor/core
npm install -D @capacitor/cli
npm install @capacitor/android
npx cap add android
npx cap sync android
npx cap open android
```

Note: `capacitor.config.json` already exists, with `webDir` set to `www`, so you don't need `npx cap init` for this project. Android Studio can build an APK using **Build > Build Bundle(s) / APK(s) > Build APK(s)**. Install the resulting debug APK on a test device. The UI code remains in `www`. After changing it, rerun `npx cap sync android` before a new Android build.

If needed, see official docs: https://capacitorjs.com/docs/getting-started and https://capacitorjs.com/docs/android

## Features
- Add / edit / delete assignments
- Assign course, priority, deadline and notes
- Complete / reopen assignments
- Dashboard counts and completion progress
- Upcoming and completed views
- Search, filter by priority, sort by date/priority/recent
- Browser-local persistence (`localStorage`)
- JSON export and import
- Offline service worker and installable web manifest
- Responsive desktop and mobile layout

## Submission evidence
- Public live website URL
- Android APK if the teacher requires an Android/iOS app
- Miro brainstorming board share link + screenshots
- Screenshots: dashboard, create task, task list, completed task, Android app
- Brief demonstration of add > complete > refresh (data persists)

## Scope / limitations
- Data is stored **per device and browser**; there is no user account or cloud synchronization.
- App is a functional offline-first demo, not a deployed Android APK. You must create the APK in Android Studio and test it yourself.
- The four example tasks are demo-only; delete or edit them to customize your submission.
