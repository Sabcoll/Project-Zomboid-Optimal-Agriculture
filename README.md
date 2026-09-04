### Project Zomboid Sowing Calendar & Dynamic Growth Grid

An interactive, single-file HTML tool designed for Project Zomboid (Build 42) farming. It visualizes ideal sowing seasons and tracks crop growth timelines based on your in-game planting date.

## Features
* Overview Grid: Displays climate suitability ratings (Best/Good/Poor/Bad) and real-time growth phases across the entire year for every crop.

* Dynamic Grid Interval: Toggle timeline resolution from 1-day exact tracking up to 7-day intervals.

* Growth Phase Tracking: Visualizes active growth, Phase 6 (Harvest window), and Phase 7 (Seed blooming) derived from your chosen sowing date.

## Filter Views:

* By Month: Group crops by suitability for a specific month with direct harvest/seed date estimates.

* By Crop: Focus on an individual crop's full-year timeline and requirements.

* Zero Dependencies: Pure HTML/JS/CSS in a single file. Open index.html directly in any browser—no installation or web server required.

---

### Growth Phase Math & Accuracy

Growth time refers to the average number of days it takes a crop to reach phase 6.
Growth timelines are calculated relative to your selected sowing date:

* **Base Growth Time:** The crop's total base growth duration in days (e.g., 60 days for Broccoli, 240 days for Garlic).
* **Harvest Phase (Phase 6):** Begins immediately after the base growth period ends. Its duration scales dynamically as `max(3, round(base_days * 0.12))` days.
* **Seed Blooming Phase (Phase 7):** Begins immediately following Phase 6 and runs for the exact same duration (`max(3, round(base_days * 0.12))` days).

> **Note on Accuracy:** In-game growth rates in Project Zomboid are influenced by environmental variables (temperature, light, and soil quality). As a result, exact in-game phase shifts may vary by **1 to 2 days up to a few days ** compared to this calendar.
