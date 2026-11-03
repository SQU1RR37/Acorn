# Squirrels Farm Manager (Android)

A local-only account organizer for up to 100 Top Lords game accounts. It is an account inventory tool, not a bot or account-registration automation tool.

## Features
- Add, edit, search, and delete up to 100 account records
- Track username, login email, password, server, status, creation date, last login, and notes
- Local encrypted vault using AES-256-GCM with the key held in Android Keystore
- No network permission and Android backup disabled
- Dark Material 3 interface

## Build
1. Install Android Studio (current stable) and Android SDK Platform 35.
2. Open this folder in Android Studio.
3. Allow Gradle sync to finish.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Install the generated APK from `app/build/outputs/apk/debug/app-debug.apk`.

Minimum Android version: Android 8.0 (API 26).

## Security notes
- Account data is encrypted at rest using AES/GCM; the encryption key is generated and retained by Android Keystore.
- The app has no Internet permission and disables Android cloud backup.
- If app data is cleared or the app is uninstalled, the vault and its Keystore key are removed. There is currently no export/restore feature.
- Store only account credentials you are authorized to manage. Use the game's official account and recovery processes.
- The app does not create game accounts, interact with the game client, bypass CAPTCHA, or evade service limits.
