# Map sample

This project use firebase, with tutorial:

firebase.google.com/docs/flutter/setup?platform=android

dart pub global activate flutterfire_cli

npm install -g firebase-tools

Check

- firebase login
- firebase --version
- flutterfire --version
- environment variable pub/chache/bin...

flutter pub add firebase_core

flutterfire configure failed -> firebase logout then -> firebase login

create firebase project map.sample (4 steps)

- paste the goolge-services.json in app/
- plugins -> settings.gradle in android/ (should be in build.gradle but meh
  screw it)
- dependencies -> build.gradle in android/ (above flutter{...})
- plugins in app/

On lib/main.dart: import 'package:flutter/material.dart'; import
'package:firebase_core/firebase_core.dart'; import 'firebase_options.dart';

Future<void> main() async { WidgetsFlutterBinding.ensureInitialized(); await
Firebase.initializeApp( options: DefaultFirebaseOptions.currentPlatform, );
runApp(const MyApp()); }
