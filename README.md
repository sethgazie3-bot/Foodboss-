# FoodBoss — Android-ready app starter

FoodBoss is a mobile-first food delivery prototype for Johannesburg, South Africa. This project is now configured to be wrapped as an Android app using Capacitor.

## What's included
- Customer ordering prototype: restaurant discovery, search, categories, menus, cart, ZAR totals and demo checkout.
- Restaurant dashboard: shared demo order queue and status updates.
- Driver dashboard: pickup/drop-off tasks and delivery status updates.
- Responsive design for Android phones and desktop.
- Capacitor configuration for Android packaging.

## Requirements
- Node.js 18+ and npm
- Android Studio (current stable release)
- Android SDK installed through Android Studio
- Java version supported by your installed Android Gradle Plugin (Android Studio's bundled JDK is usually the easiest choice)

## Run the web preview
```bash
npm install
npm run dev
```

## Create the Android project
From this folder:

```bash
npm install
npx cap add android
npm run android:sync
npm run android:open
```

In Android Studio, wait for Gradle sync, choose an emulator or connect an Android phone with USB debugging enabled, then press Run.

If you change the React app later, run:
```bash
npm run android:sync
```

## Build an installable APK
After the Android project has been generated and synced, open it in Android Studio:
1. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)** for a test APK.
2. For Google Play, use **Build → Generate Signed Bundle / APK** and choose **Android App Bundle (AAB)**.
3. Keep signing keys private and backed up. Never commit them to a public repository.

Exact menu names can vary slightly by Android Studio version. Google Play publishing requires a developer account, store listing, privacy disclosures, app testing and compliance with current Play policies.

## Important: this is not yet a live delivery service
This starter is a frontend prototype packaged for Android development. It does not yet include:
- Backend server, persistent database or shared orders across different phones
- Secure sign-in and role permissions
- Real payment processing or refunds
- Live driver GPS, routing or push notifications
- Restaurant onboarding, driver verification, customer support or admin moderation

The demo orders are sample data and reset when the app reloads. Checkout does not collect payment or dispatch a driver.

## Suggested production build
1. Create a backend API and PostgreSQL database.
2. Add customer, restaurant, driver and admin authentication with server-enforced permissions.
3. Add order persistence and real-time updates.
4. Integrate a South African payment provider after merchant onboarding.
5. Add address lookup, map routing, driver location permissions and push notifications.
6. Add cancellation/refund rules, delivery zones, audit logs and support workflows.
7. Review POPIA and relevant South African consumer, food and business requirements before launch.

## Project files
- `src/main.jsx` — app screens and demo interactions
- `src/styles.css` — responsive styling
- `capacitor.config.json` — Android app configuration
- `package.json` — dependencies and scripts
