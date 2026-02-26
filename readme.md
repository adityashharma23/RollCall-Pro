# 📊 Addentance Tracker

> A smart, offline-first attendance tracker PWA for students — with subject-wise analytics, calendar view, timetable planner, and PDF/Excel export. No account needed. All data saved privately on your device.

![PWA](https://img.shields.io/badge/PWA-Ready-7c6df0?style=flat-square) ![Offline](https://img.shields.io/badge/Storage-Local%20Only-3ecf8e?style=flat-square) ![No Backend](https://img.shields.io/badge/Backend-None-fbbf24?style=flat-square) ![License](https://img.shields.io/badge/License-MIT-60a5fa?style=flat-square)

---

## ✨ Features

| Feature | Description |
|--------|-------------|
| 📅 **Calendar View** | FullCalendar.js powered month/week view — click any date to mark attendance |
| ✔️ **Attendance Marking** | Mark days as Present, Absent, or Off Day with per-subject breakdown |
| 🗓️ **Weekly Timetable** | Define subjects per weekday — auto-fills when marking attendance |
| 📊 **Analytics Dashboard** | Subject-wise percentage bars, overall stats, and detailed report table |
| 🔔 **Smart Alerts** | Auto-warns when any subject or overall attendance drops below 75% |
| 📄 **PDF Export** | Generates a clean attendance report via jsPDF |
| 📊 **Excel Export** | Multi-sheet Excel file (attendance log + subject summary) via SheetJS |
| 💾 **Local Storage** | All data saved on-device — restores automatically on every visit |
| 📱 **PWA** | Installable on Android & iOS, works fully offline |
| ✏️ **Editable Profile** | Name, Course, Branch, Semester, Academic Year |
| 🌙 **Dark UI** | Modern dark glassmorphism dashboard design |

---

## 📸 Screenshots

> Calendar view · Analytics dashboard · Timetable planner · Mobile bottom nav

---

## 🚀 Live Demo

👉 **[Try it here](https://your-deployment-url.netlify.app)** ← replace with your URL

---

## 📂 File Structure

```
addentance-tracker/
├── index.html        ← Entire app (HTML + CSS + JS, single file)
├── manifest.json     ← PWA manifest (name, icons, theme)
├── sw.js             ← Service worker (offline caching)
├── icon-192.png      ← PWA icon — add your own
├── icon-512.png      ← PWA icon — add your own
└── README.md
```

> The entire app lives in **one HTML file** — no build tools, no npm, no dependencies to install.

---

## ⚡ Quick Start

### Option 1 — Open directly
Download the repo and open `index.html` in any browser. Done.

### Option 2 — Local server (recommended for PWA features)
```bash
# Using Node
npx serve .

# Using Python
python -m http.server 3000
```
Then visit `http://localhost:3000`

### Option 3 — Deploy instantly
Drag and drop the folder at **[netlify.com/drop](https://netlify.com/drop)** — live in 10 seconds.

---

## 💾 How Local Storage Works

Addentance Tracker is **100% offline-first**. There is no server, no account, no cloud.

```
First visit
  └── Shows welcome screen → "Open My Tracker"
      └── If no profile yet → Setup Wizard (name, course, off days)
          └── App opens → data saved to localStorage

Every visit after
  └── App boots automatically
      └── Restores your full attendance history, timetable & profile
          └── Every change is saved instantly to localStorage
```

Your data is stored under the key `addentance_tracker_data` in your browser's localStorage. It persists until you clear browser data or click **"Clear All Data"** inside the app.

> ⚠️ **Note:** localStorage is per-browser per-device. Data does not sync across devices. To move data, use the Excel export feature.

---

## 📱 Install as Mobile App (PWA)

### Android (Chrome)
1. Open the app in Chrome
2. Tap **⋮ Menu → "Add to Home Screen"**
3. App opens fullscreen like a native app

### iOS (Safari)
1. Open in Safari
2. Tap the **Share icon → "Add to Home Screen"**
3. App launches fullscreen with no browser bar

### Desktop (Chrome / Edge)
1. Click the **install icon** in the address bar
2. App opens in its own window

---

## 🛠️ Tech Stack

| Library | Version | Purpose |
|---------|---------|---------|
| [FullCalendar.js](https://fullcalendar.io) | 6.1.10 | Calendar UI |
| [jsPDF](https://github.com/parallax/jsPDF) | 2.5.1 | PDF generation |
| [jsPDF-AutoTable](https://github.com/simonbengtsson/jsPDF-AutoTable) | 3.8.2 | PDF tables |
| [SheetJS (XLSX)](https://sheetjs.com) | 0.18.5 | Excel export |
| [Google Fonts](https://fonts.google.com) | — | Syne + DM Sans |
| Web localStorage API | built-in | Data persistence |
| Service Worker API | built-in | Offline support |

**No frameworks. No build step. No npm install.**

---

## 📋 How to Use

### 1. Set Up Profile
On first launch, the setup wizard asks for your name, course details, and weekly off days (e.g. Saturday + Sunday). These are saved and restored every time.

### 2. Build Your Timetable
Go to the **Timetable** tab → add subjects for each weekday. These auto-populate when you mark attendance so you can record per-subject presence.

### 3. Mark Attendance
Click any date on the **Calendar** → choose Present ✔️ / Absent ❌ / Off Day ⭕ → mark each subject individually → Save.

### 4. Track Analytics
The **Analytics** tab shows:
- Overall attendance percentage
- Subject-wise progress bars
- Red alerts for subjects below 75%
- How many consecutive classes needed to recover

### 5. Export Reports
Click your avatar (top right) → **Export PDF** or **Export Excel**.

---

## ⚙️ Configuration

No configuration needed to run. Optional tweaks inside `index.html`:

```javascript
// Change the attendance warning threshold (default: 75%)
threshold: 75

// Change the localStorage key (if running multiple instances)
const STORAGE_KEY = 'addentance_tracker_data';
```

---

## 🌐 Deployment

### Netlify (Easiest)
```bash
npm install -g netlify-cli
netlify deploy --dir . --prod
```
Or drag-drop at [netlify.com/drop](https://netlify.com/drop)

### Vercel
```bash
npm install -g vercel
vercel
```

### GitHub Pages
1. Push repo to GitHub
2. Go to **Settings → Pages → Deploy from branch `main`**
3. Your app is live at `https://yourusername.github.io/repo-name`

---

## 🔮 Roadmap

- [ ] Data backup/restore via JSON file download
- [ ] Multiple profiles (for different semesters)
- [ ] Attendance goal setting per subject
- [ ] Push notification reminders
- [ ] Dark/light theme toggle
- [ ] Optional Firebase cloud sync

---

## 🤝 Contributing

1. Fork the repo
2. Create a branch: `git checkout -b feature/your-feature`
3. Commit: `git commit -m "Add your feature"`
4. Push: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

MIT — free to use, modify, and distribute.

---

<div align="center">
  Made for students, by students 🎓<br/>
  <strong>No login. No cloud. No tracking. Just your attendance.</strong>
</div>
