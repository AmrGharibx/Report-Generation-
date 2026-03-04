# RED Report Generator — AI-Powered Trainee Performance Reports

A complete, interactive web application for generating professional A4 trainee performance reports for **RED Real Estate Domain Training Academy**.

![License](https://img.shields.io/badge/license-MIT-blue)
![Deploy](https://img.shields.io/badge/deploy-GitHub%20Pages-brightgreen)

## Features

- **AI-Powered Data Extraction** — Upload evaluation screenshots and let AI (Google Gemini or OpenAI GPT-4o) extract all trainee scores automatically
- **Screenshot Upload** — Drag-and-drop or click to upload multiple images at once
- **Manual Entry** — Add trainee data manually without AI if preferred
- **Editable Review** — Verify and edit all extracted data before generating the report
- **Auto-Calculation** — Recalculate derived scores (tech %, soft %, overall %) from base scores
- **Per-Trainee AI Assessment** — Regenerate professional assessment paragraphs per trainee with one click
- **Pixel-Perfect A4 Reports** — Cover page, individual trainee pages, and concluding remarks — all formatted to A4
- **PDF Download** — Direct in-browser PDF generation (html2canvas + jsPDF)
- **Print Support** — Perfect print-to-PDF via browser print dialog
- **Persistent Settings** — API key and company info saved in localStorage

## Quick Start

### Option 1: GitHub Pages (Recommended)
1. Fork this repo
2. Go to **Settings → Pages → Source: main / root**
3. Your app will be live at `https://<username>.github.io/Report-Generation-/`

### Option 2: Open Locally
Just open `index.html` in Chrome or Edge. No server needed.

## How to Use

### Step 1 — Setup
Enter your company name, batch number, and AI API key.
- **Google Gemini** (recommended, free): Get a key at [aistudio.google.com/apikey](https://aistudio.google.com/apikey)
- **OpenAI GPT-4o** (paid): Get a key at [platform.openai.com](https://platform.openai.com/api-keys)

### Step 2 — Upload Screenshots
Upload evaluation spreadsheet screenshots. The AI will analyze them and extract all trainee data.
- Or click **Manual Entry** to skip AI and enter data by hand.

### Step 3 — Review & Edit
Verify extracted data. Click any trainee card to expand and edit fields.
- **Recalculate Scores** — auto-computes all derived percentages from base scores
- **Regenerate with AI** — rewrites the assessment paragraph for a specific trainee

### Step 4 — Report Preview
View the full A4 report. Then:
- **Download PDF** — saves directly as a PDF file
- **Print** — opens browser print dialog (use "Save as PDF" for best quality)

## Assessment Tiers

| Score | Result | Badge |
|-------|--------|-------|
| ≥ 90% | Aced | 🟢 Green |
| ≥ 80% | Excellent | 🔵 Blue |
| ≥ 70% | Good | 🟡 Yellow |
| ≥ 60% | Passed | ⚪ Gray |
| < 60% | Failed | 🔴 Red |

## Tech Stack

- **HTML/CSS/JS** — Single-file, zero dependencies (no framework, no build step)
- **Google Fonts** — Sora + Playfair Display
- **html2canvas** — DOM-to-canvas rendering for PDF
- **jsPDF** — Client-side PDF generation
- **Gemini / OpenAI API** — Vision-capable AI for screenshot analysis

## Score Calculation

```
totalCore = productKnowledge + mapping
techScore% = (totalCore / 10) × 100
conductRating = presentability + softSkills
softScore% = (conductRating / 10) × 100
overallScore = (techScore% + softScore%) / 2
```

## Privacy

- API keys are stored **only in your browser's localStorage**
- Screenshots are sent **directly to the AI provider you choose** (Google or OpenAI)
- No data is collected, stored, or sent to any third-party server
- The app runs 100% client-side

## License

MIT — use freely.
