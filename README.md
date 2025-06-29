# Android UI Automation with WebdriverIO & Appium

This repository contains automated UI test scripts written in **JavaScript** using **WebdriverIO** and **Appium** with the **Mocha** test framework.  
The tests simulate user interactions such as adding and verifying notes in a note-taking Android application.

## Demo Link:  
Make sure to check the Allure report on GitHub Pages for detailed test results:

👉 [View Allure Test Report](https://mirgb.github.io/Appium_automated_tests/)

---

## 📱 Application Under Test

- **App Name:** ColorNote Notepad Notes  
- **Version Tested:** 4.2.4  
- **Google Play Store Link:**  
  [ColorNote on Google Play](https://play.google.com/store/apps/details?id=com.socialnmobile.dictapps.notepad.color.note)

> ⚠️ **Disclaimer:**  
> This repository does **not** contain the APK or source code of the application.  
> These tests are for **educational and demonstration purposes only** and this project is **not affiliated with or endorsed by the creators of ColorNote**.

---

## 🚀 How to Run the Tests Locally

### 🛠 Prerequisites

- [Node.js](https://nodejs.org/) (version 18 or higher recommended)  
- [Java JDK](https://adoptopenjdk.net/) (version 11 or higher)  
- [Android Studio](https://developer.android.com/studio) with Android SDK and emulator installed  
- Android emulator or a real Android device connected via USB with **USB debugging enabled**  
- [Appium](https://appium.io/) server installed globally (`npm install -g appium`) or use local Appium from devDependencies  
- `adb` tool available in your system PATH (comes with Android SDK)  

---

### 1. Install dependencies

Run this command in your project root to install all required packages:

`npm install`

### 2. Start Android Emulator or Connect Real Device

Open Android Studio

Launch an emulator with API 30 or above OR connect your real device via USB

Verify device connection:

`adb devices`

Your device/emulator should appear in the list.

### 3. Start Appium Server

You can start Appium server in one of two ways:

Globally installed Appium:

`appium`

Or via npm script (if Appium installed locally):

`npm run appium`

Make sure Appium server is running at `http://localhost:4723`.

### 4. Install the Tested App

You need to manually install the ColorNote APK on your emulator or device. The APK is not included in this repo due to licensing.

You can install it via:

`adb install /path/to/colornote.apk`

Alternatively, install the app directly from Google Play on your device or emulator.

### 5. Run the Tests

Finally, run the test suite with:

`npx wdio config/wdio.conf.js`

This will execute your WebdriverIO tests using Appium.

## 📊 Allure Report

After the tests are executed, an Allure Report is automatically generated in the allure-report directory.

To open the report locally, run:

`npx allure open`

### Demo Link:  
Make sure to check the Allure report on GitHub Pages for detailed test results:

👉 [View Allure Test Report](https://mirgb.github.io/Appium_automated_tests/)

### 6. Configuration

WebdriverIO is configured with Mocha framework, Appium service, and Android capabilities.

JavaScript config (`jsconfig.json`) is used to provide IDE support for JS files.

ESLint with eslint-plugin-wdio ensures coding standards for test files.

### 7. Legal Notice

This project is for educational and demonstration purposes only.

No proprietary APK files, source code, or assets of ColorNote are included.

All trademarks and copyrights belong to their respective owners.

Use responsibly and respect third-party application licenses.

---

## 📄 Copyright Notice

Copyright © MiRGB, 2025.  
All rights reserved.
