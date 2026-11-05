# Bookshelf – Android app

Your book reader, wrapped as a native Android app (Capacitor). Native extras: screen stays on while reading, real scheduled "resume your book" notifications, status-bar hiding for full screen, and the Back button.

## Option A – get an APK without installing anything (GitHub)
1. Create a free GitHub account and a new empty repository.
2. Upload every file in this folder to it (keep the `.github` folder).
3. Open the **Actions** tab → **Build Android APK** → **Run workflow**.
4. When it finishes (about 5 minutes), open the run and download **Bookshelf-debug-apk**. Unzip it to get `app-debug.apk`.
5. Send the APK to your phone, open it and allow "Install unknown apps" when asked.

## Option B – build on your computer
Install Node 20+, JDK 17 and Android Studio, then:
```
npm install
npx cap sync android
npx cap open android
```
In Android Studio choose **Build → Build APK(s)**.

## Publishing to Google Play
The APK above is a debug build for personal use. For Play Store you need a signed release (AAB) and a Play developer account.

## Changing the app
The app lives in `www/index.html`. After editing run `npx cap sync android` and rebuild.
