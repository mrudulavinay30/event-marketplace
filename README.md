# Elite Events (EventFlow) - Premium Event Management & Marketplace

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![GSAP](https://img.shields.io/badge/GSAP-88CE02?style=for-the-badge&logo=greensock&logoColor=white)

**Elite Events (EventFlow)** is a modern, responsive, and visually stunning web application designed for organizing, discovering, and managing technology conferences, expos, and summits. Built with sleek dark-mode aesthetics, glassmorphism UI elements, smooth GSAP animations, and browser-native local storage, Elite Events provides a complete event ecosystem for both attendees and event organizers.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack & Dependencies](#tech-stack--dependencies)
- [Project Architecture & File Structure](#project-architecture--file-structure)
- [Getting Started: How to Run Locally](#getting-started-how-to-run-locally)
  - [Option 1: Using VS Code Live Server (Recommended)](#option-1-using-vs-code-live-server-recommended)
  - [Option 2: Using Python HTTP Server](#option-2-using-python-http-server)
  - [Option 3: Using Node.js (`serve` / `http-server`)](#option-3-using-nodejs-serve--http-server)
  - [Option 4: Direct Browser Execution](#option-4-direct-browser-execution)
- [Application Pages & User Navigation](#application-pages--user-navigation)
- [Data Storage & Management](#data-storage--management)
- [Troubleshooting & Bug Fixes](#troubleshooting--bug-fixes)

---

## 🌟 Overview

Elite Events brings a high-end experience to event management. Whether browsing upcoming summits, registering as an attendee, showcasing interactive video promos, or managing analytics from an admin dashboard, the app operates seamlessly in any modern web browser without requiring a heavy backend setup.

---

## ✨ Key Features

- 🎨 **Modern Dark & Glassmorphic UI**: High-contrast, dark-mode design with blurred glass containers and smooth color gradients.
- ⚡ **Dynamic & Static Event Listings**: Showcase curated marquee events (AI Frontiers Summit, DevCon Global, CyberGuard Expo) alongside dynamically published events.
- 🎟️ **Seamless Attendee Registration**: Interactive registration form with automatic event pre-selection, screenshot proof attachment handling, and local storage fallback validation.
- ➕ **Event Creation Portal**: Event organizers and admins can instantly publish new tech events with custom titles, dates, locations, and banner image URLs.
- 📊 **Admin Dashboard & Analytics**: Dedicated management interface featuring interactive primary analytics and user management views.
- 🎬 **Video Hero Section & Interactive Demos**: Video backgrounds and integrated promotional video preview playback.
- 📱 **Fully Responsive Layout**: Built with Tailwind CSS utilities to ensure full compatibility across mobile devices, tablets, and desktop screens.
- 💫 **Interactive Micro-Animations**: Powered by GSAP (GreenSock Animation Platform) and AOS (Animate On Scroll) for high-performance scroll effects.

---

## 🛠️ Tech Stack & Dependencies

| Layer | Technologies / Libraries |
| :--- | :--- |
| **Markup & Structure** | HTML5 (Semantic elements) |
| **Styling & Frameworks** | [Tailwind CSS CDN](https://tailwindcss.com/), Custom Vanilla CSS (Glassmorphism, Shimmer effects) |
| **Icons & Typography** | [FontAwesome 6](https://fontawesome.com/), Google Fonts (`Inter`) |
| **Animations** | [GSAP 3.12.2](https://greensock.com/gsap/) + ScrollTrigger, [AOS (Animate On Scroll)](https://michalsnik.github.io/aos/) |
| **Client-Side Logic** | Vanilla JavaScript (ES6+) |
| **Data Persistence** | Web Storage API (`localStorage`) |

---

## 📁 Project Architecture & File Structure

```
event_marketplace/
│
├── index.html                           # Landing page with Hero video, featured & dynamic events
├── events.html                          # Full list of available events
├── event_register.html                  # Form page for attendees to register for selected events
├── register.html                        # Organizer page to create & publish new tech events
├── login.html                           # User authentication / login portal
├── admin.html                           # Admin sidebar shell hosting analytics & user management
├── dashboard.html                       # Primary analytics dashboard iframe view
├── dashboard2.html                      # Secondary dashboard / user management view
├── about.html                           # About the company / platform
├── contact.html                         # Contact & inquiry form page
├── thank-you.html                       # Registration confirmation & thank-you page
├── BUGS.md                              # Log of resolved bugs and storage fixes
├── TODO.md                              # Completed task tracking checklist
├── Event_Management_Video_Generated.mp4 # Promotional video demonstration file
├── lc.png                               # Brand logo asset
├── download.jpg                         # Sample banner asset
└── README.md                            # Comprehensive project documentation
```

---

## 🚀 Getting Started: How to Run Locally

Since this is a client-side web application, running it locally is fast and straightforward. No `npm install` or compilation step is needed.

### Option 1: Using VS Code Live Server (Recommended)
1. Install [Visual Studio Code](https://code.visualstudio.com/) if you haven't already.
2. Install the **Live Server** extension by *Ritwick Dey* from the VS Code Marketplace.
3. Open the `event_marketplace` folder in VS Code (`File -> Open Folder...`).
4. Right-click on `index.html` in the file explorer and select **"Open with Live Server"** (or click **"Go Live"** in the bottom status bar).
5. The project will open automatically in your browser at `http://127.0.0.1:5500/index.html`.

---

### Option 2: Using Python HTTP Server
If you have Python installed on your system:

1. Open your terminal or command line prompt.
2. Navigate to the project directory:
   ```bash
   cd path/to/event_marketplace
   ```
3. Run the Python HTTP server command:
   - **Python 3.x**:
     ```bash
     python -m http.server 8000
     ```
   - **Python 2.x**:
     ```bash
     python -m SimpleHTTPServer 8000
     ```
4. Open your web browser and navigate to:
   ```text
   http://localhost:8000/index.html
   ```

---

### Option 3: Using Node.js (`serve` / `http-server`)
If you have Node.js installed:

1. Open terminal in the project directory.
2. Run one of the static server packages using `npx`:
   ```bash
   npx serve .
   ```
   *or*
   ```bash
   npx http-server -p 8000
   ```
3. Open the local address printed in the terminal console (e.g., `http://localhost:3000` or `http://localhost:8000`).

---

### Option 4: Direct Browser Execution
1. Open your file manager (File Explorer on Windows / Finder on macOS).
2. Navigate to the `event_marketplace` folder.
3. Double-click on `index.html` (or right-click -> **Open with** -> **Google Chrome / Firefox / Edge / Safari**).

---

## 🗺️ Application Pages & User Navigation

1. **Home Page (`index.html`)**:
   - Hero banner with video backdrop.
   - Highlights featured events and dynamically created events.
   - **"Join Event"** button saves chosen event to `localStorage` and opens `event_register.html`.
   - **"Watch Demo"** link opens `Event_Management_Video_Generated.mp4`.

2. **Event Registration (`event_register.html`)**:
   - Pre-populates the event title selected on the homepage or allows selecting from available events.
   - Saves attendee information to `localStorage` (`attendees`).
   - Includes graceful fallback handling for browser quota limits.

3. **Event Creator (`register.html`)**:
   - Allows event organizers to create and publish new tech events.
   - Stores new events in `localStorage` under `myEvents` which render dynamically on the home page.

4. **Admin Dashboard (`admin.html`)**:
   - Sidebar navigation to toggle between Primary Analytics (`dashboard.html`), User Management (`dashboard2.html`), and Event Creation (`register.html`).

---

## 💾 Data Storage & Management

The application utilizes browser `localStorage` to simulate persistent data across sessions:

- `selectedEvent`: Temporarily holds the event title selected when clicking **Join Event**.
- `myEvents`: JSON array containing dynamically published event objects created via `register.html`.
- `attendees`: JSON array containing registered attendee details collected via `event_register.html`.

*Tip: To reset application data, open Browser Developer Tools (F12) -> Application -> Local Storage -> Clear All.*

---

## 📝 Troubleshooting & Notes

- **Animations Not Triggering**: Ensure you have an active internet connection so CDN scripts for GSAP, AOS, and Tailwind CSS can load.
- **Quota Exceeded Error**: If uploading large image attachments during registration, the app automatically switches to storing minimal attendee data to avoid `QuotaExceededError`.

---

Developed with ❤️ for seamless event discovery and management.
