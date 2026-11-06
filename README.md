# 🌸 JAPAN TOURS • Ultra-Luxury 10-Day Curated Expedition

[![Live Demo](https://img.shields.io/badge/Demo-japan--tour--blue.vercel.app-00f0ff?style=for-the-badge&logo=vercel&logoColor=white)](https://japan-tour-blue.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Mohithkushakumar511-violet?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Mohithkushakumar511)
[![Node.js](https://img.shields.io/badge/Node.js-v16+-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

A production-ready, client-facing ultra-luxury travel web experience for **JAPAN TOURS**, showcasing an exclusive 10-day curated expedition across Osaka, Kyoto, and Tokyo. Designed with a dark obsidian aesthetic, fluid 300-frame scroll-driven canvas animations, inertia-damped 3D perspective physics, an interactive Web Audio synthesizer, and a full-featured concierge booking engine.

---

## 📑 Table of Contents

- [Live Demo](#-live-demo)
- [Highlights & Features](#-highlights--features)
- [Destination Highlights](#-destination-highlights)
- [Tech Stack & Architecture](#-tech-stack--architecture)
- [Project Structure](#-project-structure)
- [Quick Start & Local Setup](#-quick-start--local-setup)
- [API Reference](#-api-reference)
- [Deployment](#-deployment)
- [Author & Credits](#-author--credits)
- [License](#-license)

---

## 🔗 Live Demo

Experience the live application here:  
👉 **[https://japan-tour-blue.vercel.app/](https://japan-tour-blue.vercel.app/)**

---

## ✨ Highlights & Features

### 🎬 Fixed-Background 300-Frame Canvas Scroll Engine
- High-performance HTML5 `<canvas>` rendering engine delivering butter-smooth lerp-damped frame playback across a 300-frame image sequence (`ezgif-frame-001.jpg` to `300.jpg`).
- Responsive image aspect ratio calculation and automatic retina display scaling.

### 🌌 Pure Dark Obsidian Aesthetics
- Deep pitch-black (`#000000`) canvas complemented by neon violet, magenta, and electric cyan accents.
- Luxury radial vignettes and alpha edge-masking that melt editorial photography into the background without harsh borders.
- Interactive cursor spotlight tracking mouse position.

### 🕹️ 3D Physics & Tilt Perspectives
- Physics-based card tilt with lerp inertia damping for desktop pointer interaction.
- Harmonic oscillation floating loops (`fluidLevitate`) at 60fps for mobile and touch screens.

### 🕒 Real-Time Tokyo (JST) Clock & Status Ping
- Live navbar status beacon displaying real-time Japan Standard Time (JST) with live pulsing indicator.

### 🎵 Web Audio API Ambient Soundscape
- Custom Web Audio synthesizer playing gentle, meditative pentatonic chime chords and subtle haptic-style audio feedback upon interaction.

### 🖼️ Interactive Fullscreen Photo Lightbox
- High-resolution modal viewer with blurred dark backdrop, technical camera/shot metadata breakdown, and keyboard navigation (`Escape` dismissal).

### 📋 Bespoke Journey Concierge & Reservation Engine
- Two-column validated booking panel supporting live destination selection (Tokyo, Kyoto, Osaka, All Japan), date picker, traveler stepper, and custom itinerary notes.
- Persistent backend API (`POST /api/contact`) recording inquiries directly to `enquiries.json`.
- Dynamic booking confirmation modal presenting generated booking reference IDs (e.g., `JP-XXXXXXXX`).

---

## 🗺️ Destination Highlights

| Destination | Curated Experience | Key Sights & Highlights |
| :--- | :--- | :--- |
| **Tokyo** | Modern Metropolis & Cyberpunk Nightscapes | Shibuya Crossing, teamLab Planets, Shinjuku Golden Gai, Michelin culinary private dining |
| **Kyoto** | Ancient Sanctuaries & Imperial Heritage | Fushimi Inari-taisha torii gates, Gion geisha district, private tea ceremony & zen gardens |
| **Osaka** | Gastronomy & Blue Hour Canals | Dotonbori neon canal reflections, Osaka Castle private grounds, Kuromon Ichiba market |
| **Mt. Fuji** | Sacred Serenity & Onsen Retreats | Lake Kawaguchiko twilight reflections, luxury ryokan with private cedar onsen |

---

## 🛠️ Tech Stack & Architecture

### Frontend
- **HTML5 & Vanilla JavaScript (ES6+):** Core logic, lerp physics, animation loops, and modal handling without heavy framework bloat.
- **Tailwind CSS (CDN):** Modern utility-first styling with custom theme extensions (`darkSurface`, `cardDark`, `glassBorder`).
- **HTML5 Canvas API:** 300-frame sequence scroll synchronization with window scroll position.
- **Web Audio API:** Real-time synthesis for ambient audio landscapes.
- **Lucide Icons:** Clean, modern vector iconography.
- **Google Fonts:** Typography powered by *DM Sans*.

### Backend
- **Node.js Native HTTP Server:** Zero-dependency, lightweight server (`server.js`) handling static asset streaming with aggressive caching for JPEG assets.
- **JSON File-Based Store:** Direct persistence of user inquiries to `enquiries.json`.
- **CORS & Security:** Configured CORS headers and path traversal protections.

---

## 📁 Project Structure

```text
japan-tour/
├── index.html                   # Core single-page application & layout
├── server.js                    # Zero-dependency Node.js HTTP server & API handler
├── enquiries.json               # Persisted expedition inquiries & bookings
├── .gitignore                   # Git ignore specifications
├── README.md                    # Project documentation
├── assets/
│   ├── css/
│   │   └── style.css            # Custom CSS animations, canvas sizing & luxury styling
│   ├── js/
│   │   └── main.js              # Canvas scroll engine, Web Audio, lightbox & form logic
│   └── images/                  # High-resolution editorial photography
│       ├── hero-kimono-fuji.jpg
│       ├── tokyo-shibuya-night.jpg
│       ├── fuji-twilight-lake.jpg
│       ├── artisan-ramen-macro.jpg
│       ├── kyoto-gion-lanterns.jpg
│       ├── fushimi-torii-editorial.jpg
│       └── osaka-dotonbori-night.jpg
└── ezgif-frame-001.jpg ... 300  # Scroll animation frame sequence (300 JPGs)
```

---

## 🚀 Quick Start & Local Setup

### Prerequisites
- [Node.js](https://nodejs.org/) (version 16 or later recommended)
- [Git](https://git-scm.com/)

### 1. Clone the Repository
```bash
git clone https://github.com/Mohithkushakumar511/japan-tour.git
cd japan-tour
```

### 2. Start the Server
Run the native Node.js server:
```bash
node server.js
```

By default, the server will start on port `3000`:
```text
==============================================
  Scroll Animation Server is running!
  Local URL: http://localhost:3000/
==============================================
```
*(If port 3000 is occupied, the server automatically selects the next available port).*

### 3. Open in Browser
Visit [http://localhost:3000](http://localhost:3000) in your web browser.

---

## 📡 API Reference

### `POST /api/contact`
Receives and records luxury expedition reservation requests.

#### Request Headers
```http
Content-Type: application/json
```

#### Request Body
```json
{
  "name": "Alexander Vance",
  "email": "alexander.vance@example.com",
  "phone": "+81 90-1234-5678",
  "destination": "Osaka",
  "travelDate": "2026-11-20",
  "travelers": 2,
  "notes": "Interested in private architecture guides and Michelin dining."
}
```

#### Successful Response (`200 OK`)
```json
{
  "success": true,
  "message": "Your enquiry has been received.",
  "enquiry": {
    "id": "JP-MVQTFNHP",
    "destination": "Osaka",
    "travelDate": "2026-11-20",
    "travelers": 2
  }
}
```

#### Error Response (`400 Bad Request`)
```json
{
  "success": false,
  "error": "A valid email address is required."
}
```

---

## 🚢 Deployment

### Deploying to Vercel
The project can be deployed seamlessly to Vercel:
1. Push your repository to GitHub.
2. Import the `japan-tour` repository into your [Vercel Dashboard](https://vercel.com).
3. Set the Framework Preset to **Other** (Static Site).
4. Deploy! Static assets and client functionality will be instantly live.

---

## 👤 Author & Credits

Crafted with care by **Mohith Kusha Kumar**
- **GitHub:** [@Mohithkushakumar511](https://github.com/Mohithkushakumar511)
- **Repository:** [Mohithkushakumar511/japan-tour](https://github.com/Mohithkushakumar511/japan-tour)

---

## 📄 License

This project is licensed under the MIT License - feel free to customize and adapt it for your own luxury travel experiences.

&copy; 2026 JAPAN TOURS. All rights reserved.
