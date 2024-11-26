 
---

# 📱 Convert Your React Vite App into an Android App  

Welcome! 🚀 This guide will walk you through converting your **React Vite web app** into a fully functional Android app using **Capacitor** and **Android Studio**. Whether you're a beginner or a pro, this guide has you covered! Let's turn your website into an app. 🎉  

LIve Link : https://focuszen.netlify.app/
---
![Screenshot (9389)](https://github.com/user-attachments/assets/e73659fc-6341-4f82-aeb5-249aa9dafc37)

## 🛠️ Prerequisites  
Before starting, make sure you have the following installed:  
- **Node.js** and **npm**  
- A **React Vite project** ready to go  
- **Android Studio** installed on your laptop  
- A connected Android device or emulator  

---

## 📋 Step-by-Step Guide  

### 1️⃣ **Install Capacitor in Your React Vite Project**  
Open your terminal in the project folder and run:  
```bash
npm install @capacitor/core @capacitor/cli
```  
This installs Capacitor's core and CLI tools.  

### 2️⃣ **Build Your Project for Production**  
Generate the production-ready files:  
```bash
npm run build
```  
This creates a `dist` folder containing your web app files.  

### 3️⃣ **Initialize Capacitor**  
Add Capacitor to your project:  
```bash
npx cap init
```  
It will ask for:  
- **App Name**: Give your app a name (e.g., "My App").  
- **App ID**: Use a unique ID (e.g., `com.example.myapp`).  

### 4️⃣ **Add the Android Platform**  
Add Android as the platform:  
```bash
npm install @capacitor/android
npx cap add android
```  
You should now see an `android` folder in your project directory.  

### 5️⃣ **Copy Your Build Files to Android**  
Copy your `dist` folder to the Android project:  
```bash
npx cap copy
```  

### 6️⃣ **Open the Android Project in Android Studio**  
Launch Android Studio with this command:  
```bash
npx cap open android
```  
If you get an error like **"Unable to launch Android Studio"**, make sure Android Studio is correctly installed and added to your PATH.

---

## ⚙️ Configuring and Running the App  

### 7️⃣ **Build the App in Android Studio**  
1. In Android Studio, open the project from the `android` folder.  
2. Go to **Build > Build Bundle(s)/APK(s) > Build APK(s)**.  
3. Wait for the build to finish.  

### 8️⃣ **Find and Install the APK**  
1. Once the build completes, click the **Locate** button in the bottom-right popup.  
2. Transfer the generated `app-debug.apk` to your phone via USB or cloud storage.  
3. Install the APK by opening it on your phone (you may need to enable "Install from unknown sources" in your phone settings).  

---

## 📱 Using the App on Your Phone  
1. After installation, go to your phone's **App Drawer** (list of all apps).  
2. Search for your app by the name you provided in Step 3.  
3. Open it and enjoy your app on mobile! 🎉  

---

## 🐛 Common Errors and Fixes  

### ❌ **Error: Unable to launch Android Studio**  
**Fix**: Ensure Android Studio is installed and added to your PATH environment variable.  

### ❌ **App not visible after installation**  
**Fix**: Ensure the `AndroidManifest.xml` file has the correct intent filters:  
```xml
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
```  

### ❌ **Build issues in Android Studio**  
**Fix**: Make sure you’ve copied the `dist` folder correctly and run `npx cap sync` after any changes.  

---

## 🎉 Final Thoughts  
Congratulations! 🎊 You’ve successfully converted your React Vite app into an Android app. This guide ensures you can build, install, and run your app without any hiccups.  


---

