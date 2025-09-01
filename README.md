Universal Emergency Hub(Tracks: Grandma's Digital Sage + Universal Access Guardian + 2G Connection Ninja)
A one-stop emergency information system that works for everyone, everywhere, on everything. This is a lightweight, accessible web application built with pure HTML, CSS, and vanilla JavaScript, designed to load quickly even on 2G networks. It provides essential emergency tools without relying on any external libraries, packages, or servers—everything is inline in a single HTML file.
The project emphasizes efficiency, optimization, and universal accessibility, following best practices for low-bandwidth environments (total page size < 50KB), offline functionality via localStorage, and inclusive design for users with disabilities, elderly users, or those in low-resource settings.
Features
The application is divided into two main sections: Emergency Essentials and Crisis Communication. All features are optimized for touch, keyboard, and voice interactions, with large interactive elements (min 44px touch targets), high-contrast colors, and ARIA labels for screen readers.
Emergency Essentials

Quick Dial

Large, prominent buttons to instantly call emergency numbers.
Pre-set buttons for:

911 (Emergency Services)
Poison Control (1-800-222-1222)


Customizable local police number: Enter and save a number, which generates a dedicated call button.
Functionality: Uses tel: links for direct dialing on mobile devices. Saved via localStorage for offline access.
Voice feedback: Announces "Local police number saved" on save.


Basic First Aid

Simple, text-based step-by-step guides for common emergencies.
Covers:

CPR: Call 911, push hard and fast (30 compressions, 2 breaths).
Bleeding: Apply pressure, elevate.
Choking: 5 back blows, 5 abdominal thrusts.


Designed for quick reading with large fonts and clear structure. No images to keep load times minimal.


Emergency Contacts

Store up to 5 personal contacts (name and phone number).
Add contacts via form inputs; saved in localStorage.
Displayed as a list with direct call links (tel:) and remove buttons.
Confirmation prompt for deletions to prevent mistakes.
Voice feedback: Announces "Contact added" on addition.


Location Share

One-click button to get and share your current location.
Uses browser Geolocation API to generate a Google Maps link (e.g., https://maps.google.com/?q=lat,long).
Copies the link to clipboard for easy sharing via text or call.
Displays the link on-screen if successful.
Handles errors gracefully (e.g., permission denied).
Voice feedback: Announces "Location copied to clipboard."


Medication Tracker

Textarea to enter critical medications and allergies.
Save button stores info in localStorage and displays it below for quick reference.
Persistent across sessions; loads automatically on page open.
Voice feedback: Announces "Meds info saved."



Crisis Communication

"I'm Safe" Button

One-click to send a predefined "I'm safe." message to all saved emergency contacts.
Uses sms: links to open the device's messaging app for each contact.
Requires at least one contact; alerts if none are added.
Voice feedback: Announces "Sending I'm safe messages."


Simple Check-in

Daily wellness check for users (e.g., elderly).
"Check In Now" button records the current timestamp in localStorage.
Displays "Last check-in: [date/time]" or "Never" if none.
Loads automatically on page open.
Voice feedback: Announces "Checked in."


Emergency Phrases

Basic help phrases in multiple languages for communication in crises.
Selectable languages: English (default), Spanish, French.
Phrases include:

Help! / ¡Ayuda! / Aide!
I need a doctor. / Necesito un doctor. / J'ai besoin d'un médecin.
Call the police. / Llama a la policía. / Appelez la police.


"Update Language" button refreshes the list based on selection.
Displays English alongside the selected language for reference.



Functionalities and User Experience

Offline-First Design: All data (contacts, meds, police number, check-ins) is stored in localStorage. The app works fully offline after the first load, with no network required for core features.
Progressive Loading: Critical elements (buttons, guides) are at the top; scripts load at the end.
Voice Feedback: Uses Web Speech API (SpeechSynthesis) for audio announcements on key actions, aiding visually impaired or elderly users.
Mistake Forgiveness: Confirmations for destructive actions (e.g., removing contacts).
Multi-Input Support: Works with touch, keyboard (full tab navigation), and voice (via browser features).
Responsive Design: Viewport meta tag ensures mobile-friendliness; max-width for readability on larger screens.

Tech Stack and Implementation
This project uses a "raw" 2015-era web development approach: no folders, bundlers, or dependencies. Everything is in one file (index.html) with inline <style> for CSS and <script> for JS.

HTML: Semantic structure with sections, ARIA attributes (e.g., aria-label), and roles for accessibility.
CSS: Inline styles for optimization. Features include:

Linear gradient background for subtle design (#f0f4f8 to #ffffff).
Box shadows and transitions for modern feel without heavy assets.
High contrast (dark text on light backgrounds).
Media queries for reduced motion, high contrast, and color-blind friendliness (avoids red-green reliance).
Large fonts (18px min, 24px for buttons), rounded corners, and spacious padding.


JavaScript: Vanilla JS only.

Event handlers for buttons (e.g., onclick).
LocalStorage for persistence.
Geolocation and Clipboard APIs for location sharing.
SpeechSynthesis for voice.
Dynamic DOM updates (e.g., adding/removing list items).


Optimization for 2G:

Total size < 50KB (inline everything, no images/icons).
No external resources; loads in ~20s on 2G.
Minimal JS: Efficient functions, no loops or heavy computations.


Accessibility Guardian:

Keyboard navigation: Logical tab order, focus outlines.
Screen reader support: ARIA labels, semantic tags.
Color-blind friendly: Text/patterns over color.
Motor/cognitive support: Large targets, simple nav (2 levels deep), clear labels.



Installation and Usage

Download the single index.html file.
Open it in any modern web browser (desktop or mobile).
No installation required—it's a static page.
For offline use: Save to your device; it caches via browser.

Example: On a phone, add to home screen for app-like access.
Limitations and Future Tracks

Current Limitations: Limited to browser-supported APIs (e.g., Geolocation requires permission). Phrases support only 3 languages; expandable in JS.
Future Tracks:

Add more first-aid guides or languages.
Integrate Service Workers for true PWA offline caching.
Expand to more emergency types (e.g., natural disasters).
User testing for further accessibility improvements.



Contributing
This is an open project—fork and modify the single HTML file. Pull requests welcome for bug fixes or feature additions, keeping the "no dependencies" rule.
Built with ❤️ for safety and accessibility. If you have feedback, open an issue!