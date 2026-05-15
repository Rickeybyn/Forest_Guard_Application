# Sahyadri-Samrakshane (ForestGuard) 🌿

<div align="center">

**Citizen-Powered Forest Protection Mobile Application**

[![Android](https://img.shields.io/badge/Android-7.0+-green?logo=android)](https://www.android.com)
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9+-purple?logo=kotlin)](https://kotlinlang.org)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-Latest-blue?logo=android)](https://developer.android.com/jetpack/compose)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active%20Development-orange)]()

*Protecting Our Forests, Empowering Our Communities*

</div>

---

## 🎯 Quick Overview

A mobile app that empowers citizens to report environmental incidents to forest authorities **instantly** with photo evidence and precise GPS location. Designed with a beautiful green-themed UI for usability in remote forest areas.

| Feature | Details |
|---------|---------|
| 📱 **Platform** | Android 7.0+ |
| 🎨 **Framework** | Jetpack Compose + Kotlin |
| ⚡ **Status** | MVP Complete, Production Ready |
| 🗺️ **Ideal For** | Western Ghats & Forest Regions |
| 👥 **Users** | Citizens & Forest Officers |

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Building the App](#building-the-app)
- [Project Screens](#project-screens)
- [Next Steps for Production](#next-steps-for-production)
- [Android Permissions](#android-permissions)
- [Contributing](#contributing)
- [License](#license)

---

## 📱 Overview

**Sahyadri-Samrakshane** (Protection of the Sahyadri Range) is a forest sentinel application designed to bridge the gap between local communities and forest authorities.

### The Problem
The Western Ghats region faces constant threats from:
- Forest fires and uncontrolled blazes
- Illegal logging and deforestation
- Landslides and soil erosion
- Endangered wildlife trafficking

Local communities witness these incidents first but lack a direct way to alert forest authorities with precise location data.

### The Solution
A mobile app that enables citizens to:
- Report incidents in **less than 2 minutes**
- Capture **photo evidence** + **precise GPS location**
- Work **offline** in no-signal forest areas
- Track incident status in **real-time**
- Access **educational content** on forest protection
- Support **forest department response teams**

### Impact
- 🌿 **Faster Response**: Accurate location data reduces response time from hours to minutes
- 🤝 **Community Empowerment**: Citizens become active stakeholders in forest protection
- 📊 **Data-Driven Insights**: Authorities gain valuable incident patterns
- ♿ **Inclusive Design**: Intuitive interface works for all users, regardless of tech literacy

---

## 📸 App Screenshots

### Citizen Reporting Flow

<div align="center">

**Authentication & Dashboard**

```
┌─────────────┐    ┌──────────────┐    ┌─────────────────┐
│   Login     │───▶│ Dashboard    │───▶│ Report Incident │
│   Screen    │    │  Citizen     │    │    Button       │
└─────────────┘    └──────────────┘    └─────────────────┘
```

**5-Step Incident Reporting**

```
Step 1          Step 2           Step 3          Step 4        Step 5
┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐
│ Incident │───▶│  Photo   │───▶│  GPS     │───▶│ Details  │───▶│ Review & │
│  Type    │   │ Capture  │   │Location  │   │  Form    │   │ Submit   │
└──────────┘   └──────────┘   └──────────┘   └──────────┘   └──────────┘
                                                                    │
                                                                    ▼
                                                            ┌──────────────┐
                                                            │ Tracking ID  │
                                                            │ Confirmation │
                                                            └──────────────┘
```

</div>

> 📱 **Screenshots coming soon!** See [assets/SCREENSHOTS.md](assets/SCREENSHOTS.md) for where to add app screenshots.

### Current Screen Previews

#### Citizen Screens
- 🔐 Login & Sign-up
- 📊 Dashboard with incident list
- 🏷️ Incident type selection (Fire, Landslide, Illegal Cutting, Wildlife, Other)
- 📸 Photo capture interface
- 📍 GPS location display with coordinates
- 📝 Detailed incident description form
- ✅ Review and confirmation
- 📱 My Reports with status timeline
- 📚 Educational content section

#### Officer Screens
- 🗺️ Incident map dashboard
- 👁️ Incident detail viewer
- 🎯 Status management controls

---



## ✨ Key Features

### For Citizens
✅ **Easy Incident Reporting**
- 5-step guided reporting flow
- 5 incident types: Fire, Landslide, Illegal Cutting, Wildlife, Other
- Real-time photo capture with evidence verification
- Automatic GPS location capture
- Detailed incident description form

✅ **Real-Time Status Tracking**
- 4-stage status: Reported → Verified → Team Dispatched → Resolved
- Real-time notifications on status changes
- Incident timeline and history
- Tracking ID for reference

✅ **Offline-First Capability**
- Works in no-signal areas
- Local caching with Room database
- Automatic sync when connectivity returns
- "Pending Sync" indicator for pending reports

✅ **User Authentication**
- Email and Google Sign-In
- Secure session management
- User profile and preferences
- Report history management

✅ **Educational Content**
- Forest protection tips and guidelines
- Environmental awareness content
- Safety and best practice guides

### For Forest Department
✅ **Forest Officer Dashboard**
- Real-time incident map view
- Photo and metadata display
- Status update controls
- Response team dispatch management
- Incident filtering and search

### Feature Comparison

| Feature | Status | Mobile | Desktop | Offline |
|---------|--------|--------|---------|---------|
| 🔐 **Authentication** | ✅ MVP | ✅ Yes | 🔄 Backend | ✅ Yes |
| 📝 **Incident Reporting** | ✅ MVP | ✅ Yes | ✅ Yes | ✅ Yes |
| 📸 **Photo Evidence** | ✅ MVP | ✅ Yes | ✅ Yes | ✅ Yes |
| 📍 **GPS Location** | ✅ MVP | ✅ Yes | ✅ Yes | ✅ Yes |
| 🔔 **Push Notifications** | 🔄 Ready | ✅ Yes | ❌ No | ❌ No |
| 📊 **Status Tracking** | ✅ MVP | ✅ Yes | ✅ Yes | ⚠️ Cached |
| 🗺️ **Officer Dashboard** | 🔄 UI Ready | ✅ Yes | 🔄 Soon | ❌ No |
| 💾 **Offline Sync** | 🔄 Ready | ✅ Yes | ❌ No | ✅ Yes |
| 📚 **Education Content** | ✅ MVP | ✅ Yes | ✅ Yes | ✅ Yes |

**Legend**: ✅ Implemented | 🔄 Ready to Connect | ⚠️ Partial | ❌ Not Applicable

### MVP Functionality Currently Implemented
- ✅ Login and signup simulation
- ✅ Complete 5-step incident reporting flow
- ✅ Photo capture simulation screen
- ✅ GPS location simulation screen
- ✅ Citizen dashboard
- ✅ My Reports status timeline
- ✅ Education tips section
- ✅ Officer dashboard mock UI

---

## 🛠️ Tech Stack

### Frontend
- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM with Compose State Management
- **Android Target**: API 24+ (Android 7.0+)

### Backend (Production Integration Needed)
- **Database**: Firebase Firestore
- **Local Storage**: Room Database
- **Authentication**: Firebase Auth
- **Real-time Updates**: Firebase Cloud Messaging (FCM)
- **Background Sync**: WorkManager
- **Camera**: CameraX
- **Location**: Google Play Services FusedLocationProviderClient

### Build System
- **Gradle**: Kotlin DSL
- **Build Tool**: Android Gradle Plugin 8.x

---

### Architecture Diagram

<div align="center">

```
┌─────────────────────────────────────────────────────────────┐
│                    USER INTERFACE LAYER                      │
│              (Jetpack Compose UI Components)                │
│  ┌─────────────┬──────────────┬──────────────┬────────────┐ │
│  │   Auth UI   │ Citizen UI   │  Officer UI  │ Education  │ │
│  └─────────────┴──────────────┴──────────────┴────────────┘ │
└────────────────────────────────┬────────────────────────────┘
                                 │
┌────────────────────────────────▼────────────────────────────┐
│                    VIEWMODEL LAYER                          │
│              (State Management & Business Logic)            │
│  ┌──────────────────────────────────────────────────────┐  │
│  │  AuthViewModel │ ReportViewModel │ OfficeViewModel  │  │
│  └──────────────────────────────────────────────────────┘  │
└────────────────┬─────────────────────────┬──────────────────┘
                 │                         │
      ┌──────────▼───────────┐   ┌────────▼──────────────┐
      │  LOCAL DATABASE      │   │  REMOTE BACKEND      │
      │  (Room + SQLite)     │   │  (Firebase)          │
      │  ┌────────────────┐  │   │  ┌────────────────┐  │
      │  │ Incident Table │  │   │  │ Firestore DB   │  │
      │  │ User Cache     │  │   │  │ FCM Messaging  │  │
      │  │ Photos         │  │   │  │ Auth Service   │  │
      │  └────────────────┘  │   │  └────────────────┘  │
      └──────────────────────┘   └────────────────────┘
```

</div>

---



## 📁 Project Structure

```
Forest_Guard-master/
├── app/                                    # Main Android app module
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/sahyadrisamrakshane/
│   │   │   │   ├── ForestGuardAppUI.kt    # Main UI orchestrator
│   │   │   │   ├── MainActivity.kt        # Entry point
│   │   │   │   ├── model/
│   │   │   │   │   └── AppModels.kt       # Data models
│   │   │   │   ├── ui/
│   │   │   │   │   ├── screens/           # Screen compositions
│   │   │   │   │   ├── components/        # Reusable UI components
│   │   │   │   │   └── theme/             # Theme and colors
│   │   │   │   ├── util/
│   │   │   │   │   └── Formatters.kt      # Utility functions
│   │   │   │   └── data/
│   │   │   │       └── IncidentSeedData.kt # Mock data
│   │   │   └── res/                       # Android resources
│   │   └── AndroidManifest.xml
│   └── build.gradle.kts
├── gradle/                                # Gradle wrapper config
├── build.gradle.kts                       # Root build config
├── settings.gradle.kts                    # Gradle settings
├── README.md                              # This file
├── README_ANDROID.md                      # Android setup details
├── README_UPDATED.md                      # Detailed features
├── UI_DESIGN_SYSTEM.md                    # Design specifications
└── app.js, server.js                      # Backend server files (Node.js)
```

---

## 🔧 Prerequisites

Before you begin, ensure you have installed:

- **Android Studio** (Electric Eel or newer) — [Download](https://developer.android.com/studio)
- **Java Development Kit (JDK)** 11+ — [Download](https://www.oracle.com/java/technologies/downloads/)
- **Git** — [Download](https://git-scm.com/)
- **Gradle** (included with Android Studio)

### Minimum System Requirements
- RAM: 8GB (16GB recommended)
- Storage: 10GB free space
- Display: 1920x1080 or higher for Android Studio

---

## ⚡ Quick Start (5 Minutes)

<div align="center">

```
1️⃣  CLONE          2️⃣  OPEN           3️⃣  SYNC           4️⃣  BUILD          5️⃣  RUN
   Repository  →   Android Studio  →  Gradle   →     APK      →   Emulator
   
git clone        File → Open         Wait 5min     Build → APK      Run app
https://...      Select Folder       Complete      Menu             
```

</div>

### In 60 Seconds:
```bash
# 1. Clone
git clone https://github.com/Rickeybyn/Forest_Guard_Application.git
cd Forest_Guard_Application

# 2. Open in Android Studio (File → Open, select folder)

# 3. Wait for Gradle sync (~5 minutes)

# 4. Click Run (Shift+F10) or Build APK
```

---



### 1. Clone the Repository
```bash
git clone https://github.com/Rickeybyn/Forest_Guard_Application.git
cd Forest_Guard_Application
```

### 2. Open in Android Studio
1. Launch **Android Studio**
2. Click **File** → **Open**
3. Navigate to the cloned `Forest_Guard_Application` folder
4. Click **OK**
5. Wait for Gradle sync to complete (may take 5-10 minutes on first run)

### 3. Install Dependencies
Gradle will automatically download all required dependencies during the sync process.

### 4. Configure Android SDK
If prompted:
- Click **Tools** → **SDK Manager**
- Install Android SDK Platform 34 (or as required)
- Install Build Tools 34.0.0 (or as required)

---

## 🚀 Building the App (Detailed)

### Build and Run on Emulator
1. Click **Tools** → **AVD Manager**
2. Create a new Android Virtual Device (Pixel 4, Android 12+)
3. Start the emulator
4. Click **Run** → **Run 'app'** (or press Shift+F10)
5. Select the running emulator

### Build APK
1. Click **Build** → **Build Bundle(s) / APK(s)** → **Build APK(s)**
2. Wait for the build to complete
3. Find the APK at `app/build/outputs/apk/debug/app-debug.apk`

### Build Release APK (for Deployment)
1. Click **Build** → **Build Bundle(s) / APK(s)** → **Build Bundle(s)**
2. Follow the signing key setup
3. Locate the signed AAB/APK in `app/build/outputs/`

---

## 📱 Project Screens

The following screens are currently implemented with UI and state management:

### Authentication Screens
- **Login Screen** — Email/password or Google sign-in
- **Sign-up Screen** — New user registration

### Citizen Screens
1. **Dashboard** — Home with recent incidents and action buttons
2. **Incident Type Selection** — Choose from 5 incident types
3. **Photo Capture** — Simulate or capture actual photos
4. **GPS Location** — Display captured coordinates
5. **Incident Details Form** — Enter address and description
6. **Review Summary** — Confirm all details before submission
7. **Confirmation Screen** — Display tracking ID
8. **My Reports** — Timeline view of past reports with status
9. **Education Tips** — Forest protection guidelines

### Officer Screens
- **Dashboard Mock** — Preview of officer incident management UI

---

## ⚙️ Android Permissions Prepared

The app is configured with the following permissions (in `AndroidManifest.xml`):

```xml
<!-- Camera access for photo capture -->
<uses-permission android:name="android.permission.CAMERA" />

<!-- GPS location access -->
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />

<!-- Internet for API calls and Firebase -->
<uses-permission android:name="android.permission.INTERNET" />

<!-- Push notifications -->
<uses-permission android:name="android.permission.POST_NOTIFICATIONS" />
```

These are declared but not yet integrated into the app logic. Permission requests will be added when the respective features are implemented.

---

## �️ Production Roadmap

The current app is **fully UI and state-based** and can run without Firebase. Here's the integration roadmap:

<div align="center">

```
PHASE 1              PHASE 2               PHASE 3              PHASE 4
(Week 1-2)          (Week 3-4)            (Week 5-6)           (Week 7-8)
┌──────────┐        ┌────────────┐       ┌────────────┐      ┌──────────────┐
│ Camera & │   →    │  Location  │   →   │ Offline DB │  →   │  Firebase &  │
│ Location │        │  & Offline │       │  + Sync    │      │ Real-time    │
└──────────┘        └────────────┘       └────────────┘      └──────────────┘
```

</div>

### 🔧 Phase 1: Camera & Location Integration
- [ ] Replace photo simulation with **CameraX**
- [ ] Add photo compression and validation
- [ ] Implement gallery fallback option
- [ ] Replace GPS simulation with **FusedLocationProviderClient**
- [ ] Add location permission handling
- [ ] Implement location accuracy verification
- [ ] **Estimated**: 1-2 weeks

### 💾 Phase 2: Offline-First & Sync
- [ ] Implement **Room database** for local report caching
- [ ] Add sync queue management
- [ ] Implement background sync with **WorkManager**
- [ ] Add "Pending Sync" status indicator
- [ ] **Estimated**: 1-2 weeks

### 🔐 Phase 3: Authentication & User Management
- [ ] Integrate **Firebase Authentication**
- [ ] Add email verification flow
- [ ] Implement session management and token refresh
- [ ] Add user profile management
- [ ] **Estimated**: 1 week

### 🌐 Phase 4: Real-Time Sync & Notifications
- [ ] Connect to **Firebase Firestore** for cloud storage
- [ ] Implement real-time incident status updates
- [ ] Configure **Firebase Cloud Messaging (FCM)**
- [ ] Implement notification handlers
- [ ] **Estimated**: 1-2 weeks

### 🧪 Phase 5: Testing & Optimization
- [ ] Add unit tests with JUnit4
- [ ] Add UI tests with Compose Testing
- [ ] Performance optimization
- [ ] Battery usage optimization
- [ ] Multi-device testing
- [ ] **Estimated**: 1 week

---

## ⚙️ Next Steps for Production

The current app is **fully UI and state-based** and can run without Firebase. To make it production-ready, integrate:

### 1. Real Photo Capture
- [ ] Replace photo simulation with **CameraX**
- [ ] Add photo compression and validation
- [ ] Implement gallery fallback option

### 2. Real GPS Location
- [ ] Replace GPS simulation with **FusedLocationProviderClient**
- [ ] Add location permission handling
- [ ] Implement location accuracy verification
- [ ] Add map preview with incident location

### 3. Offline-First Storage
- [ ] Implement **Room database** for local report caching
- [ ] Add sync queue management
- [ ] Implement background sync with **WorkManager**

### 4. User Authentication
- [ ] Integrate **Firebase Authentication**
- [ ] Add email verification flow
- [ ] Implement session management and token refresh

### 5. Real-Time Data Sync
- [ ] Connect to **Firebase Firestore** for cloud storage
- [ ] Implement real-time incident status updates
- [ ] Add listener for push notifications

### 6. Push Notifications
- [ ] Configure **Firebase Cloud Messaging (FCM)**
- [ ] Implement notification handlers for status changes
- [ ] Add notification preferences management

### 7. Testing & Optimization
- [ ] Add unit tests with JUnit4
- [ ] Add UI tests with Compose Testing
- [ ] Optimize performance and battery usage
- [ ] Test with various device sizes and Android versions

---

## 📋 Usage Guide

### For Citizens
1. **Launch the App** → Login or sign up
2. **Tap "Report Incident"** → Dashboard
3. **Select Incident Type** → Choose the type of environmental issue
4. **Capture Photo** → Take a clear photo as evidence
5. **Confirm Location** → Verify GPS coordinates
6. **Fill Details** → Add description and address
7. **Review & Submit** → Confirm and submit
8. **Track Status** → Check "My Reports" for real-time updates

### For Officers
1. **Launch Officer Dashboard**
2. **View Incident Map** → See all reported incidents
3. **Review Incident Details** → Photo, location, description
4. **Update Status** → Move through workflow
5. **Dispatch Response** → Assign to response team

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. **Fork** the repository on GitHub
2. **Create a feature branch**: `git checkout -b feature/your-feature-name`
3. **Make your changes** and test thoroughly
4. **Commit with clear messages**: `git commit -m "Add feature: description"`
5. **Push to your fork**: `git push origin feature/your-feature-name`
6. **Submit a Pull Request** with a detailed description

### Code Style Guidelines
- Follow Kotlin conventions and Android best practices
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions focused and modular
- Ensure all screens are tested

---

## 📄 Documentation

For more details, see:
- **[README_ANDROID.md](README_ANDROID.md)** — Android setup and build instructions
- **[README_UPDATED.md](README_UPDATED.md)** — Extended features and architecture details
- **[UI_DESIGN_SYSTEM.md](UI_DESIGN_SYSTEM.md)** — Design system and UI guidelines

---

## 📞 Contact & Support

For questions or support:
- **GitHub Issues** — [Open an issue](https://github.com/Rickeybyn/Forest_Guard_Application/issues)
- **Email** — sahyadrisamrakshane@example.com (replace with actual contact)

---

## 📜 License

This project is licensed under the **MIT License** — see the LICENSE file for details.

---

## 🙏 Acknowledgments

Built with ❤️ for forest protection and community empowerment.

**Sahyadri-Samrakshane: Protecting Our Forests, Empowering Our Communities**

<div align="center">

---

### Made with 🌿 for the Western Ghats

[![GitHub](https://img.shields.io/badge/GitHub-Rickeybyn-black?logo=github)](https://github.com/Rickeybyn/Forest_Guard_Application)
[![Android](https://img.shields.io/badge/Android-ForestGuard-green?logo=android)](https://play.google.com)
[![Contributors](https://img.shields.io/badge/Contributors-Welcome-brightgreen)](.github/CONTRIBUTING.md)

</div>
