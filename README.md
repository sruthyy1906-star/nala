# Nalayini — Professional Video Editor Portfolio

A premium, dark-cinematic, modern portfolio website built for **Nalayini** (Video Editor & Visual Storyteller).

---

## Features

- **Dark Cinematic Aesthetic**: Deep charcoal background, glowing radial ambient lighting, glassmorphism cards, and high-end video production visual style.
- **Hero Section**: Powerful intro with glowing profile avatar, status badges ("Available for Freelance"), and primary call-to-action buttons.
- **About Me Section**: Passionate bio, core values, and animated statistics cards (1+ Year Experience, 60+ Edits Completed, 5M+ Views reach).
- **Skills Showcase**: Filterable skill cards with proficiency indicators (Video Editing, Instagram Reels, YouTube Shorts, Color Grading, Motion Graphics, Audio Sync, etc.).
- **Software Suite**: Showcase cards for **CapCut Pro**, **Adobe Premiere Pro**, **After Effects**, and **DaVinci Resolve**.
- **Portfolio Lightbox**: Filterable video project grid (Instagram Reels, YouTube Shorts, Cinematic Edits, Commercial Promos, Music Cuts) with full embedded video playback modal.
- **Services Section**: 8 feature cards detailing specialized video editing services.
- **Work Timeline**: Clean vertical timeline detailing 1+ year editing history and milestones.
- **Creative Signature Section**: *"Every Frame Tells a Story."* film-strip showreel ticker with audio wave animation.
- **Interactive Contact Form**: Direct brief form with confetti celebration + editable direct links for Instagram, YouTube, WhatsApp, and Email.

---

## 1. How to Run the Project Locally

To run the dev server on your machine:

```bash
# 1. Install dependencies (if not already installed)
npm install

# 2. Start local dev server
npm run dev
```

Open the printed localhost URL (e.g. `http://localhost:5173`) in your browser.

To test building for production:
```bash
npx vite build
```

---

## 2. Where to Replace Profile Photo

You can replace Nalayini's profile photo in two ways:

1. **Option A (Recommended)**: Drop your image into `public/images/profile.png` (overwrite the existing photo file).
2. **Option B**: Open `src/data/portfolioData.js` and change `profilePhoto` to any image URL or file path:
   ```javascript
   export const personalInfo = {
     profilePhoto: "/images/your-new-photo.png",
     // ...
   };
   ```

---

## 3. Where to Add or Edit Portfolio Videos & Thumbnails

All portfolio items are controlled inside **`src/data/portfolioData.js`**.

To add a new video project, add an entry to the `portfolioProjects` array:

```javascript
{
  id: "p7",
  title: "My New Travel Reel",
  category: "Instagram Reels", // Choose from portfolioCategories
  aspectRatio: "9:16", // "9:16" for vertical or "16:9" for widescreen
  duration: "0:30",
  thumbnail: "/images/your-thumbnail.png", // Or external image URL
  videoUrl: "https://www.youtube.com/embed/YOUR_VIDEO_ID?autoplay=1",
  description: "Description of the edit, pacing, sound design, and style...",
  toolsUsed: ["CapCut Pro", "DaVinci Resolve"],
  views: "100K+",
  featured: true
}
```

To add or modify category tabs, edit `portfolioCategories` in `src/data/portfolioData.js`.

---

## 4. Where to Update Social Media Links & Contact Details

Open **`src/data/portfolioData.js`** and edit the `socials`, `email`, and `whatsapp` fields under `personalInfo`:

```javascript
export const personalInfo = {
  email: "your-real-email@gmail.com",
  whatsapp: "+919876543210",
  location: "Available Worldwide (Remote)",
  socials: {
    instagram: "https://instagram.com/your-username",
    youtube: "https://youtube.com/@your-channel",
    whatsapp: "https://wa.me/919876543210",
    email: "mailto:your-real-email@gmail.com"
  }
};
```

---

## 5. Where to Edit Skills, Software Tools & Services

All section contents are organized cleanly in **`src/data/portfolioData.js`**:

- **Skills**: Update `skillsData` array.
- **Software Tools**: Update `toolsData` array (add, remove, or replace tools like CapCut, Premiere Pro, After Effects, DaVinci Resolve).
- **Services**: Update `servicesData` array (8 services provided).
- **Timeline**: Update `experienceTimeline` array.

---

## Tech Stack

- **Framework**: React 19 + Vite 6
- **Styling**: Tailwind CSS v3 + Custom Dark Glassmorphism CSS
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Confetti FX**: Canvas Confetti
