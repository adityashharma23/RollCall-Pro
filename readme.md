# 📊 RollCall Pro

> A smart, offline-first attendance tracker PWA for students — with subject-wise analytics, calendar view, timetable planner, and PDF/Excel export. No account needed. All data saved privately on your device.

![PWA](https://img.shields.io/badge/PWA-Ready-7c6df0?style=flat-square) ![Offline](https://img.shields.io/badge/Storage-Local%20Only-3ecf8e?style=flat-square) ![No Backend](https://img.shields.io/badge/Backend-None-fbbf24?style=flat-square) ![License](https://img.shields.io/badge/License-MIT-60a5fa?style=flat-square)



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

## 🚀 Live Demo

👉 **[Try it here](https://rollcallpro.netlify.app)** ← replace with your URL 

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

## 📄 License

MIT — free to use, modify, and distribute.

---

<div align="center">
  Made for students, by students 🎓<br/>
  <strong>No login. No cloud. No tracking. Just your attendance.</strong>
</div>
