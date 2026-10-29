# Institutional Governance & Complaint Monitoring System

An AICTE-aligned, integrated dashboard for monitoring and tracking institution-related complaint cases across bureaus and cells. Built for **Smart India Hackathon 2026 – Problem Statement 26264** (AICTE, Regulation Bureau).

> **Demo environment:** all records are fictional sample data. Changes are stored only in your browser (`localStorage`).

## Features

| Section | Modules |
|---|---|
| **Overview** | Central Dashboard, Live Monitoring |
| **Institution** | Institution Profile, Institutional Risk Signals, Issue Relationship Map |
| **Case Management** | Complaint Tracking, Action Gap Detector, Overlap Detection, Action History, Complaint Blind-Spot Detector, Complaint view |
| **Intelligence & Evidence** | Department Dependencies, Evidence Provenance, Explainable Priority Engine |
| **Administration** | Search & Filters, Alerts & Notifications, Reports & Analytics (printable) |

Also includes light/dark theme, SLA tracking, explainable risk scoring and a reset-to-original-data option.

## Tech Stack

- HTML, CSS and vanilla JavaScript (single `index.html`, no build step)
- [Chart.js 4.4.1](https://www.chartjs.org/) via jsDelivr CDN
- Browser `localStorage` for demo state
- Hosted on [Vercel](https://vercel.com/) (`vercel.json` adds SPA rewrites and security headers)

## Project Structure

```
AICTE Project/
├── index.html    # Entire application (UI, data, logic)
├── vercel.json   # Vercel routing + security headers
└── README.md
```

## Run Locally

No installation needed. Either open `index.html` in a browser, or serve it:

```bash
# Python
python -m http.server 5500

# or Node
npx serve .
```

Then visit `http://localhost:5500`. (Internet is needed for the Chart.js CDN.)

## Deployment

### 1. Push to GitHub

```bash
git add .
git commit -m "Add README"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git   # skip if origin already set
git push -u origin main
```

### 2. Deploy on Vercel

1. Sign in at [vercel.com](https://vercel.com) with GitHub.
2. Click **Add New → Project** and import the repository.
3. Settings: **Framework Preset:** `Other` · **Build Command:** leave empty · **Output Directory:** leave empty (root) · **Install Command:** leave empty.
4. Click **Deploy**. Your site goes live at `https://<project-name>.vercel.app`.

Every later `git push` to `main` redeploys automatically.

## Notes

- Data is illustrative; risk scores and priorities use demonstration rules, not official AICTE criteria.
- Use the in-app reset to restore the original sample records.

## Team

Team ScienceDot — Rajalakshmi Institute of Technology (RIT), Dept. of Computer Science and Engineering.
