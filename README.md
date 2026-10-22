# Job Tracker Dashboard

**A visual job application tracker that turns your search into a live flow diagram.**

<p align="left">
  <a href="https://jobtracker08.netlify.app/"><img src="https://img.shields.io/badge/Live%20Demo-Open%20App-2ea44f?style=for-the-badge&logo=netlify&logoColor=white" alt="Live Demo"></a>
  <a href="https://www.linkedin.com/in/neel-nagesh-bandiwadekar-478737272/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://github.com/neelbandiwadekar08-hub"><img src="https://img.shields.io/badge/GitHub-Profile-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
</p>

<p align="left">
  <a href="https://github.com/neelbandiwadekar08-hub/job-tracker-dashboard/stargazers"><img src="https://img.shields.io/github/stars/neelbandiwadekar08-hub/job-tracker-dashboard?style=flat&logo=github" alt="Stars"></a>
  <a href="https://github.com/neelbandiwadekar08-hub/job-tracker-dashboard/commits/main"><img src="https://img.shields.io/github/last-commit/neelbandiwadekar08-hub/job-tracker-dashboard?style=flat" alt="Last commit"></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat" alt="MIT License"></a>
  <img src="https://img.shields.io/badge/React-18-61DAFB?style=flat&logo=react&logoColor=black" alt="React 18">
  <img src="https://img.shields.io/badge/Tailwind-CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/Built%20with-Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white" alt="Built with Gemini">
  <img src="https://img.shields.io/badge/Storage-Local%20Only-orange?style=flat" alt="Local storage only">
</p>

<!--
  DEMO VIDEO: delete this comment block, then drag your video file into the
  GitHub editor at this spot. GitHub will insert the link automatically.
-->

---

## Why I built this

Every job tracker I tried had the same design: a spreadsheet, a dropdown, a status. It worked as a list, but it could not show me what was actually happening inside my search.

I wanted to see where applications moved forward and where they stalled. So I built a tracker that shows the whole pipeline at once instead of listing it row by row.

## What it does

Every application moves through a live flow diagram (a Sankey diagram), from submitted through to offer. The diagram is the main interface, not a decoration: it reacts to your clicks and filters.

## Features

- **Interactive Sankey diagram.** Click any stage and the dashboard filters to just those applications. Hover over a stage to see the exact numbers.
- **Live insight cards.** Total applications (with how many are still active), interview rate, and offer conversion, calculated from your data.
- **Role filters.** Narrow everything by Working Student, Internship, Master's Thesis, or Full-time. The diagram redraws around the selected role.
- **Search and stage filter.** Search by company, position, or location, or filter by stage from a dropdown.
- **Add, edit, and delete.** Manage applications through a form with company, position, role type, stage, location, applied date, salary or stipend, notes, and the job posting link.
- **JSON export.** Download all your data as a dated JSON file whenever you want a backup.
- **Light and dark mode.** Your theme preference is remembered.
- **Runs locally.** Data is stored in your browser, so there is no account, no server, and nothing leaves your device.
- **Preloaded demo data.** Opens with 52 sample applications so you can explore the diagram right away.

## How the insights are calculated

| Metric | Formula |
| --- | --- |
| Interview rate | Applications that reached Interview or later, divided by total applications |
| Offer conversion | Applications that reached Offer or later, divided by applications that reached Interview or later |

Both recalculate instantly whenever your data changes.

## Tech stack

- **React 18** for the interface and state
- **Tailwind CSS** for styling
- **Custom SVG** for the Sankey diagram, built without a charting library
- **Babel Standalone** to run JSX directly in the browser
- **localStorage** for persistence
- Delivered as a **single self-contained HTML file**, no build step required

## How I built it

I built this by directing Gemini: I described the problem from my own job search routine and what I wanted the dashboard to do, and Gemini generated the code. The app is hosted so it can be opened from a link.

## Getting started

No installation needed.

1. Clone the repository, or download `index.html`.
   ```bash
   git clone https://github.com/neelbandiwadekar08-hub/job-tracker-dashboard.git
   ```
2. Open `index.html` in any modern browser.

The app loads its libraries from a CDN, so an internet connection is needed on first load.

## Data and privacy

All application data is stored in your browser's local storage on your own device. Clearing your browser data removes it, so use the JSON export if you want a backup.

## Known limitations

- The **Avg. Response Time** card currently shows a default value, because the app does not yet collect response dates. It is not calculated from your entries.

## Sample data notice

The companies, positions, and statuses shown in the demo are a **sample dataset for demonstration purposes only**. They are not my real applications, and they do not reflect real hiring decisions by any company named.

## Author

**Neel**
Master's student in Global Production Engineering, TU Berlin

[LinkedIn](https://www.linkedin.com/in/neel-nagesh-bandiwadekar-478737272/) | [GitHub](https://github.com/neelbandiwadekar08-hub)
