# AutoCare AI — Get Your APK in 15 Minutes

## STEP-BY-STEP GUIDE TO GET YOUR APK

---

## STEP 1 — Create GitHub Repository (2 min)

1. Go to **github.com** → Click the **+** icon (top right) → **New repository**
2. Name it: `autocare-ai`
3. Set to **Public**
4. ✅ Check **"Add a README file"**
5. Click **Create repository**

---

## STEP 2 — Upload All Files (5 min)

### Method A: GitHub Web Upload (easiest, no terminal needed)

1. In your new repo, click **"Add file"** → **"Upload files"**
2. Upload the entire `autocare-ai-source.zip` contents:
   - Drag ALL folders: `src/`, `public/`, `.github/`
   - Drag ALL files: `package.json`, `capacitor.config.json`, `tsconfig.json`, `.gitignore`
3. Scroll down → Click **"Commit changes"**

### Method B: Git Terminal (faster)

```bash
# On your PC/Mac — open Terminal

git clone https://github.com/YOUR_USERNAME/autocare-ai.git
cd autocare-ai

# Copy all files from the ZIP into this folder, then:
git add .
git commit -m "Initial commit - AutoCare AI"
git push origin main
```

---

## STEP 3 — Watch the APK Build (10-15 min)

1. Go to your GitHub repo
2. Click the **"Actions"** tab (top menu)
3. You'll see **"Build AutoCare AI APK"** workflow running 🟡
4. Wait ~12-15 minutes for it to complete ✅
5. When done:
   - Click on the completed workflow
   - Scroll to **"Artifacts"** section at bottom
   - Click **"AutoCare-AI-Debug-APK"** to download!

**OR** — it also creates a GitHub Release automatically:
- Click **"Releases"** on the right sidebar of your repo
- Download `app-debug.apk` from there

---

## STEP 4 — Install on Your Phone (2 min)

### Android:
1. Transfer the APK to your phone (WhatsApp to yourself, Google Drive, or USB cable)
2. On phone: **Settings** → **Security** → Enable **"Install Unknown Apps"** (or "Unknown Sources")
3. Open the APK file → Tap **Install**
4. Done! AutoCare AI is on your phone 🎉

### Share with Others:
- Upload to Google Drive → Share link
- Send via WhatsApp directly
- Upload to **appetize.io** for browser testing

---

## TROUBLESHOOTING

### Build failed?
- Click the failed job in Actions → Read the red error
- Most common fix: make sure ALL files are uploaded including `.github/workflows/build-apk.yml`

### Can't install APK?
- Android 8+: Settings → Apps → Special App Access → Install Unknown Apps → Allow your file manager
- Android 7: Settings → Security → Unknown Sources → Enable

### APK too large?
- The debug APK will be ~8-15MB — totally normal
- For smaller production APK, use `assembleRelease` instead

---

## FILE STRUCTURE (what to upload)

```
autocare-ai/
├── .github/
│   └── workflows/
│       └── build-apk.yml        ← THE MOST IMPORTANT FILE
├── src/
│   ├── App.tsx
│   ├── App.css
│   ├── index.css
│   ├── index.tsx
│   ├── components/
│   │   ├── BottomNav.tsx
│   │   └── SplashScreen.tsx
│   └── screens/
│       ├── Dashboard.tsx
│       ├── FuelHistory.tsx
│       ├── OilChange.tsx
│       ├── RPMMeter.tsx
│       ├── Analytics.tsx
│       └── Vehicles.tsx
├── public/
│   └── index.html
├── capacitor.config.json        ← Required for Android
├── package.json
├── tsconfig.json
└── .gitignore
```

---

## Build time: ~12-15 minutes on GitHub's servers (free)
## APK size: ~8-15 MB
## Supports: Android 7.0+ (API 24+)
