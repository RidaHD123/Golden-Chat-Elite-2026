# Golden Chat Elite 🌟

A sovereign social platform combining the best of Substack, Wire, and Facebook — with robust local persistence and secure AI services powered by Gemini.

## Features

- 💬 Secure real-time chat (Wire-style)
- 📰 Publishing & newsletters (Substack-style)
- 👥 Social feed & community (Facebook-style)
- 🤖 AI assistant via Gemini (Firebase AI)
- 🗄️ Local persistence with Room database
- 🔒 Firebase App Check (reCAPTCHA)

## Requirements

- [Android Studio](https://developer.android.com/studio) (latest stable)
- Android SDK 24+
- A [Gemini API key](https://aistudio.google.com/app/apikey)

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/golden-chat-elite.git
cd golden-chat-elite
```

### 2. Configure your API key

Create a `.env` file in the **root of the project** (next to `build.gradle.kts`):

```env
GEMINI_API_KEY=your_actual_api_key_here
```

> ⚠️ Never commit your `.env` file — it is already in `.gitignore`.

### 3. Open in Android Studio

1. Open Android Studio
2. Select **File → Open** and choose the project directory
3. Wait for Gradle sync to complete

### 4. Run the app

- Connect a physical device or start an emulator
- Click **Run ▶** or press `Shift+F10`

## Project Structure

```
app/
├── src/
│   ├── main/
│   │   ├── java/com/example/   # Kotlin source code
│   │   └── res/                # Resources
│   ├── test/                   # Unit tests
│   └── androidTest/            # Instrumentation tests
├── build.gradle.kts
gradle/
└── libs.versions.toml          # Version catalog
```

## Tech Stack

| Layer | Technology |
|-------|-----------|
| UI | Jetpack Compose + Material 3 |
| Navigation | Navigation Compose |
| Database | Room |
| Networking | Retrofit + OkHttp + Moshi |
| AI | Firebase AI (Gemini) |
| Images | Coil |
| Security | Firebase App Check |

## Build Variants

| Variant | Description |
|---------|-------------|
| `debug` | Development build with debug signing |
| `release` | Production build — requires keystore env vars |

For release builds, set these environment variables:
```
KEYSTORE_PATH=/path/to/your.jks
STORE_PASSWORD=your_store_password
KEY_PASSWORD=your_key_password
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](LICENSE)
