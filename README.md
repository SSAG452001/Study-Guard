# 🛡️ Study Guard

**Sant Sri Asaramji Gurukul, Indore's Study Guard**
🌿 Green House ( Panini Sadan )

A study-focused DNS blocker for Android. Study Guard blocks AI websites and apps (ChatGPT, Gemini, Claude and more) while students study, so they work out the answer themselves instead of copying it.

---

## ✨ Features

- 🚫 **Blocks AI websites** – chatgpt.com, gemini.google.com, claude.ai, perplexity.ai, deepseek.com, homework-answer sites and more
- 📱 **Blocks AI apps** – opening a blocked app sends you back to the home screen
- 🎯 **Blocks distractions** – optional blocking of social media and video apps
- 🎚️ **Simple controls** – separate switches for "Block AI" and "Block distractions", plus Start/Stop Study Mode
- 🔒 **Private** – filtering runs on the phone; browsing is not sent to any Study Guard server

## ⚙️ How it works

| Layer | What it does |
|---|---|
| **DNS filter (local VPN)** | Captures only DNS requests. Blocked domains get a "site not found" reply; everything else is forwarded to Google DNS (8.8.8.8). |
| **App blocker (Accessibility service)** | Detects when a blocked app opens during Study Mode and returns you to the home screen. |

## 📥 Install

1. Download `app.apk` from this repository (or the project website).
2. Open the file and allow **Install unknown apps** if Android asks.
3. Open **Study Guard** and complete the setup below.

**Requires:** Android 7.0 (API 24) or higher.

## 🛠️ Setup after installing

1. Tap **Enable app blocking** and switch on *Study Guard* in Accessibility settings.
   On Android 13+, first go to *Settings → Apps → Study Guard → ⋮ → Allow restricted settings*.
2. Tap **Start Study Mode** and accept the VPN prompt (it is only a local filter).
3. In Chrome, turn off **Use secure DNS**, and set Android **Private DNS** to *Off*. Otherwise DNS blocking can be bypassed.

## 🌐 Project website (GitHub Pages)

The website is a single self-contained file, `index.html`, with no libraries.

1. Upload `index.html` and `app.apk` to the root of this repository.
2. Go to **Settings → Pages**, choose the `main` branch and the `/ (root)` folder, then save.
3. Your site will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

> The download button links to `app.apk`, so the APK must sit in the same folder as `index.html` with exactly that name.

## 🧱 Build the Android app from source

1. In Android Studio create a new **Empty Views Activity** project (Kotlin, package `com.paninisadan.studyguard`, minSdk 24).
2. Copy the source files over `app/src/main/`.
3. Keep `targetSdk` equal to `compileSdk` (the template default) to avoid "built for an older Android version" warnings.
4. Build the APK from **Build → Build APK(s)**.

Blocked domains and apps can be edited in `Blocklist.kt`.

## ⚠️ Limitations

- Blocks IPv4 DNS only, and only the domains and apps in the list.
- A student can stop Study Mode or uninstall the app; there is no PIN lock yet.
- The APK is installed outside the Play Store, so Android or Play Protect may show an "unknown app" warning.

## 📄 Disclaimer

This is a school project. Please get the school's permission before using its name or branding on a public website.

## ⚠️ "Blocked by Play Protect" warning

Because the APK is installed outside the Play Store, Google Play Protect may show a warning. This is normal. Tap **More details → Install anyway** (choose *Don't send* if it asks to scan). The website shows these steps before the download starts.
