# Development Guide 🛠️

This guide helps you set up your development environment and get started contributing to ForestGuard.

## 📋 Prerequisites

### Required
- **Android Studio**: Electric Eel or newer — [Download](https://developer.android.com/studio)
- **JDK 11+**: [Download](https://www.oracle.com/java/technologies/downloads/)
- **Git**: [Download](https://git-scm.com)
- **RAM**: Minimum 8GB (16GB recommended)
- **Storage**: 10GB+ free space

### Optional (for real device testing)
- Android physical device with USB debugging enabled
- Android emulator (comes with Android Studio)

## 🚀 Getting Started

### 1. Clone & Setup
```bash
# Clone repository
git clone https://github.com/Rickeybyn/Forest_Guard_Application.git
cd Forest_Guard_Application

# Open in Android Studio
# File → Open → Select folder
```

### 2. Wait for Gradle Sync
- First sync takes 5-10 minutes
- Downloads dependencies and builds cache
- Android Studio shows progress

### 3. Configure SDK (if needed)
```
Tools → SDK Manager
→ Android SDK Platforms → Android 14 (API 34)
→ SDK Tools → Build Tools 34.0.0
→ Install
```

### 4. Create Virtual Device (for emulator)
```
Tools → AVD Manager
→ Create Virtual Device
→ Select "Pixel 5" or "Pixel 6"
→ Select Android 12 or higher
→ Finish
```

## ▶️ Running the App

### On Emulator
1. **Start emulator**: `Tools → AVD Manager → Play button`
2. **Run app**: `Run → Run 'app'` (or Shift+F10)
3. **Select emulator** from device list
4. **Wait** for deployment (1-2 minutes)

### On Physical Device
1. **Enable USB Debugging**: `Settings → Developer Options → USB Debugging`
2. **Connect** device via USB cable
3. **Trust** computer when prompted
4. **Run app**: `Run → Run 'app'` (or Shift+F10)
5. **Select device** from list

## 📦 Project Structure

```
Forest_Guard_Application/
├── app/                           # Android app module
│   ├── src/
│   │   └── main/
│   │       ├── java/com/example/sahyadrisamrakshane/
│   │       │   ├── MainActivity.kt                  # Entry point
│   │       │   ├── ForestGuardAppUI.kt             # Main UI
│   │       │   ├── ui/
│   │       │   │   ├── screens/                    # Screen components
│   │       │   │   ├── components/                 # Reusable widgets
│   │       │   │   └── theme/                      # Colors, typography
│   │       │   ├── model/
│   │       │   │   └── AppModels.kt                # Data models
│   │       │   ├── data/
│   │       │   │   └── IncidentSeedData.kt        # Mock data
│   │       │   └── util/
│   │       │       └── Formatters.kt               # Utilities
│   │       └── AndroidManifest.xml
│   └── build.gradle.kts
├── gradle/                        # Gradle configuration
├── build.gradle.kts              # Root build config
├── settings.gradle.kts           # Gradle settings
└── README.md                     # Project documentation
```

## 🔍 Understanding the Code

### UI Structure (Jetpack Compose)
```
ForestGuardAppUI.kt (Main composable)
├── AuthScreens.kt
│   ├── LoginScreen()
│   └── SignUpScreen()
├── HomeScreens.kt
│   ├── CitizenDashboard()
│   └── OfficerDashboard()
├── ReportFlowScreens.kt
│   ├── SelectIncidentType()
│   ├── CapturePhoto()
│   ├── CaptureLocation()
│   ├── IncidentDetails()
│   ├── ReviewIncident()
│   └── ConfirmationScreen()
└── StatusScreens.kt
    └── MyReports()
```

### State Management
```kotlin
// Example: How screens manage state
@Composable
fun SelectIncidentType(onTypeSelected: (IncidentType) -> Unit) {
    var selectedType by remember { mutableStateOf<IncidentType?>(null) }
    
    LazyVerticalGrid(...) {
        items(IncidentType.values()) { type ->
            // UI for type
        }
    }
}
```

## ⚙️ Gradle Build Configuration

### Key build.gradle.kts files

**Root** (`build.gradle.kts`):
```kotlin
plugins {
    id("com.android.application") version "8.x.x"
    kotlin("android") version "1.9.x"
}
```

**App** (`app/build.gradle.kts`):
```kotlin
android {
    compileSdk = 34
    
    defaultConfig {
        applicationId = "com.example.sahyadrisamrakshane"
        minSdk = 24
        targetSdk = 34
    }
}

dependencies {
    // Jetpack Compose
    implementation("androidx.compose.ui:ui:1.5.x")
    
    // Firebase (when integrated)
    implementation("com.google.firebase:firebase-firestore:x.x.x")
}
```

## 🧪 Testing

### UI Testing with Compose
```kotlin
@RunWith(ComposeTestRule::class)
class ExampleTest {
    @get:Rule
    val composeTestRule = createComposeRule()
    
    @Test
    fun testLoginButton() {
        composeTestRule.setContent {
            LoginScreen()
        }
        
        composeTestRule.onNodeWithText("Login").performClick()
    }
}
```

### Running Tests
```bash
# All unit tests
./gradlew test

# All instrumented tests
./gradlew connectedAndroidTest

# Specific test
./gradlew testDebugUnitTest
```

## 🐛 Debugging

### Android Studio Debugger
1. **Set breakpoint**: Click line number
2. **Run debug**: `Run → Debug 'app'` (Shift+F9)
3. **Step through**: Use F10/F11 or debug toolbar

### Logcat
```
View → Tool Windows → Logcat

// Add logs in code
Log.d("ForestGuard", "User logged in: $userId")
Log.e("ForestGuard", "Error: $errorMessage", exception)
```

### Common Debug Tasks
```bash
# View logs from last hour
./gradlew logcat -s "ForestGuard" --tail=100

# Clear app data (factory reset)
adb shell pm clear com.example.sahyadrisamrakshane

# Reinstall app
./gradlew uninstallDebug assembleDebug installDebug
```

## 📱 Building & Installation

### Debug APK (for testing)
```bash
./gradlew assembleDebug
# Output: app/build/outputs/apk/debug/app-debug.apk
```

### Release APK (for distribution)
```bash
./gradlew assembleRelease
# Requires signing key setup
# Output: app/build/outputs/apk/release/app-release.apk
```

### Install APK manually
```bash
adb install app/build/outputs/apk/debug/app-debug.apk
```

## 🔧 Useful Commands

```bash
# Clean build
./gradlew clean build

# Rebuild without cache
./gradlew --no-build-cache assembleDebug

# List all tasks
./gradlew tasks

# Check dependencies
./gradlew dependencies

# Format code (if configured)
./gradlew spotlessApply

# Static analysis
./gradlew lint
```

## 📚 Resources

- **Jetpack Compose**: https://developer.android.com/jetpack/compose
- **Android Architecture**: https://developer.android.com/guide/architecture
- **Kotlin**: https://kotlinlang.org/docs/
- **Firebase**: https://firebase.google.com/docs/android/setup
- **Android Best Practices**: https://developer.android.com/guide

## 🆘 Troubleshooting

### Gradle Sync Fails
```bash
# Clear gradle cache
rm -rf ~/.gradle/caches

# Update gradle wrapper
./gradlew wrapper --gradle-version=8.x.x
```

### Emulator Slow
- Allocate more RAM in AVD settings
- Enable Hardware Acceleration (KVM on Linux, HyperV on Windows)
- Use x86_64 architecture

### Build Error: "Duplicate class"
- Clean: `./gradlew clean`
- Invalidate caches: `File → Invalidate Caches`

### APK Installation Fails
```bash
# Uninstall first
adb uninstall com.example.sahyadrisamrakshane

# Clear app storage
adb shell pm clear com.example.sahyadrisamrakshane
```

## 📞 Getting Help

- **Documentation**: See [README.md](README.md)
- **Issues**: [GitHub Issues](https://github.com/Rickeybyn/Forest_Guard_Application/issues)
- **Contributing**: See [CONTRIBUTING.md](CONTRIBUTING.md)

---

Happy coding! 🌿
