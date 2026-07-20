<div align="center">
  <h1>🌌 星系风格个人介绍主页 | Galaxy Theme Portfolio</h1>
</div>

<p align="center">
  <strong>A stunning, immersive dark cosmic portfolio & personal homepage built with Astro 6 & Three.js</strong>
</p>

<p align="center">
  <a href="https://astro.build/"><img src="https://img.shields.io/badge/Astro-6.x-883AEA?style=for-the-badge&logo=astro&logoColor=white" alt="Astro 6"></a>
  <a href="https://threejs.org/"><img src="https://img.shields.io/badge/Three.js-v0.184-black?style=for-the-badge&logo=three.js&logoColor=white" alt="Three.js"></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-5.9-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-GPL--3.0-blue?style=for-the-badge" alt="License"></a>
</p>

<p align="center">
  <a href="README.md"><strong>🇨🇳 中文文档</strong></a> ·
  <a href="README_EN.md"><strong>🇺🇸 English</strong></a> ·
  <a href="https://ai-work-team-demo.pages.dev"><strong>🔮 DEMO</strong></a> ·
  <a href="#quick-start"><strong>🚀 Quick Start</strong></a> ·
  <a href="#site-configuration"><strong>📔 Configuration</strong></a>
</p>

---

## ✨ Features

- 🌌 **3D Particle Cosmic Background**: 5,000+ feather-glow circular particles generated dynamically with Three.js, featuring smooth mouse interaction and sinusoidal breathing animation.
- 🧪 **4 Experimental Dark Themes**: One-click theme switcher in top-right Labs icon (Default Abyss, Cyberpunk Emerald, Nordic Aurora, Cosmic Amber) with real-time 3D particle color synchronization.
- 💫 **360° Rotating Stream Light Buttons**: Core CTAs with smooth clockwise laser stream borders and translucent highlighter sweep animations.
- 📱 **Single-Screen & Responsive**: Locked single-screen layout for homepage, with a rich, glassmorphic card-style About Studio page.

---

## Quick Start

Get your own galaxy portfolio up and running in 3 simple steps:

### Fork This Repository

Click the **Fork** button at the top right of this repository to copy it to your GitHub account, or clone it locally:

```bash
git clone https://github.com/FrankWkd-Plus/galaxy-theme-portfolio.git
cd galaxy-theme-portfolio
npm install
```

---

### Site Configuration

You only need to customize **3 files** to make it your own:

#### 🔹 1. Hero Content & Buttons (`src/components/Hero.astro`)
- Edit the greeting `HELLO, I'M` and `Outwardly Verse` main title text.
- Modify the `About Me` route and `Read Blog` external link.

#### 🔹 2. Top Navigation & GitHub Link (`src/components/Navigation.astro`)
- Change the brand logo name `Outwardly Verse`.
- Replace `https://github.com/FrankWkd-Plus` with your own GitHub profile URL in the top left and drawer menu.

#### 🔹 3. About Page & Skills (`src/pages/about.astro`)
- Edit studio name, slogan, and alert tip boxes.
- Modify or replace tech stack Shields.io badges in `.skills-matrix`.
- Fill in your projects and contact cards (Email, Xiaohongshu, Telegram, etc.) in `.projects-grid` and `.contacts-grid`.

---

### Deploy to Cloudflare Pages

1. Log into your [Cloudflare Dashboard](https://dash.cloudflare.com/), navigate to **Workers & Pages** -> **Create application** -> **Pages**.
2. Select **Connect to Git** and choose your forked GitHub repository.
3. Configure the build settings as follows:

| Setting | Value |
| :--- | :--- |
| **Framework preset** | `Astro` |
| **Build command** | `npm run build` |
| **Build output directory** | `dist` |
| **Root directory** | Leave empty (or `/`) |

4. Click **Save and Deploy**.

---

## 🛠️ Development & Contributing

```bash
# Start local development server
npm run dev

# Build production bundle
npm run build

# Preview production build locally
npm run preview
```

---

## 📄 License

This project is licensed under the [GNU General Public License v3.0 (GPL-3.0)](LICENSE).

---

<p align="center">
  Crafted with ❤️ by <a href="https://github.com/FrankWkd-Plus">FrankWkd</a>
</p>
