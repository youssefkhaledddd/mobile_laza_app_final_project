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

✔️ Collections:
users
carts
favorites
orders
------------------------------------------------------------------------------------------------------------------------------------------------------------
