Consensual Live-Location Starter (Flutter)
=========================================

What this is
------------
A minimal, consent-first Flutter starter for a live-location sharing app (owner invites, receiver accepts and shares).
This is a starting point — it is NOT a production-ready app. You must complete Firebase configuration, app signing, and review platform-specific background permission steps before publishing.

Contents
--------
- pubspec.yaml
- lib/main.dart
- lib/auth_page.dart
- lib/home_page.dart
- lib/create_invite.dart
- lib/accept_invite.dart
- README has build & Firebase setup steps.

How to use
----------
1) Install Flutter on your machine: https://flutter.dev/docs/get-started/install
2) Create a new Flutter app:
   flutter create consensual_location_app
3) Replace the generated pubspec.yaml and the lib/ folder with the files from this ZIP.
4) Run:
   flutter pub get
   flutter run

To build an APK:
   flutter build apk --release
or to install on a connected device:
   flutter install

Firebase setup (quick)
----------------------
1. Create Firebase project at https://console.firebase.google.com/
2. Add Android app (package name e.g. com.example.consensual_location_app) and add SHA-1.
3. Download google-services.json and place into android/app/.
4. Enable Authentication (Email/Password), Firestore, and Dynamic Links (optional).
5. Follow FlutterFire docs to initialize Firebase: https://firebase.flutter.dev/docs/overview

Important notes
---------------
- This app requires location permissions. For background sharing, you must add platform-specific manifest/Info.plist entries and justify background usage to Apple; Android needs foreground service + ACCESS_BACKGROUND_LOCATION.
- NEVER use this app without explicit, informed consent from the person sharing their location.
- Review and tighten Firestore security rules before deployment.
