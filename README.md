Universal Emergency Hub(Tracks: Grandma's Digital Sage + Universal Access Guardian + 2G Connection Ninja)
A one-stop emergency information system that works for everyone, everywhere, on everything. This is a lightweight, accessible web application built with pure HTML, CSS, and vanilla JavaScript, designed to load quickly even on 2G networks. It provides essential emergency tools without relying on any external libraries, packages, or servers—everything is inline in a single HTML file.
The project emphasizes efficiency, optimization, and universal accessibility, following best practices for low-bandwidth environments (total page size < 50KB), offline functionality via localStorage, and inclusive design for users with disabilities, elderly users, or those in low-resource settings.

# 🆘 Universal Emergency Hub

A one-stop emergency assistant that works for everyone, everywhere — even on 2G. Built with pure HTML, CSS, and vanilla JS in a single `index.html` file. Zero dependencies. Ultra-fast. Accessible by design.

• Size-conscious (< 50KB) • Offline-first • High contrast • Keyboard & screen-reader friendly

## ✨ Highlights
- ⚡ Ultra-lightweight: No builds, no packages, no trackers — just one static file.
- 📴 Offline-first: Stores data in `localStorage` (contacts, meds, check-ins, police number).
- 🗣️ Voice feedback: Uses Web Speech API for key actions.
- ♿ Inclusive UX: Large touch targets (≥44px), high contrast, ARIA labels, full keyboard navigation.
- 📶 2G-ready: Minimal JS and inline CSS, no external assets.

## 🧭 Table of Contents
- Overview
- Features
- Accessibility by Design
- Performance & 2G Strategy
- Tech Stack
- Quick Start
- Usage Guide
- Data & Privacy
- Troubleshooting
- Roadmap
- Acknowledgements

## 🔎 Overview
The app splits into two areas: Emergency Essentials and Crisis Communication. All actions are large, clear, and fast — usable by touch, keyboard, or assistive tech.

## 🚀 Features

### ☎️ Quick Dial
- 911 and Poison Control one-tap call buttons
- Custom Local Police button (saved to `localStorage`)
- Uses `tel:` links for instant dialing on mobile

### 🩺 Basic First Aid (text-only, rapid-read)
- CPR: Call 911 → 30 compressions → 2 breaths
- Bleeding: Apply pressure → Elevate
- Choking: 5 back blows → 5 abdominal thrusts

### 👥 Emergency Contacts (up to 5)
- Add name + phone → saved locally
- Tap to call; remove with confirmation

### 📍 Location Share
- One-tap: gets GPS and creates a Google Maps link
- Auto-copies link to clipboard; displays on screen
- Graceful error states; voice confirmation

### 💊 Medications & Allergies
- Save critical info for quick access
- Persisted in `localStorage`

### ✅ “I’m Safe” Broadcast
- Opens SMS composer to each saved contact with “I’m safe.”

### 📅 Daily Check‑in
- Records timestamp; shows “Last check‑in”

### 🌐 Emergency Phrases (EN/ES/FR)
- Shows English + selected language side‑by‑side

## ♿ Accessibility by Design
- High contrast palette; readable sizes (18px base, 24px buttons)
- Logical tab order; clear focus styles
- ARIA labels for assistive tech
- Reduced‑motion support via media queries
- Color‑blind friendly (avoid red/green reliance)

## 📶 Performance & 2G Strategy
- Inline CSS/JS, zero images/icons
- No network requests after first load
- Minimal DOM & efficient event handlers

## 🛠️ Tech Stack
- HTML (semantic structure + ARIA)
- CSS (inline, responsive, high‑contrast)
- JavaScript (vanilla; Web Speech, Geolocation, Clipboard, localStorage)

## ⚙️ Quick Start
1) Download `index.html`
2) Open in any modern browser (mobile or desktop)
3) Optional: “Add to Home Screen” on mobile for app-like access

## 📘 Usage Guide
- Set your Local Police number and save
- Add up to 5 emergency contacts
- Share location during emergencies
- Store meds/allergy info for quick recall
- Use “I’m Safe” after a crisis to notify contacts
- Check in daily to keep a wellness trail

## 🔒 Data & Privacy
- All data stays on your device via `localStorage`
- No servers, no analytics, no network calls

## 🛟 Troubleshooting
- Location not working: ensure location permissions are allowed for the browser
- SMS not opening: some desktop browsers block `sms:` links — try on mobile
- Voice feedback missing: your browser may not support Speech Synthesis

## 🗺️ Roadmap
- Service Worker for true PWA offline caching
- More languages and first‑aid modules
- Expanded emergency scenarios (natural disasters, etc.)
- Ongoing user testing for accessibility improvements

## 🙌 Acknowledgements
Built for accessibility, resilience, and speed — especially where connectivity and resources are limited.

Contributing
This is an open project—fork and modify the single HTML file. Pull requests welcome for bug fixes or feature additions, keeping the "no dependencies" rule.
Built with ❤️ for safety and accessibility. If you have feedback, open an issue!