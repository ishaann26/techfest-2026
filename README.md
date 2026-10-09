# TECHFEST 2026: BEYOND THE SINGULARITY ⚛️

A futuristic, 3D interactive web application for **TECHFEST 2026**, built with React, Vite, TypeScript, Tailwind CSS, Three.js (React Three Fiber & Drei), GSAP, and Framer Motion.

---

## 🚀 FEATURES OVERVIEW

1. **Futuristic Hero Scene**: Fullscreen WebGL 3D Canvas featuring an interactive rotating Reactor Core with inner/outer floating tech rings, real-time mouse tracking parallax, dynamic energy rings, particles, and volumetric light effects.
2. **Scrollytelling Journey**: Multi-chapter visual narrative ("THE SINGULARITY CONVERGENCE", "QUANTUM CRYPTOGRAPHY", "AUTONOMOUS ROBOTICS", "INTERPLANETARY FRONTIERS") with interactive tab navigation and technical architecture specs.
3. **3D Events Explorer**: Showcase of 7 flagship competitions (AI Innovation Lab, Cyber Arena, Bot Wars, Gameverse, Code Storm, Startup Launchpad, Space Explorers). Includes interactive 3D geometry icons, category filters, hover highlights, and detailed glassmorphism modals.
4. **Interactive 3D Robot Mascot (NEXUS-9)**: Real-time head tracking 3D mascot that idles, rotates, reacts to cursor position, and responds with tech facts, hackathon advice, audio blips, and festival lore when clicked.
5. **Festival Experience Highlights & Stats**: Interactive track overview and animated key statistics ($50,000+ Prize Pool, 5,000+ Participants, 25+ Events, 120+ Colleges).
6. **Live Countdown & Spatial Timeline**: Real-time ticker counting down to the festival launch date (October 24, 2026), paired with a spatial roadmap of event milestones.
7. **Portal Registration Form**: Fully validated registration interface with field checks, demo payload submission feedback, celebratory confetti, and audio synthesis.
8. **Accessibility & Audio Controls**: Integrated Web Audio API sci-fi synthesizer, sound toggle (default muted until gesture), and one-click Reduced Motion toggle.

---

## 🛠️ TECHNICAL STACK

- **Frontend Framework**: React 19 + TypeScript
- **Build Tool**: Vite 6 + Tailwind CSS v4 (`@tailwindcss/vite`)
- **3D Graphics & Canvas**: Three.js, `@react-three/fiber`, `@react-three/drei`
- **Animations & Transitions**: GSAP, Framer Motion, Canvas Confetti
- **Icons**: Lucide React
- **Audio Engine**: Custom Web Audio API Synthesizer (`src/utils/audio.ts`)

---

## 📦 INSTALLATION & DEV SERVER LAUNCH

### Prerequisites
- Node.js v18+ or v24+
- npm v9+ or npm v11+

### Step-by-Step Launch Instructions

1. **Navigate to project directory**:
   ```bash
   cd techfest-2026
   ```

2. **Install dependencies** (if not already installed):
   ```bash
   npm install
   ```

3. **Start local development server**:
   ```bash
   npm run dev
   ```
   Open your browser at `http://localhost:5173` to explore the experience.

4. **Build for production**:
   ```bash
   npm run build
   ```
   The compiled distribution files will be located in the `dist/` directory.

5. **Preview production build**:
   ```bash
   npm run preview
   ```

---

## ⚙️ CONFIGURATION & CUSTOMIZATION GUIDE

### 1. Updating Event Information & Prizes
Edit `src/utils/eventsData.ts`:
- Modify title, description, date, venue, team size, prize pool, status (`Open`, `Filling Fast`, `Limited Slots`), rules, or schedule.

### 2. Updating Countdown Date & Timeline
Edit `src/components/FestivalTimeline.tsx`:
- Update `FESTIVAL_START_DATE`:
  ```typescript
  const FESTIVAL_START_DATE = new Date('2026-10-24T09:00:00+05:30');
  ```
Edit `src/utils/timelineData.ts` to add or update roadmap phases and milestone descriptions.

### 3. Customizing Robot Mascot (NEXUS-9) Dialogue
Edit `src/utils/mascotFacts.ts`:
- Add or update dialogue items in `MASCOT_DIALOGUES` array with custom tips, facts, or lore.

### 4. Integrating a Backend for Registration
In `src/components/RegistrationForm.tsx`, replace the `setTimeout` block in `handleSubmit` with your backend endpoint:
```typescript
const response = await fetch('https://your-api.com/api/register', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(formData),
});
```

---

## 📄 LICENSE

Designed and engineered for **TECHFEST 2026**.
