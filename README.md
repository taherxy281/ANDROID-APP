# YouTube Music Player

একটি advanced Android music player app যা YouTube থেকে music fetch করে এবং offline download সুবিধা প্রদান করে।

## Features

✨ **Core Features:**
- 🎵 YouTube থেকে music খুঁজুন এবং চালান
- 🎧 Background playback সাপোর্ট
- 📥 Music offline download করুন
- ❤️ Favorite songs save করুন
- 📋 Playlist তৈরি করুন এবং পরিচালনা করুন
- 🔍 Advanced search এবং filter
- 📊 Music metadata (title, description, duration, etc.)
- 🖼️ Thumbnail এবং album art
- 📱 Material Design UI
- 🔐 Secure এবং সুরক্ষিত

## Technical Stack

### Architecture
- **MVVM** Architecture Pattern
- **Coroutines** for async operations
- **Flow** for reactive programming

### Libraries & Tools
- **Dagger 2** - Dependency Injection
- **Room Database** - Local storage
- **Retrofit 2** - REST API calls
- **ExoPlayer/Media3** - Audio playback
- **Glide** - Image loading
- **OkHttp** - Networking
- **Timber** - Logging
- **DataStore** - Preferences

### Build & CI/CD
- **GitHub Actions** - Automated build & test
- **Gradle Kotlin DSL** - Build configuration
- **ProGuard** - Code obfuscation & optimization

## Project Structure

```
app/src/
├── main/
│   ├── java/com/musicplayer/youtube/
│   │   ├── MusicPlayerApplication.kt
│   │   ├── di/                  # Dependency Injection modules
│   │   ├── data/
│   │   │   ├── api/            # API Service
│   │   │   ├── db/             # Room Database & DAOs
│   │   │   ├── model/          # Data models
│   │   │   └── repository/     # Data repositories
│   │   ├── service/            # Background services
│   │   ├── receiver/           # Broadcast receivers
│   │   └── ui/                 # Activities & UI components
│   └── res/                    # Resources
└── test/                       # Unit tests
```

## Installation & Setup

### Prerequisites
- Java 11+
- Android SDK 34
- Gradle 8.0+

### Build Steps

1. **Clone Repository**
```bash
git clone https://github.com/taherxy281/ANDROID-APP.git
cd ANDROID-APP
```

2. **Build Debug APK**
```bash
./gradlew assembleDebug
```

3. **Build Release APK**
```bash
./gradlew assembleRelease
```

4. **Run Tests**
```bash
./gradlew test
```

5. **Run Lint**
```bash
./gradlew lint
```

## GitHub Actions Workflow

Automated build process যা নিম্নলিখিত কাজ করে:
- ✅ Code compilation
- ✅ Unit tests
- ✅ Lint analysis
- ✅ APK generation
- ✅ Artifact upload

### Trigger Conditions
- Push to `main` or `develop` branch
- Pull requests
- Manual workflow dispatch

## Permissions Required

```xml
<!-- Internet -->
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<!-- Storage -->
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.MANAGE_EXTERNAL_STORAGE" />

<!-- Audio -->
<uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
<uses-permission android:name="android.permission.RECORD_AUDIO" />

<!-- System -->
<uses-permission android:name="android.permission.WAKE_LOCK" />
<uses-permission android:name="android.permission.FOREGROUND_SERVICE" />
```

## Testing

### Unit Tests
```bash
./gradlew testDebugUnitTest
```

### All Tests
```bash
./gradlew test
```

### Test Coverage
```bash
./gradlew testDebugUnitTest jacocoTestDebugUnitTestReport
```

## Debugging

### Enable Logging
- `BuildConfig.DEBUG` automatically enables Timber logging
- Network requests logged via OkHttp interceptor

### Proguard Rules
- Custom rules in `app/proguard-rules.pro`
- Preserves necessary classes while optimizing others

## Security Features

✅ **SSL/TLS Encryption** - All network communications
✅ **ProGuard Obfuscation** - Code protection
✅ **Secure Storage** - Encrypted preferences
✅ **Input Validation** - Safe user inputs
✅ **Permission Handling** - Runtime permissions

## Troubleshooting

### Build Issues
```bash
# Clean build
./gradlew clean build

# Rebuild with fresh cache
./gradlew clean build --no-build-cache
```

### Gradle Issues
```bash
# Update gradle wrapper
./gradlew wrapper --gradle-version latest

# Regenerate gradle files
rm -rf .gradle build
./gradlew build
```

## Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## Development Guidelines

- Follow **Kotlin conventions**
- Use **coroutines** for async operations
- Write **unit tests** for new features
- Update **documentation**
- Follow **SOLID principles**

## License

এই project এর জন্য appropriate license নির্ধারণ করুন।

## Support

Issues বা questions থাকলে GitHub Issues এ create করুন।

## Changelog

### v1.0.0
- Initial release
- YouTube music search & playback
- Offline download
- Playlist management
- Background playback

## Performance Optimization

- 🚀 Lazy loading for large lists
- 📦 Image caching with Glide
- 🔄 Database pagination
- ⚡ Efficient coroutine management
- 💾 Memory-conscious design

---

**Made with ❤️ by taherxy281**
