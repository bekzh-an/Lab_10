# Lab 10 - Starter
# Lab 10 - Post Launch Tooling: User Analytics and Feedback

## Team
- **Your Name Here**
- **Partner's Name Here** *(if applicable)*

---

## Links

### 🗺️ Roadmap & Feature Requests (Canny)
> **[https://cse110-lab10-YOUR-GITHUB-USERNAME.canny.io](https://cse110-lab10-YOUR-GITHUB-USERNAME.canny.io)**
>
> ⚠️ Replace `YOUR-GITHUB-USERNAME` with your actual GitHub username after setting up Canny.

### 🌐 Live Site (GitHub Pages)
> **[https://YOUR-GITHUB-USERNAME.github.io/Lab10_Starter](https://YOUR-GITHUB-USERNAME.github.io/Lab10_Starter)**
>
> ⚠️ Replace with your actual GitHub Pages URL after deploying.

---

## Part 1 - Roadmap & Feature Requests

Feature requests were posted to Canny, including:

| Post Title | Status |
|---|---|
| Blue Background | In Progress |
| Speech Rate Control | Under Review |
| Character Counter | Open |
| Clear Button | Open |
| Pause/Resume Speech | Open |
| Pitch Control | Open |
| Save Favorite Voice | Open |

---

## Part 2 - Google Analytics A/B Test

The `index.html` page runs a 50/50 A/B test on background color:
- **Group A (white):** Default white background
- **Group B (blue):** `body.blue` class applied → light blue background (`#a8d8f0`)

Google Tag Manager tracks which group a user lands in via a 30-second timer trigger. If a user stays on the page for 30 seconds, a GA4 event fires indicating they kept their assigned background version.

### Tags
- `Wait 30s blue tag` — fires if `body` class contains `blue`
- `Wait 30s white tag` — fires if `body` class does not contain `blue`

### Screenshot
See `/screenshots/google-analytics.png` for evidence of both tags firing in Google Analytics Realtime.

---

## Setup Notes for Graders

1. `G-XXXXXXXXXX` in `index.html` should be replaced with the actual GA4 Measurement ID
2. `GTM-XXXXXXX` in `index.html` should be replaced with the actual GTM Container ID
3. Both tags must be published in GTM (not just previewed) for data to appear in GA

---

## File Structure

```
lab10/
├── index.html              # Party Horn page (A/B test lives here)
├── speechSynth.html        # Speech Synthesizer page (rate slider feature)
├── favicon.ico
├── assets/
│   ├── scripts/
│   │   ├── partyHorn.js
│   │   ├── speechSynth.js
│   │   └── js-confetti.browser.js
│   ├── styles/
│   │   └── global.css
│   ├── images/
│   │   ├── no-image.png
│   │   ├── smiling.png
│   │   ├── smiling-open.png
│   │   ├── air-horn.svg
│   │   ├── car-horn.svg
│   │   └── party-horn.svg
│   ├── icons/
│   │   ├── volume-level-0.svg
│   │   ├── volume-level-1.svg
│   │   ├── volume-level-2.svg
│   │   └── volume-level-3.svg
│   └── audio/
│       ├── air-horn.mp3
│       ├── car-horn.mp3
│       └── party-horn.mp3
└── screenshots/
    └── google-analytics.png   # Required: GA Realtime screenshot
```