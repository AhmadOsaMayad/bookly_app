# 📚 Bookly App

A modern Flutter app for discovering, browsing, and searching books using the Google Books API.

---

## ✨ Features

- Splash screen with smooth transitions
- Home screen with:
  - **Featured books**
  - **Newest books**
- Book details screen
- Similar books recommendations
- Search books by keyword
- Cached network images
- Loading placeholders (Shimmer)
- Clean error handling for API/network issues

---

## 🧱 Architecture

This project follows a **feature-first + layered architecture**:

- `lib/core/`  
  Shared utilities (API service, routing, theming, errors, reusable widgets)
- `lib/features/home/`  
  Home feature (data repos, models, cubits, views)
- `lib/features/search/`  
  Search feature (repo, cubit, views)
- `lib/features/splash/`  
  Splash feature

State management is built with **BLoC/Cubit** (`flutter_bloc`), and dependencies are wired using **GetIt** service locator.

---

## 🛠 Tech Stack

- **Flutter** / **Dart**
- **BLoC/Cubit** for state management
- **Dio** for networking
- **GetIt** for dependency injection
- **GoRouter** for navigation
- **Dartz** (`Either`) for functional error handling
- **cached_network_image** and **shimmer** for UI/UX improvements

---

## 🌐 API

The app uses the **Google Books API**:

- Base URL: `https://www.googleapis.com/books/v1/`
- Main endpoint used: `volumes`

Examples used in the app:
- Featured books query (Love)
- Newest books query (novel)
- Search query from user input

---

## 📁 Project Structure

```text
lib/
├─ core/
│  ├─ errors/
│  ├─ utils/
│  └─ widgets/
├─ features/
│  ├─ home/
│  │  ├─ data/
│  │  └─ presentation/
│  ├─ search/
│  │  ├─ data/
│  │  └─ presentation/
│  └─ splash/
└─ main.dart
```

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK compatible with `sdk: ^3.7.0`
- Dart SDK (included with Flutter)
- Android Studio / VS Code + Flutter extensions
- Emulator or physical device

### Installation

```bash
git clone https://github.com/AhmadOsaMayad/bookly_app.git
cd bookly_app
flutter pub get
```

### Run the App

```bash
flutter run
```

---

## 🧪 Quality Checks

Run static analysis:

```bash
flutter analyze
```

Run tests:

```bash
flutter test
```

> Note: In environments without Flutter installed, these commands will fail until Flutter is available in PATH.

---

## 📦 Build

```bash
flutter build apk      # Android
flutter build ios      # iOS
flutter build web      # Web
flutter build windows  # Windows
flutter build macos    # macOS
flutter build linux    # Linux
```

---

## 🎨 Assets & Fonts

- Images: `assets/images/`
- Custom fonts:
  - `GT Sectra Fine`
  - `Montserrat`

---

## 📌 Notes

- The app is configured as a private project (`publish_to: none`).
- App icon generation is configured with `flutter_launcher_icons`.

---

## 🤝 Contributing

Contributions are welcome. Please open an issue first for major changes, then submit a pull request.

---

## 📄 License

No license file is currently specified in this repository.
