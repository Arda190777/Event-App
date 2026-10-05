# Event Scout

**A Flutter event-discovery app with local booking simulations.**

Event Scout combines Ticketmaster Discovery API event data with a seeded SQLite catalogue. It demonstrates mobile navigation, HTTP/JSON integration, local persistence, account screens and event administration.

## Features

- Browse events and view venue, date, image and available price data.
- Fetch Ticketmaster events when an API key is configured.
- Retain seeded local events when external data is unavailable.
- Register/login locally and use administrative event-management screens.
- Simulate a ticket booking and view its local confirmation/history.

**Stack:** Flutter · Dart 3 · Material UI · SQLite/sqflite · HTTP

> This is an educational prototype. Checkout writes a local booking record; it does not charge a card or purchase a Ticketmaster ticket. Use fictional data in the payment form. Local account storage is separate from production authentication.

## Run locally

Install Flutter with a compatible Dart 3 SDK and configure an Android device/emulator or iOS development environment.

```powershell
git clone https://github.com/Arda190777/Event-App.git
cd Event-App
flutter pub get
flutter run
```

The app works with seeded demo events without an API key. For API-backed discovery, pass your development key using Flutter build-time configuration:

```powershell
flutter run --dart-define=TICKETMASTER_API_KEY=YOUR_DEVELOPMENT_KEY
```

Keep actual keys out of committed files. Build-time client configuration is embedded in the app binary; a production integration needs appropriate provider restrictions and a server-side boundary.

## Verify

```powershell
flutter analyze
```

No dedicated Dart test suite is currently included. Platform scaffold test files do not establish end-to-end app acceptance.

## Code map

```text
lib/models/             Event and ticket models
lib/screens/            Discovery, local accounts, admin and booking UI
lib/services/           SQLite persistence and Ticketmaster HTTP integration
lib/current_user.dart   Local user context
lib/main.dart           App entry and platform setup
```

The repository includes desktop/mobile platform scaffolding. SQLite and platform behavior must be verified per target; the presence of a web scaffold does not establish working browser persistence. No standalone license file is currently included.
