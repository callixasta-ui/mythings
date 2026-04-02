# MyThings 📦

**MyThings** is a simple, fully offline Android app for tracking borrowed items. Designed for non-tech users with a clean, minimalist UI — and a hidden developer control system for advanced management.

---

## 📱 Download

> Coming soon on GitHub Releases.

[⬇️ Download Latest APK](https://github.com/callixasta-ui/mythings/releases/latest)

---

## 🙋 Support

Having issues or suggestions? Open an issue on GitHub:

[🐛 Report a Bug / Request a Feature](https://github.com/callixasta-ui/mythings/issues)

Or contact us at: callixasta@gmail.com

---

## ✨ Features

### 👤 User Side
- Add borrow entries with name, item, notes, and optional image
- Mark items as returned with confirmation
- View borrowed and returned lists with search and sort
- Fully offline — no internet required

### 🛠️ Developer Side (Hidden)
- Hidden dev login triggered by tapping the copyright text 5 times in the Info modal
- View all entries including deleted ones with state badges
- Edit and soft delete entries
- Restore or permanently delete entries
- Manage developer account credentials

---

## 🏗️ Tech Stack

| Layer | Technology |
|---|---|
| Language | Kotlin |
| Architecture | MVVM |
| Database | Room (SQLite) |
| UI | XML Layouts + Material Components |
| Async | Kotlin Coroutines |
| Min SDK | API 27 (Android 8.1) |

---

## 📁 Project Structure

```
com.myapp.mythings/
  ├── database/        # Room entities, DAOs, AppDatabase
  ├── repository/      # EntryRepository, PreferencesRepository
  ├── screens/         # All Fragments and Activities
  ├── utils/           # Constants
  ├── viewmodel/       # EntryViewModel
  └── MyThingsApp.kt   # Application class
```

---

## 🚀 Getting Started (For Developers)

### Prerequisites
- Android Studio Hedgehog or later
- JDK 11
- Android device or emulator running API 27+

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/callixasta-ui/mythings.git
   ```
2. Open in Android Studio
3. Sync Gradle
4. Run on your device or emulator

### Default Dev Credentials
- **Username:** `admin`
- **Password:** `admin123`

> ⚠️ Change these immediately after first login via the Account page.

---

## 🔐 Dev Access

1. Open the app
2. Tap **Info** in the navigation drawer
3. Tap the copyright text **5 times**
4. Enter dev credentials

---

## 📋 Database Schema

### `entries` table
| Column | Type | Description |
|---|---|---|
| id | INTEGER | Primary key |
| borrowerName | TEXT | Who borrowed the item |
| itemName | TEXT | What was borrowed |
| notes | TEXT | Optional notes |
| imagePath | TEXT | Path to image in internal storage |
| borrowTimestamp | LONG | When it was borrowed |
| returnTimestamp | LONG | When it was returned |
| status | TEXT | BORROWED / RETURNED |
| state | TEXT | RAW / EDITED / DELETED |

### `account` table
| Column | Type | Description |
|---|---|---|
| username | TEXT | Dev username |
| passwordHash | TEXT | SHA-256 hashed password |
| birthday | TEXT | Dev birthday (YYYY-MM-DD) |

---

## 📜 License

Copyright © 2025 **Ctrl Alt Win**. All rights reserved.

See [LICENSE](LICENSE) for details.

---

## 👨‍💻 Developer

Built by **Ctrl Alt Win**
GitHub: [@callixasta](https://github.com/callixasta-ui)
