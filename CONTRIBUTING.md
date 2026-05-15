# Contributing to ForestGuard 🌿

First, thank you for your interest in contributing to ForestGuard! We're building this together to protect our forests and empower communities.

## How to Contribute

### 1. Reporting Issues
- **Check existing issues** first to avoid duplicates
- **Be descriptive**: Include steps to reproduce, expected vs actual behavior
- **Attach logs**: Include error messages and stack traces if applicable
- **Label appropriately**: Bug, Feature Request, Enhancement, etc.

### 2. Feature Requests
- **Describe the feature** and why it's needed
- **Provide use cases** and expected behavior
- **Suggest implementation** if you have ideas
- **Link to related issues** if applicable

### 3. Code Contributions

#### Before You Start
1. **Fork** the repository
2. **Clone** your fork: `git clone https://github.com/YOUR-USERNAME/Forest_Guard_Application.git`
3. **Create a feature branch**: `git checkout -b feature/your-feature-name`

#### Making Changes
1. **Follow code style** — Kotlin conventions and Android best practices
2. **Keep commits atomic** — One feature per commit
3. **Write meaningful commit messages**:
   ```
   Add: Camera integration with CameraX
   Fix: GPS location permission handling
   Refactor: Improve incident form validation
   ```

#### Testing Your Changes
- **Test locally** on emulator and/or physical device
- **Multiple devices** — Test on different Android versions and screen sizes
- **Edge cases** — Test offline mode, no GPS signal, poor network

#### Submitting a Pull Request
1. **Push** to your fork
2. **Create a Pull Request** with:
   - Clear title: "Add feature XYZ" or "Fix bug ABC"
   - Description of changes
   - Screenshots for UI changes
   - Linked issues: "Closes #123"
3. **Respond** to review comments promptly
4. **Ensure CI passes** before merge

### 4. Documentation
- **Update README** if adding features
- **Document code** with clear comments
- **Add screenshots** to `assets/screenshots/`
- **Update SCREENSHOTS.md** with new screen guides

## Code Style Guidelines

### Kotlin Conventions
```kotlin
// Use meaningful names
val incidentReportForm: IncidentReport

// Keep functions focused
fun submitIncidentReport(report: IncidentReport) {
    // Single responsibility
}

// Use data classes for models
data class Incident(
    val id: String,
    val type: IncidentType,
    val location: Location
)
```

### Jetpack Compose Best Practices
```kotlin
// Compose functions should be short and focused
@Composable
fun IncidentTypeSelector(
    onTypeSelected: (IncidentType) -> Unit
) {
    // Implementation
}

// Extract complex UI into separate composables
@Composable
private fun IncidentTypeCard(type: IncidentType) {
    // Card implementation
}
```

### Comments & Documentation
```kotlin
// ✅ Good: Explains WHY, not WHAT
// Camera permission is required for photo evidence
if (!hasCameraPermission) {
    requestCameraPermission()
}

// ❌ Avoid: Redundant comments
// Set the user variable
val user = getCurrentUser()
```

## Development Workflow

### Setting Up Development Environment
1. Android Studio (Electric Eel or newer)
2. JDK 11+
3. Android SDK API 34+

### Running Tests
```bash
# Unit tests
./gradlew testDebug

# UI tests
./gradlew connectedAndroidTest
```

### Building Release Variant
```bash
# Generate signed APK
./gradlew bundleRelease

# Debug APK
./gradlew assembleDebug
```

## Project Structure
```
app/src/main/
├── java/com/example/sahyadrisamrakshane/
│   ├── ui/
│   │   ├── screens/          ← Add new screens here
│   │   ├── components/       ← Reusable UI components
│   │   └── theme/            ← Theme and colors
│   ├── model/                ← Data models
│   ├── util/                 ← Utility functions
│   └── data/                 ← Mock/real data
└── res/                      ← Resources
```

## Commit Message Convention

```
[TYPE]: Brief description (50 chars max)

Longer explanation (72 chars per line)
- Point 1
- Point 2

Closes #123
```

**Types**: `Add`, `Fix`, `Refactor`, `Optimize`, `Docs`, `Style`, `Test`

## Review Process

1. **Automated Checks** — CI/CD pipeline runs tests
2. **Code Review** — Maintainers review code quality
3. **Feedback** — Address requested changes
4. **Approval** — PR gets approved and merged
5. **Deployment** — Changes go to main branch

## Getting Help

- **Confused about something?** Open a discussion
- **Need guidance?** Ask in issues or PRs
- **Want to chat?** Connect with maintainers

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Code of Conduct

Be respectful, inclusive, and constructive. We're all here to build something amazing for forest protection! 🌿

---

**Thank you for contributing to ForestGuard!**

Protecting Our Forests, Empowering Our Communities ❤️
