
Luxporter Booking Widget - Installation Guide
=============================================

Files Included:
---------------
1. index.html      -> The main customer booking widget.
2. admin.html      -> Admin dashboard to view and export bookings.
3. README.txt      -> This installation guide.

Setup Instructions:
-------------------

A. Google Maps API:
-------------------
1. Go to https://console.cloud.google.com/
2. Create a project and enable:
   - Maps JavaScript API
   - Places API
3. Get your API key and replace in BOTH files:
   <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_GOOGLE_MAPS_API_KEY&libraries=places">

B. Firebase Setup:
------------------
1. Visit https://console.firebase.google.com/
2. Create a project named: the-luxporter
3. Enable Firestore Database (test mode)
4. Go to Project Settings > Web App
5. Replace the config object in BOTH files:
   const firebaseConfig = { ... }

C. Stripe & PayPal (Optional - Production Payments):
-----------------------------------------------------
Stripe:
- Get publishable and secret keys from https://dashboard.stripe.com/
- Integrate real payment session backend if required.

PayPal:
- Create an app at https://developer.paypal.com/
- Replace YOUR_PAYPAL_CLIENT_ID in:
  <script src="https://www.paypal.com/sdk/js?client-id=YOUR_PAYPAL_CLIENT_ID&currency=USD">

D. Deploying:
-------------
Option 1: GitHub Pages
- Push all files to your GitHub repo
- Go to Settings > Pages > Source > main/root
- Live at: https://your-username.github.io/your-repo/

Option 2: Local Hosting
- Open `index.html` and `admin.html` in browser.

-----------------------
Developed for: Kingsollomon / The Luxporter
