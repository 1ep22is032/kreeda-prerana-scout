# Kreeda-Prerana Scout

Kreeda-Prerana Scout is a Kotlin-based Android application for grassroots sports talent tracking. It is designed for physical education teachers, school coaches, and local scouts who need a simple offline-first tool to record student athletes, log trials, review performance signals, and share scouting reports.

The app is built as a native Android project and can be opened directly in Android Studio.

---

## Table of Contents

- [Overview](#overview)
- [Core Features](#core-features)
- [Screens Included](#screens-included)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [How to Run](#how-to-run)
- [App Workflow](#app-workflow)
- [Data Storage](#data-storage)
- [Design System](#design-system)
- [Troubleshooting](#troubleshooting)
- [Future Improvements](#future-improvements)

---

## Overview

The purpose of this application is to help schools identify and track promising young athletes using basic measurable performance data.

Teachers and coaches can:

- Create athlete profiles.
- Add an entire class roster using batch entry.
- Record sports trial results.
- Use a stopwatch for timed trials.
- View leaderboard-style rankings.
- Generate simple coaching insights.
- Share scouting reports as text.
- View the supplied UI reference screens inside the app.

The current implementation focuses on being lightweight, offline-friendly, and easy to run in Android Studio.

---

## Core Features

### 1. Dashboard

The dashboard gives a quick summary of the current scouting data.

It shows:

- Total athletes.
- Total trials.
- Number of sports represented.
- Recent trial records.
- Top talent signals based on saved results.

### 2. Athlete Profiles

The athlete profile screen allows users to create student athlete records.

Each athlete includes:

- Name
- Age
- Class or section
- School name
- Primary sport

Saved athletes are shown in a roster list.

### 3. Batch Entry

The batch entry screen allows a teacher to paste many student names at once.

This is useful when creating an entire class roster quickly. The user enters:

- One student name per line
- Class or section
- School name
- Default sport

The app creates multiple athlete records in one action.

### 4. High Precision Trial Logger

The trial logger supports both timed and manually entered results.

It includes:

- Athlete selection
- Event selection
- Stopwatch timer
- Manual result entry
- Trial saving

Supported sample events:

- 100m Sprint
- Long Jump
- Shot Put
- Yo-Yo Test
- Vertical Jump

### 5. Leaderboard

The leaderboard ranks athletes based on their strongest recorded benchmark.

This helps coaches quickly identify students who may deserve closer observation or additional trials.

### 6. Coach Insights

The insights screen generates simple rule-based coaching notes from the locally stored trial data.

Example insight types:

- Sprint potential
- Power event potential
- Need for more testing data
- Consistency signals

### 7. Export Report

The export screen creates a shareable text report.

The report includes:

- Total athletes
- Total trials
- Ranked athlete results

The report can be shared using Android's native share sheet.

### 8. Provided Screens Gallery

The app includes a dedicated `Screens` tab that displays the design reference screens supplied in the project zip file.

This makes it easy to compare the implemented Android app with the original visual direction.

---

## Screens Included

The following supplied screens were added as Android drawable resources:

- Athlete Discovery
- Performance Dashboard
- High Precision Trial Logger
- Batch Entry
- School Leaderboard
- Coach Insights
- Export Report Sharing
## Attachments
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 52 PM" src="https://github.com/user-attachments/assets/4a34db79-7f40-4117-a95a-5b19346f3c31" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 52 PM (1)" src="https://github.com/user-attachments/assets/44b1b114-0774-438f-b6af-08a90c1afda2" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 52 PM (2)" src="https://github.com/user-attachments/assets/12abe403-cdbe-4392-9f4f-5eee78316073" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 52 PM (3)" src="https://github.com/user-attachments/assets/07074c75-0876-4b17-93e6-00072517fb67" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 53 PM" src="https://github.com/user-attachments/assets/ba4063f1-c365-4065-8180-d08b67414823" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 53 PM (1)" src="https://github.com/user-attachments/assets/9e0f3fab-e31e-4cda-829a-4fcdb57b3891" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 53 PM (2)" src="https://github.com/user-attachments/assets/884d39cb-10f9-43ce-934b-e070735e24e7" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 54 PM" src="https://github.com/user-attachments/assets/6c9b6915-8168-4c05-be02-1c1abffa6933" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 54 PM (1)" src="https://github.com/user-attachments/assets/e6505525-a061-4ee7-be9c-a6ac9a3575b5" />
<img width="720" height="1600" alt="WhatsApp Image 2026-05-13 at 10 25 54 PM (2)" src="https://github.com/user-attachments/assets/8602b75f-7288-4b52-a504-03f6089bd898" />


Source design archive:

```text
stitch_athlete_performance_scouting_suite (7).zip
```

Extracted screen assets are stored in:

```text
app/src/main/res/drawable/
```

---

## Technology Stack

| Area | Technology |
| --- | --- |
| Platform | Android |
| Language | Kotlin |
| UI Approach | Native Android views created in Kotlin |
| Minimum SDK | API 26, Android 8.0 |
| Target SDK | API 34, Android 14 |
| Build System | Gradle Kotlin DSL |
| Local Storage | SharedPreferences with JSON |
| Architecture Style | Activity + Repository-style local data layer |
| App Icon | Adaptive launcher icon |

---

## Project Structure

```text
project/
├── app/
│   ├── build.gradle.kts
│   └── src/
│       └── main/
│           ├── AndroidManifest.xml
│           ├── java/
│           │   └── com/
│           │       └── mindmatrix/
│           │           └── kreedaprerana/
│           │               └── MainActivity.kt
│           └── res/
│               ├── drawable/
│               │   ├── ic_launcher_foreground.xml
│               │   ├── screen_athlete_discovery.png
│               │   ├── screen_batch_entry.png
│               │   ├── screen_coach_insights.png
│               │   ├── screen_export_report.png
│               │   ├── screen_performance_dashboard.png
│               │   ├── screen_school_leaderboard.png
│               │   └── screen_trial_logger.png
│               ├── mipmap-anydpi-v26/
│               │   ├── ic_launcher.xml
│               │   └── ic_launcher_round.xml
│               └── values/
│                   ├── colors.xml
│                   ├── strings.xml
│                   └── styles.xml
├── build.gradle.kts
├── settings.gradle.kts
├── README.md
└── stitch_athlete_performance_scouting_suite (7).zip
```

---

## Setup Instructions

### Prerequisites

Install the following:

- Android Studio
- Android SDK Platform 34
- Android SDK Build Tools
- Android Emulator or a physical Android device

Recommended:

- Windows 10 or later
- 8 GB RAM or more
- Internet connection for the first Gradle sync

### Open the Project

1. Open Android Studio.
2. Click `Open`.
3. Select this folder:

```text
C:\Users\deiva\OneDrive\Desktop\project
```

4. Wait for Gradle sync to finish.

---

## How to Run

### Option 1: Run on Emulator

1. Open Android Studio.
2. Create or select an Android emulator.
3. Choose the `app` run configuration.
4. Click the green Run button.

### Option 2: Run on Android Phone

1. Enable Developer Options on your Android device.
2. Enable USB Debugging.
3. Connect the phone using USB.
4. Select the device in Android Studio.
5. Click Run.

---

## App Workflow

A typical user flow is:

1. Open the app.
2. Review the dashboard.
3. Go to `Athletes` and create athlete profiles.
4. Use `Batch` to add a full class roster.
5. Go to `Trial` and record event results.
6. Check `Leaderboard` for top performers.
7. Open `Insights` for coaching notes.
8. Use `Export` to share the scouting report.
9. Open `Screens` to view the provided design references.

---

## Data Storage

The current version stores data locally on the device using `SharedPreferences`.

Stored data includes:

- Athlete records
- Trial records

The storage is offline-first and does not require an internet connection.

Important note:

```text
Uninstalling the app or clearing app data will remove saved athletes and trials.
```

---

## Design System

The app follows the supplied high-contrast scouting design direction.

Main visual ideas:

- Deep athletics blue for the app bar and navigation.
- Safety orange for high-priority actions.
- White cards with clear borders.
- Large touch targets for field use.
- Strong contrast for outdoor readability.

Important colors:

| Purpose | Color |
| --- | --- |
| Primary Blue | `#1A237E` |
| Safety Orange | `#FF6D00` |
| Ink Text | `#1A1C1C` |
| Surface | `#F9F9F9` |
| Card Border | `#E0E0E0` |

---

## Troubleshooting

### Gradle Sync Failed

Try:

1. Click `Try Again`.
2. Open `File > Sync Project with Gradle Files`.
3. Make sure Android SDK Platform 34 is installed.
4. Make sure Android Studio is using its bundled JDK.

### JVM Target Error

The project is configured with:

```kotlin
compileOptions {
    sourceCompatibility = JavaVersion.VERSION_17
    targetCompatibility = JavaVersion.VERSION_17
}

kotlinOptions {
    jvmTarget = "17"
}
```

If Android Studio still shows a JVM mismatch, check:

```text
File > Settings > Build, Execution, Deployment > Build Tools > Gradle
```

Set Gradle JDK to:

```text
Embedded JDK
```

### SDK Not Found

If Android Studio cannot find the SDK:

1. Open `File > Project Structure`.
2. Go to `SDK Location`.
3. Select your Android SDK folder.
4. Apply changes and sync again.

### App Does Not Install

Try:

- Rebuilding the project.
- Deleting the app from the emulator or phone.
- Running again from Android Studio.

---

## Future Improvements

The current app is functional and lightweight. Future versions can improve it with:

- Room database instead of SharedPreferences.
- MVVM with ViewModel and LiveData or StateFlow.
- Jetpack Compose UI.
- PDF export.
- CSV export.
- Cloud sync.
- User login.
- School-level reports.
- More sports and event-specific scoring models.
- Real GenAI integration for personalized coaching insights.
- Charts for athlete progression over time.

---

## Project Status

Current status:

```text
Native Kotlin Android app scaffolded and implemented.
Core screens are functional.
Launcher icon added.
Provided design screens added as in-app references.
Offline data storage is enabled.
```

---

## Author / Project


Project name:DINESH

