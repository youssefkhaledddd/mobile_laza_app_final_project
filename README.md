# mobile_laza_app_final_project
🛍️ Laza – E-Commerce Mobile App (Flutter)
📌 Project Overview
Laza is an e-commerce application built with Flutter, providing a complete shopping experience (MVP) that includes:
Authentication
Product Display via API
Cart
Favorites
Checkout
Orders
Firebase Integration
This project was developed as part of the Final Project – Mobile Programming Course.
==================================================================================================================================================
🧰 Technologies Used
Flutter (Android)
Firebase Authentication
Cloud Firestore
REST API
Provider (State Management جزئي)
Material UI
==================================================================================================================================================
🔐 Authentication (Firebase)
✔️ Features:
Sign up باستخدام Email & Password
Login
Logout
Auto-login (Persist Login State)
Password Reset
===========================================
📂 Files:
lib/auth/login_screen.dart
lib/auth/signup_screen.dart
main.dart
===========================================
📦 Firebase Structure:
users/{uid}
  ├── email
  └── createdAt
==================================================================================================================================================
🛒 Products (API Integration)
✔️ Source:
https://api.escuelajs.co/api/v1/products
------------------------------------------------------------------------------
✔️ Features:
Fetch products from REST API
Display products in GridView
Search products by name
Product Details Page
------------------------------------------------------------------------------------------------------------------------------------------------------------
📂 Files:
lib/services/product_service.dart
lib/models/products.dart
lib/home/home_screen.dart
lib/pages/product_details_page.dart
------------------------------------------------------------------------------------------------------------------------------------------------------------
❤️ Favorites (Wishlist)
✔️ Features:
Add / Remove favorites
Favorites page
Linked with product details
------------------------------------------------------------------------------
📂 Files:
lib/services/favorite_service.dart
lib/models/favorite.dart
lib/pages/favorites_page.dart
==================================================================================================================================================
📦 Firestore Structure:
favorites/{userId}/orders/{productId}/
------------------------------------------------------------------------------------------------------------------------------------------------------------
🚚 Checkout Flow (Advanced)
🧭 Flow:
Cart → Address → Payment → Order Success
==================================================================================================================================================
📍 Address Page
✔️ Features:
Enter shipping details:
Full name
Phone number
City
Street address
------------------------------------------------------------------------------------------------------------------------------------------------------------
📂 File:
lib/pages/address_page.dart
==================================================================================================================================================
💳 Payment Page
✔️ Features:
Select payment method:
Cash on Delivery (COD)
Credit Card (UI only)
Confirm order
------------------------------------------------------------------------------------------------------------------------------------------------------------
📂 File:
lib/pages/payment_page.dart
==================================================================================================================================================
📦 Orders
✔️ Features:
Create order after checkout
Save full order details
Order Success Page
------------------------------------------------------------------------------------------------------------------------------------------------------------
📂 Files:
lib/services/order_service.dart
lib/pages/order_success_page.dart
==================================================================================================================================================
👤 Profile Page
✔️ Features:
Display user email
Logout
------------------------------------------------------------------------------------------------------------------------------------------------------------
📂 File:
lib/pages/profile_page.dart
==================================================================================================================================================
🔥 Firebase Summary

✔️ Services Used:
Firebase Authentication
Cloud Firestore
------------------------------------------------------------------------------------------------------------------------------------------------------------
✔️ Collections:
users
carts
favorites
orders
------------------------------------------------------------------------------------------------------------------------------------------------------------
1️⃣ Install Flutter SDK

Download Flutter SDK from:
https://flutter.dev/docs/get-started/install

Extract Flutter to:
C:\flutter   (Windows)

Add Flutter to PATH:
C:\flutter\bin

Verify installation:
flutter doctor
==================================================================================================================================================
2️⃣ Install Project Dependencies
flutter pub get
==================================================================================================================================================
🔥 Firebase Setup Steps
1️⃣ Create Firebase Project
Go to:
https://console.firebase.google.com
Create a new project
==================================================================================================================================================
2️⃣ Add Android App to Firebase
Package name:
com.example.laza_app
==================================================================================================================================================
Download:
google-services.json
==================================================================================================================================================
Put it in:
android/app/
==================================================================================================================================================
3️⃣ Enable Firebase Services
From Firebase Console:
🔐 Authentication
Enable Email/Password
==================================================================================================================================================
📦 Firestore Database
Create Firestore database
Start in test mode (for development)
==================================================================================================================================================
4️⃣ FlutterFire CLI Setup
dart pub global activate flutterfire_cli
firebase login
flutterfire configure
lib/firebase_options.dart
==================================================================================================================================================
🔐 Firestore Rules Installation

Firestore Rules (Development / Course Project)
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {

    match /users/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }

    match /carts/{userId}/items/{itemId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }

    match /favorites/{userId}/items/{itemId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }

    match /orders/{orderId} {
      allow create: if request.auth != null;
      allow read: if request.auth != null;
    }
  }
}
==================================================================================================================================================

▶️ How to Run the Application

📱 Run on Android Emulator
Open Android Studio
Start Emulator
==================================================================================================================================================
Run:
flutter run
==================================================================================================================================================
📱 Run on Physical Android Device
Enable Developer Options
flutter run
==================================================================================================================================================
🍎 Run on iOS (Mac only)
flutter pub get
cd ios
pod install
cd ..
flutter run
==================================================================================================================================================
📌 Requires:
macOS
Xcode
CocoaPods
==================================================================================================================================================
🏗️ Build APK (Android)
flutter build apk
==================================================================================================================================================
Output:
build/app/outputs/flutter-apk/app-release.apk
==================================================================================================================================================
🏗️ Build iOS (Release)
flutter build ios
==================================================================================================================================================
