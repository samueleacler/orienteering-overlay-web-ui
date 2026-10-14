# Orienteering Video Overlay HUD 🧭🏃‍♂️

A lightweight, web-based tool designed for orienteering content creators. It generates a real-time Head-Up Display (HUD) ready to be recorded over a green screen and superimposed onto your POV headcam footage (GoPro, DJI, etc.) using any video editing software like Final Cut Pro, Premiere Pro, or DaVinci Resolve.

## ✨ Features
- **Dynamic Leaderboard:** Import race results directly via Excel (`.xlsx`) or CSV. The leaderboard automatically calculates gaps and updates smoothly using broadcast-style FLIP animations whenever you punch a new control.
- **Leg Splits Panel:** A dynamic pop-up appears at the center of the screen at each control, showing the top 5 partial times for that specific leg before fading out.
- **GPX Data Sync:** Upload your `.gpx` track (from Garmin, Polar, Suunto) to display real-time **Heart Rate (bpm)** and calculated **Pace (min/km)**.
- **Long Race Support:** Seamlessly handles long-distance races, accurately parsing times over the 60-minute mark (H:MM:SS format).
- **Green Screen Ready:** The UI is set on a pure `#00FF00` background with contrasting white text and heavy drop shadows, optimized for flawless Chroma Key extraction.
- **Customizable Race Info:** Add your event name, category, and target athlete name directly from the UI.
- **No Installation Required:** Runs entirely in your local browser using vanilla HTML, CSS, and JS (with SheetJS for Excel parsing).

## 📊 How to Prepare the Results File (Excel)
You don't need to manually type the results or format them in a complex way. Just follow these quick steps:
1. Open the official split times/results page of your race (e.g., from your federation's website or WinSplits).
2. Highlight and copy the entire table of results for your category (make sure to select only the ranked/non-disqualified athletes).
3. Paste everything directly into a new, blank Microsoft Excel or Google Sheets document.
4. Save or export the file as `.xlsx` or `.csv`. 

## 🚀 How to Use

1. **Open the App:** Open `index.html` in any modern web browser.
2. **Load Data:**
   * Enter your name exactly as it appears in the results file.
   * Upload the race results you just created (`.xlsx` or `.csv`).
   * Upload your `.gpx` file containing Heart Rate data.
3. **Set Race Info:** Type the Event Name and Category.
4. **Record:** 
   * Set the slider to `0` (or your desired starting point).
   * Start your screen recording software (e.g., QuickTime Player on Mac, OBS).
   * Click **"▶ Avvia Tempo (1x) & Registra"** to start the real-time simulation.
5. **Video Editing:**
   * Import the screen recording into your NLE (Final Cut Pro, DaVinci Resolve).
   * Place it on the track above your headcam footage.
   * Apply a **Keyer / 3D Keyer** effect to remove the green background.
   * *Pro tip: Use the crop tool to remove the browser edges. The UI already has built-in shadows for perfect visibility over the footage.*

## ⌨️ Controls
- **Click anywhere** on the green background or press **ESC** to pause the timer and bring back the setup panel.
- Use the **Slider** to preview specific legs of the course before recording.

## 🛠 Tech Stack
- HTML5 / CSS3
- Vanilla JavaScript
- [SheetJS](https://sheetjs.com/) (for parsing Excel files locally)

## 📄 License
This project is open-source and available under the MIT License.
