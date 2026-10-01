Steppy — Smart Step Tracking & Fitness App
Steppy is an Android fitness application designed to help users track their daily physical activity, monitor step counts, participate in challenges, connect with friends, and stay motivated through gamification.
The application integrates Android Health Connect for health and step data, Firebase for authentication and cloud data management, and follows a modular architecture to keep the application maintainable and scalable.
📱 Project Overview
Steppy provides users with a simple platform to monitor their physical activity and improve their fitness habits.
The application focuses on:
- 👟 Daily step tracking
- 📊 Activity and health analytics
- 🏆 Fitness challenges
- 👥 Friends and social interaction
- 🎮 Gamification
- 🔐 User authentication
- ☁️ Firebase cloud integration
- 🔄 Background synchronization of health data
The project is developed as an Android application using Kotlin.
✨ Features
👟 Step Tracking
- Track daily step counts.
- Retrieve step information through Android Health Connect.
- Synchronize health data with the application.
- Display activity information to users.
📊 Analytics
Users can view their physical activity and step-related information through dedicated analytics screens.
🏆 Challenges
Users can participate in fitness challenges.
The challenge system includes:
- Creating challenges
- Joining challenges
- Tracking participant progress
- Managing challenge participants
- Monitoring challenge activity
👥 Friends
The application provides social functionality that allows users to interact with other users.
Features include:
- Friend management
- Friend data synchronization
- Social activity
🎮 Gamification
Steppy includes gamification functionality to encourage users to remain physically active.
The gamification system is handled through the application's domain layer.
🔐 Authentication
The application includes authentication functionality using Firebase.
The authentication layer separates authentication logic from the user interface through repositories.
🔄 Background Synchronization
Health information can be synchronized in the background using a dedicated worker.
This allows step information to remain updated without requiring the user to manually refresh the application.
🏗️ Project Architecture
Steppy follows a modular architecture that separates UI, business logic, data handling, and dependency injection.
Steppy
│
├── Presentation / UI
│   ├── Screens
│   ├── Navigation
│   └── UI Components
│
├── Domain
│   └── Use Cases
│
├── Data
│   ├── Health
│   ├── Repositories
│   └── Models
│
├── Dependency Injection
│   ├── AppModule
│   ├── FirebaseModule
│   └── RepositoryModule
│
└── Firebase
    └── Authentication & Cloud Data

🛠️ Technologies Used
Technology	Purpose
Kotlin	Main programming language
Android Studio	Android development
Jetpack Compose / Android UI	User interface
Health Connect	Health and step data
Firebase	Authentication and cloud services
Gradle	Build system
WorkManager	Background synchronization
Git & GitHub	Version control


📂 Project Structure
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
├── gradlew
├── gradlew.bat
├── firestore.rules
└── README.md

📦 Important Components
Health Data
data/
└── health/
    ├── HealthConnectManager.kt
    └── StepSyncWorker.kt

These components handle interaction with health data and background step synchronization.
Models
models/
├── Challenge.kt
├── Participant.kt
├── StepData.kt
└── User.kt

These classes represent the primary data structures used by the application.
Repositories
repositories/
├── AuthRepository.kt
├── AuthRepositoryImpl.kt
├── ChallengeRepository.kt
├── ChallengeRepositoryImpl.kt
├── FriendsRepository.kt
└── FriendsRepositoryImpl.kt

Repositories provide an abstraction between the application logic and external data sources.
Domain Layer
domain/
└── usecase/
    └── GamificationUseCase.kt

The domain layer contains application-specific business logic.
Dependency Injection
di/
├── AppModule.kt
├── FirebaseModule.kt
└── RepositoryModule.kt

These modules manage application dependencies and make the architecture easier to maintain.
🔥 Firebase
Steppy uses Firebase services for cloud-based functionality.
Firebase is used for areas such as:
- User authentication
- User information
- Challenge information
- Friends/social data
- Cloud database functionality
The project also includes:
firestore.rules

which contains Firestore security rules.
Security Note: Never upload private Firebase credentials, API secrets, service-account keys, or other sensitive information to GitHub.

🚀 Getting Started
1. Clone the Repository
git clone https://github.com/aryanburramukku2007-droid/DBSE-DBD-Project.git

Navigate to the project:
cd DBSE-DBD-Project/Project/Steppy

2. Open in Android Studio
Open the following folder in Android Studio:
DBSE-DBD-Project/Project/Steppy

Allow Android Studio to:
- Sync Gradle
- Download required dependencies
- Index the project
3. Configure Firebase
Set up the Firebase project required by the application.
Add the appropriate Firebase configuration file:
google-services.json

Place it inside:
Steppy/app/

Do not commit sensitive credentials or private configuration files if they contain secrets.
4. Configure Health Connect
Install Health Connect on a supported Android device and grant the required health permissions to Steppy.
The application uses Health Connect to access step-related health information.
5. Build the Application
From Android Studio, select:
Build → Make Project

or run:
./gradlew build

On Windows:
.\gradlew.bat build

▶️ Running the Application
Connect an Android device or start an Android Emulator.
Then:
Run → Run 'app'

Alternatively, use:
./gradlew installDebug

On Windows:
.\gradlew.bat installDebug

🧪 Testing
The project contains both unit and Android instrumentation tests.
app/
├── src/
│   ├── test/
│   └── androidTest/

Run unit tests:
./gradlew test

Run Android tests:
./gradlew connectedAndroidTest

🔐 Security
The project includes Firestore security rules to help control access to cloud data.
Important security practices:
- Do not expose Firebase private keys.
- Do not upload service-account credentials.
- Use appropriate Firestore security rules.
- Validate authenticated users before accessing protected data.
- Keep sensitive configuration outside the public repository.
🌟 Future Improvements
Possible future enhancements include:
- 🤖 AI-powered fitness recommendations
- 📈 Advanced activity analytics
- 🏃 Personalized fitness goals
- 🥇 Leaderboards
- 🔔 Smart fitness notifications
- 🌎 Global fitness competitions
- 🧠 Personalized activity predictions
- ⌚ Wearable device integration
- 📱 Improved smartwatch support
- 🎯 Personalized daily challenges
🎯 Project Objectives
The main objectives of Steppy are:
1. Provide users with an easy way to monitor physical activity.
2. Integrate Android health data into a single application.
3. Encourage users to maintain an active lifestyle.
4. Introduce social interaction through fitness challenges.
5. Use gamification to increase user engagement.
6. Demonstrate the development of a modern Android application.
7. Implement a scalable architecture separating UI, business logic, and data layers.
👨‍💻 Development
Project: Steppy
Platform: Android
Language: Kotlin
Category: Health & Fitness
Repository: DBSE-DBD-Project
