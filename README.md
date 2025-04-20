### 📥 How to Use the Downloaded FCMExampleApp ZIP in Android Studio

This ZIP file contains the **Kotlin source code** and **XML layouts** needed to implement **Firebase Cloud Messaging (FCM)** push notifications in your Android app.

---

#### ✅ Steps to Set It Up in Android Studio

1. **Download the ZIP file**
   - [Click here to download](sandbox:/mnt/data/FCMExampleApp.zip)
   - Save it somewhere on your computer.

2. **Extract the ZIP**
   - Right-click on the ZIP file and choose **“Extract All”** (Windows) or use **Archive Utility** (Mac).
   - You will get a folder named `FCMExampleApp`.

3. **Open Android Studio**
   - Open **Android Studio**.
   - Choose **File > New > Import Project** or **File > Open**.
   - Navigate to the extracted folder and open it.

---

#### 🔧 Important Notes

- 🧠 **This repository only contains Kotlin classes and XML layout files.**
  - You will need to copy the relevant files into your **own Android Studio project** if you don’t open the full project.
  
- 📦 **Add Firebase dependencies**
  Open your `build.gradle (app-level)` and include the following:
  ```gradle
  implementation 'com.google.firebase:firebase-messaging:23.0.0'
  ```

  Also, make sure your `build.gradle (project-level)` includes:
  ```gradle
  classpath 'com.google.gms:google-services:4.3.15'
  ```

- 🛡️ **Add the google-services plugin**
  In your app-level `build.gradle`, add this at the bottom:
  ```gradle
  apply plugin: 'com.google.gms.google-services'
  ```

- 🔑 **Add your `google-services.json` file**
  - Sign in to [Firebase Console](https://console.firebase.google.com/).
  - Create a new Firebase project and connect your Android app.
  - Download the `google-services.json` file.
  - **Place it in the `/app` directory** of your project.

---

#### 🟢 Run the App

- Once the setup is done, click **Run** ▶️ in Android Studio.
- Test push notifications from Firebase console or use a test server.
