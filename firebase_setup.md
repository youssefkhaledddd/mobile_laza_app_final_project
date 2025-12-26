# 🔥 Firebase Setup Guide – LAZA App

This explains how Firebase is configured and connected to the LAZA Flutter application.
==========================================================================================================================
## 1️⃣ Create Firebase Project
1. Go to:
   https://console.firebase.google.com
2. Click **Create Project**
3. Enter project name: `LAZA App`
4. Disable Google Analytics (optional)
5. Create project
==========================================================================================================================
## 2️⃣ Add Android App
1. Click **Add App → Android**
2. Package name:com.example.laza_app
4. Place file in:google-services.json
==========================================================================================================================
android/app/

## 3️⃣ Enable Firebase Services
### 🔐 Authentication
- Enable **Email / Password** authentication
### 📦 Firestore Database
- Create Firestore database
- Start in **Test Mode** (for development)
- Change rules later using `firestore.rules`
  ==========================================================================================================================
## 4️⃣ FlutterFire Configuration
Run the following commands:
dart pub global activate flutterfire_cli
firebase login
flutterfire configure
This will generate:
lib/firebase_options.dart
==========================================================================================================================
The project uses the following Firebase packages:
firebase_core
firebase_auth
cloud_firestore
==========================================================================================================================
