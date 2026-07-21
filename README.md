# CryptoTracker 📈

CryptoTracker is a native Android app built with Kotlin and Jetpack Compose for tracking crypto market data from the [CoinCap API](https://docs.coincap.io/).

## What it currently does

- Loads and displays live crypto assets (rank, name, symbol, market cap, price, and 24h change).
- Uses an adaptive list/detail layout that works on phones and larger screens.
- Shows a detailed coin screen with:
  - coin icon and metadata
  - market cap, current price, and 24h absolute change
  - an interactive line chart using recent historical price data (6h interval)
- Handles API/network errors and surfaces user-friendly messages.

## Tech stack

- **Language**: Kotlin
- **UI**: Jetpack Compose + Material 3 Adaptive Navigation
- **Architecture**: Layered (data/domain/presentation)
- **Dependency Injection**: Koin
- **Networking**: Ktor Client + Kotlinx Serialization + Coroutines
- **Build**: Gradle Kotlin DSL

## Project structure

- `/app/src/main/java/com/plcoding/cryptotracker/crypto/data` – API DTOs, mappers, remote datasource
- `/app/src/main/java/com/plcoding/cryptotracker/crypto/domain` – domain models and datasource contract
- `/app/src/main/java/com/plcoding/cryptotracker/crypto/presentation` – Compose UI, ViewModel, and UI models
- `/app/src/main/java/com/plcoding/cryptotracker/core` – networking/result utilities and shared presentation helpers
- `/app/src/main/java/com/plcoding/cryptotracker/di` – Koin module definitions

## Getting started

### Requirements

- Android Studio (latest stable recommended)
- Android SDK with **minSdk 26** support

### Run the app

1. Clone this repository.
2. Open the project root folder in Android Studio.
3. Sync Gradle.
4. Run the `app` configuration on an emulator or Android device.

## Notes

- The app uses `https://api.coincap.io/v2/` as its base API URL.
- Internet permission is required and already configured in the Android manifest.