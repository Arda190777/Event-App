# 🎟️ Event Scout

A Flutter-based event discovery and ticket booking app that integrates with the **Ticketmaster API** to browse real events, purchase tickets, and manage bookings — all from a clean, modern mobile interface.

---

## Features

- 🔐 User registration & login (with role-based access)
- 🎭 Browse real events fetched from the Ticketmaster API
- 📍 Event detail pages with location, date, image, and price
- 🛒 Ticket purchasing with booking confirmation
- 🎫 View purchased tickets history
- 🛠️ Admin dashboard to add, edit, and delete events
- 💾 Local SQLite database (offline-friendly with seeded events)

---

## Screenshots

> *(Add screenshots here)*

---

## Getting Started

### Prerequisites

- [Flutter SDK](https://flutter.dev/docs/get-started/install) (Dart ≥ 3.0.0)
- Android emulator / physical device / iOS simulator

### Installation

```bash
git clone https://github.com/YOUR_USERNAME/event-scout-app.git
cd event-scout-app
flutter pub get
flutter run
```

---

## Demo Credentials

| Role  | Email             | Password |
|-------|-------------------|----------|
| Admin | admin@gmail.com   | 1234     |
| User  | Register yourself | —        |

---

## Tech Stack

| Layer       | Technology                        |
|-------------|-----------------------------------|
| Framework   | Flutter / Dart                    |
| Database    | SQLite via `sqflite`              |
| API         | Ticketmaster Discovery API v2     |
| HTTP Client | `http` package                    |
| UI          | Material 3                        |

---

## Project Structure

```
lib/
├── main.dart
├── current_user.dart
├── models/
│   ├── event_model.dart
│   └── tickets.dart
├── screens/
│   ├── splash_screen.dart
│   ├── login_screen.dart
│   ├── register_screen.dart
│   ├── home_screen.dart
│   ├── event_detail_screen.dart
│   ├── payment_screen.dart
│   ├── confirmation_screen.dart
│   ├── purchased_tickets_screen.dart
│   ├── admin_dashboard.dart
│   └── add_event_screen.dart
└── services/
    ├── database_helper.dart
    └── ticketmaster_service.dart
```

---

## License

This project was built for educational purposes.
