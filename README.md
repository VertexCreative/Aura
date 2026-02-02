# AURA | Studio Audio Engine 🎧

![Version](https://img.shields.io/badge/VERSION-2.0_STUDIO-8b5cf6?style=for-the-badge)
![Tech](https://img.shields.io/badge/CORE-WEB_AUDIO_API-000000?style=for-the-badge)
![Status](https://img.shields.io/badge/STATUS-STABLE-00ff41?style=for-the-badge)
![License](https://img.shields.io/badge/LICENSE-MIT-ffffff?style=for-the-badge)

## 📂 Overview

**AURA (Audio Universal Rendering Architecture)** is a high-fidelity, browser-based audio visualization engine developed by **Vertex Creative**. 

Unlike standard visualizers that use basic volume metering, AURA utilizes a **Symmetric Dual-Channel Rendering** engine built on the HTML5 Canvas and the advanced Web Audio API. It processes raw audio frequency data (FFT) in real-time, applying liquid smoothing algorithms to create a cinematic, studio-grade visual experience.

> **Visual Logic:** 2048 FFT Size // 0.85 Smoothing Constant // Symmetric Mirroring.

---

## ✨ Key Features

### 🎚️ Studio-Grade Audio Engine
* **High-Res Analysis:** Uses an FFT (Fast Fourier Transform) size of `2048` for ultra-precise frequency detection (Bass, Mids, Highs).
* **Liquid Smoothing:** Implements `smoothingTimeConstant` logic to prevent visual jitter, resulting in fluid, organic motion.
* **Symmetric Rendering:** Visuals are mirrored from the center-out (Dual-Channel), creating a balanced, Rorschach-test style aesthetic.

### 🎨 Professional UI (One UI Style)
* **Glassmorphism Shell:** The interface floats on a blurred, saturated backdrop using `backdrop-filter: blur(30px)`.
* **Dynamic Gradient:** Frequency bars transition dynamically from **Cyan** to **Purple** to **Deep Blue** based on amplitude.
* **Interactive Controls:**
    * **Seek Bar:** Draggable progress bar to jump to specific timestamps.
    * **Volume Fader:** Precision audio level control.
    * **Local File Support:** Built-in file reader to process user-uploaded MP3/WAV files.

---

## 🚀 Installation & Setup

**⚠️ CRITICAL:** Due to browser security policies regarding the **Web Audio API** and local file access (CORS), this application **must** be run on a local server. It will not function correctly if you simply double-click the HTML file.

### 1. Folder Structure
Ensure your project folder looks like this:
```text
/Aura-Engine
  ├── index.html        (Rename aura.html to index.html for standalone use)
  ├── README.md
  └── assets/           (Optional: For local icons if not using CDN)
### 2. How to Run

**Option A: VS Code (Recommended)**
1.  Open the `Aura-Engine` folder in **VS Code**.
2.  Install the **"Live Server"** extension (by Ritwick Dey).
3.  Right-click `index.html`.
4.  Select **"Open with Live Server"**.

**Option B: Python Terminal**
1.  Open your terminal or command prompt in the project folder.
2.  Run the following command to start a local server:
    ```bash
    python -m http.server
    ```
3.  Open your web browser and navigate to `localhost:8000`.```

---

## 🕹️ User Manual

1.  **Launch:** Open the application in your browser.
2.  **Upload:** Click the **Upload Icon** (Top Right) or the central **Play Button** to select an audio file (MP3, WAV, OGG) from your computer.
3.  **Playback Controls:**
    * **Play/Pause:** Toggle audio playback.
    * **Skip:** Use the arrows to jump +/- 10 seconds.
    * **Seek:** Drag the progress slider to jump to a specific timestamp.
    * **Volume:** Hover over the speaker icon to reveal the precision fader.
4.  **Visualizer:** The engine will automatically detect the audio stream and begin rendering the symmetric frequencies.

---

## 💻 Technical Stack

* **Core:** HTML5 Canvas, Vanilla JavaScript (ES6+).
* **Audio Engine:** Web Audio API (`AudioContext`, `AnalyserNode`, `MediaElementSource`).
* **Smoothing Logic:** `analyser.smoothingTimeConstant = 0.85`.
* **Styling:** Tailwind CSS (via CDN).
* **Icons:** Lucide Icons (via CDN).

---

## 📄 License

**Vertex Creative Inc.**
Open Source (MIT License).
*Built by Zephyr*

> *Built for the Architects of the Future.*
