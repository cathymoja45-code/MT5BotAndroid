# MT5 Bot Android — Version 1.0

A native Android application shell with a bundled dark dashboard for the EURUSDm M5 EMA/RSI/ATR strategy. It stores display settings locally on the device.

## Important scope / safety
- This first version is a dashboard prototype, not a connected trading system.
- It does not log in to Exness, read real account balance, receive market prices, or submit trades.
- The balance shown is illustrative and editable; it is not account data.
- The demo-start control is intentionally disabled until a real, authenticated MT5 bridge is implemented and tested.
- Do not put an Exness password or API secret into this app.
- For automatic execution, the MQL5 EA must run in MT5 desktop on a Windows PC/VPS or use a supported bridge. Android alone cannot host the MT5 desktop EA.

## Build an APK with Android Studio
1. Install Android Studio on a Windows, Mac, or Linux computer.
2. Extract this project ZIP.
3. In Android Studio choose **Open**, then select the `MT5BotAndroid` folder (the folder containing `settings.gradle`).
4. Allow Gradle sync and install the Android SDK platform requested by the project (compile SDK 35).
5. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. When the build finishes, use the notification's **Locate** link. The debug APK is usually at `app/build/outputs/apk/debug/app-debug.apk`.
7. Transfer the APK to your Android phone, open it, and approve installation from that source if Android asks.

## Current features
- Dark mobile dashboard layout.
- EMA 200, RSI 14, ATR 14 strategy summary.
- ZAR illustrative balance and risk estimates.
- Editable display balance, risk percentage, and daily loss limit saved locally.
- Demo-first status and disabled execution control.

## Before automatic demo trading
A secure bridge/API and an MT5-side EA integration must be implemented. That bridge should authenticate the phone, expose account/position/status data, accept only whitelisted demo commands, validate risk server-side, log all actions, and explicitly reject live-account execution in the first release. Use HTTPS and never expose MT5 terminal credentials in the app.
