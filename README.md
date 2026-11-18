# 📝 Notepad — Easy Notes & Memos

A clean-room clone of the classic notepad app, built as a single web app and wrapped for **Android (APK)**, **iOS (Xcode)**, and **PWA** (installable on any phone).

> Built with vanilla HTML/CSS/JS + Capacitor. No frameworks, no build step for the web part.

## ✨ Features

- **Classic lined-paper look** — yellow legal pad, blue lines, red margin, handwriting fonts (12 to choose from)
- **Rich text formatting** — Bold / Italic / Underline / Strikethrough, 7 text colors, 7 highlight colors, bullet & numbered lists
- **Checklists / To-do** — interactive checkboxes, one-tap convert between note and checklist
- **Folders with colors**, pin notes to top, search, sort by date or A–Z
- **Dark mode**, 5 paper colors, default font picker
- **Auto-save** to local storage (notes persist offline)
- **Share / copy** notes, swipe-to-delete, recently deleted folder

## 🚀 Run it

### Web / PWA
Open `www/index.html` in any browser. The `docs/` folder is the PWA version (installable to home screen) — host it anywhere static (Netlify drop, Vercel, GitHub Pages).

### Android APK
```bash
npm install
npx cap sync android
cd android && ./gradlew assembleDebug
# → android/app/build/outputs/apk/debug/app-debug.apk
```
Or just push to GitHub — the included **GitHub Action** builds the APK automatically on every push (see Actions tab → download artifact).

### iOS (iPhone)
```bash
npm install
npx cap sync ios
open ios/App/App.xcworkspace   # on macOS, with Xcode
```
Select your Apple ID team, connect iPhone, press Run.

## 📁 Project structure

```
www/              the web app (single index.html)
docs/             PWA version (served by GitHub Pages)
android/          Capacitor Android project (builds APK)
ios/              Capacitor iOS Xcode project
.github/workflows/  auto-build APK + deploy PWA to Pages
```

## ⚙️ GitHub Actions

- **`build-apk.yml`** — on every push to `main`, builds a debug APK and uploads it as a run artifact.
- **`pages.yml`** — deploys the `docs/` PWA to GitHub Pages automatically.

Enable Pages in repo Settings → Pages → Source: GitHub Actions.

## 📄 License

MIT — free to use, modify, and ship.

---
*Sample notes (Aunt Sally's Apple Pie Recipe, etc.) are demo content from the original app's marketing screenshots.*
