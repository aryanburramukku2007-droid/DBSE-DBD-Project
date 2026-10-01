# 📚 DBSE-DBD Project

## 📱 Project Repository

This repository contains the academic work, practical implementations, certifications, and project development work completed as part of the DBSE-DBD coursework.

The repository also contains **Steppy**, an Android-based fitness and step-tracking application developed using Kotlin, Firebase, and Android Health Connect.

---

# 📂 Repository Structure

```text
DBSE-DBD-Project/
│
├── Certifications/
│   └── Certificates and certification-related documents
│
├── PRACTICAL/
│   └── Practical programs and academic implementations
│
├── Project/
│   │
│   ├── readme
│   │
│   └── Steppy/
│       │
│       ├── app/
│       ├── gradle/
│       ├── build.gradle.kts
│       ├── settings.gradle.kts
│       ├── gradle.properties
│       ├── firestore.rules
│       ├── gradlew
│       ├── gradlew.bat
│       └── README.md
│
└── README.md

🚶 Steppy – Smart Step Tracking & Fitness App
Steppy is an Android-based fitness and activity tracking application designed to help users monitor their daily physical activity, participate in fitness challenges, connect with friends, and stay motivated through gamification.
The application integrates Android Health Connect for health and step-related data and Firebase for authentication and cloud-based data management.
🎯 Project Objective
The main objective of Steppy is to provide users with a simple and interactive platform for monitoring physical activity and encouraging a healthier lifestyle.
The application focuses on:
- 👟 Daily step tracking
- 📊 Activity analytics
- 🏆 Fitness challenges
- 👥 Friends and social interaction
- 🎮 Gamification
- 🔐 User authentication
- ☁️ Firebase cloud integration
- 🔄 Background health-data synchronization
✨ Features
👟 Step Tracking
Steppy allows users to monitor their daily physical activity.
Features include:
- Daily step tracking
- Health data integration
- Step data synchronization
- Activity monitoring
📊 Activity Analytics
Users can view their physical activity and step-related information through the application's analytics functionality.
This helps users understand their activity patterns and monitor their progress.
🏆 Fitness Challenges
Users can participate in fitness challenges to make physical activity more engaging.
Challenge functionality includes:
- Creating challenges
- Joining challenges
- Managing participants
- Tracking progress
- Viewing challenge information
👥 Friends
Steppy provides social functionality that allows users to interact with other users.
The application contains repository components for managing friend-related information.
🎮 Gamification
Gamification is used to make fitness activities more engaging.
The project contains a dedicated:
GamificationUseCase.kt

for application-level gamification logic.
🔐 Authentication
Firebase is used to support user authentication.
Authentication functionality is separated through repository interfaces and implementations.
AuthRepository.kt
AuthRepositoryImpl.kt

🔄 Background Synchronization
Steppy includes a background worker for synchronizing step-related health information.
StepSyncWorker.kt

This allows health information to be processed without requiring constant manual interaction from the user.
🏗️ System Architecture
The application follows a layered architecture separating the presentation, domain, and data layers.
                         ┌──────────────────────┐
                         │      STEPPY APP      │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │    PRESENTATION      │
                         │    UI & Navigation   │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │       DOMAIN         │
                         │      Use Cases       │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │        DATA          │
                         │ Repositories & Models│
                         └───────┬───────┬──────┘
                                 │       │
                    ┌────────────┘       └────────────┐
                    ▼                                 ▼
          ┌──────────────────┐              ┌──────────────────┐
          │ Android Health   │              │     Firebase     │
          │     Connect      │              │ Authentication & │
          │                  │              │ Cloud Services   │
          └──────────────────┘              └──────────────────┘

🛠️ Technologies Used
Technology	Purpose
Kotlin	Android application development
Android Studio	Development environment
Android Health Connect	Health and step data
Firebase	Authentication and cloud services
Gradle	Build system
WorkManager	Background processing
Git	Version control
GitHub	Repository management


📁 Steppy Project Structure
Steppy/
│
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/example/steppy/
│   │   │   │
│   │   │   └── res/
│   │   │
│   │   ├── androidTest/
│   │   └── test/
│   │
│   └── build.gradle.kts
│
├── gradle/
│
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
├── firestore.rules
├── gradlew
├── gradlew.bat
└── README.md

📦 Main Application Components
Health
data/
└── health/
    ├── HealthConnectManager.kt
    └── StepSyncWorker.kt

HealthConnectManager
Handles interaction with Android Health Connect for health and step-related information.
StepSyncWorker
Handles background synchronization of step information.
📊 Data Models
The application contains models representing important application entities.
models/
├── Challenge.kt
├── Participant.kt
├── StepData.kt
└── User.kt

🗄️ Repository Layer
The repository layer separates data access from the rest of the application.
repositories/
├── AuthRepository.kt
├── AuthRepositoryImpl.kt
├── ChallengeRepository.kt
├── ChallengeRepositoryImpl.kt
├── FriendsRepository.kt
└── FriendsRepositoryImpl.kt

This structure helps make the application easier to maintain and extend.
🧠 Domain Layer
The domain layer contains application-specific business logic.
domain/
└── usecase/
    └── GamificationUseCase.kt

💉 Dependency Injection
The project contains dependency injection modules for managing application dependencies.
di/
├── AppModule.kt
├── FirebaseModule.kt
└── RepositoryModule.kt

🔥 Firebase Integration
Firebase provides cloud-based functionality for the application.
It is used for functionality such as:
- User authentication
- User data
- Challenge-related data
- Friends/social data
- Cloud database functionality
Firestore security rules are included in:
firestore.rules

🔐 Security
Security is an important part of the project.
Recommended practices include:
- Do not upload private Firebase credentials.
- Do not upload service-account keys.
- Do not expose passwords or API secrets.
- Use appropriate Firestore security rules.
- Protect authenticated user information.
- Validate access to protected data.
🚀 Installation
Step 1 – Clone the Repository
git clone https://github.com/aryanburramukku2007-droid/DBSE-DBD-Project.git

Step 2 – Navigate to the Project
cd DBSE-DBD-Project/Project/Steppy

Step 3 – Open in Android Studio
Open:
DBSE-DBD-Project/Project/Steppy

in Android Studio.
Allow Android Studio to complete:
- Gradle synchronization
- Dependency installation
- Project indexing
- Android SDK configuration
🔥 Firebase Setup
If the project requires Firebase configuration, configure the Firebase project and add the required configuration file.
For Android Firebase projects, the configuration file is generally:
google-services.json

and should be placed inside:
Steppy/app/

Do not commit sensitive credentials to the repository.
❤️ Health Connect Setup
Install Android Health Connect on a compatible Android device.
When the application requests health permissions, grant the permissions required for step tracking.
The application uses Health Connect to access step-related information.
▶️ Running the Project
Connect an Android device or start an Android Emulator.
From Android Studio select:
Run → Run 'app'

The application should then build and launch on the selected device.
🔨 Building the Project
Windows
.\gradlew.bat build

Linux / macOS
./gradlew build

🧪 Testing
The project contains both unit tests and Android instrumentation tests.
app/
└── src/
    ├── test/
    └── androidTest/

Run Unit Tests
./gradlew test

Windows
.\gradlew.bat test

Android Tests
./gradlew connectedAndroidTest

🎯 Project Objectives
The project aims to:
1. Develop a functional Android fitness application.
2. Track users' daily physical activity.
3. Integrate Android Health Connect.
4. Provide fitness challenges.
5. Support social interaction through friends.
6. Implement gamification.
7. Synchronize health information in the background.
8. Use Firebase for authentication and cloud functionality.
9. Apply a structured application architecture.
10. Provide a foundation for future fitness features.
🌟 Future Enhancements
Possible future improvements include:
- 🤖 AI-powered fitness recommendations
- 📈 Advanced fitness analytics
- 🏃 Personalized workout recommendations
- 🥇 Global leaderboards
- 🔔 Smart activity reminders
- 🎯 Personalized daily goals
- ⌚ Smartwatch integration
- 🌐 Online fitness competitions
- 🧠 Activity prediction
- 📊 Detailed fitness reports
- 🏅 Achievement and badge systems
📚 Learning Outcomes
This project provides practical experience in:
- Kotlin programming
- Android application development
- Firebase integration
- Android Health Connect
- Repository architecture
- Background processing
- Dependency injection
- Authentication
- Cloud data management
- Testing
- Git
- GitHub
- Android project management
👨‍💻 Project Information
Item	Details
Project Name	Steppy
Project Type	Android Fitness Application
Platform	Android
Programming Language	Kotlin
Cloud Platform	Firebase
Health Platform	Android Health Connect
Build System	Gradle
Version Control	Git
Repository	GitHub
