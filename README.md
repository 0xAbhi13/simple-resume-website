# Simple Resume Website — Veda Technology Internship, Day 3

Online resume of **Abhishek Shahaji Jadhav** — Web Developer & first-year BCA
student at VIIT, Baramati. Built with **HTML5 + CSS3 only**: no frameworks, no
JavaScript, no build step, no external assets.

## My Approach

1. **Read the brief first:** single-page resume, HTML5 + CSS3 only, semantic
   markup, responsive layout, honest content (no invented contact details,
   experience, or stats).
2. **Verified real data:** used only verified public links — portfolio,
   LinkedIn, GitHub, tribute-page repo, and personal-introduction-page
   (live site + repository). Project descriptions match what each project
   actually is (checked live pages + repos).
3. **Built mobile-up:** semantic landmarks (`header`/`main`/`section`/`footer`,
   single `h1`), CSS custom properties for the white / dark-navy / electric-blue
   theme, Flexbox for components, Grid for the hero/skills/projects layouts,
   two breakpoints (920px, 680px), and a CSS-only checkbox hamburger menu so no
   JavaScript was needed.
4. **Made the download real:** generated a valid `resume.pdf` with the same
   resume content and added a `@media print` stylesheet, so both the button and
   `Ctrl+P → Save as PDF` produce a clean resume.
5. **Tested honestly:** ran a 44-check static suite (HTML structure, link
   targets, CSS tokens, PDF validity) plus a local HTTP serve test, and fixed
   what failed before submitting.

## Outcome

A complete, responsive, dependency-free resume website: sticky nav, hero with
three working buttons, About, Education, Skills, Projects, Internship, Contact,
and footer — with a real downloadable `resume.pdf`, clean print output, and no
console errors (there is no JavaScript). Ready to push to the public
`internship-task-3` repo and deploy on GitHub Pages or Vercel.

## Features

- Sticky header with text brand and CSS-only mobile menu (checkbox hack, no JS)
- Hero with name, role, intro, and three working buttons:
  `View Projects` → `#projects`, `Download Resume` → real `resume.pdf`,
  `Contact Me` → `#contact`
- Sections: About, Education, Technical Skills, Projects, Internship, Contact, Footer
- Honest content only — no invented phone/email, employment history,
  certificates, stats, or testimonials
- Projects: Personal Portfolio, Personal Introduction Page (live site +
  repository), and Tribute Page — each described as what it actually is
- Responsive Flexbox/Grid layout with tablet and mobile breakpoints
- Accessibility: skip link, semantic landmarks, single `h1`, focus-visible
  states, AA-safe link colour (`#1d4ed8` on white), descriptive link labels,
  `rel="noopener noreferrer"` on external links
- Print stylesheet (`@media print`) for a clean one-paper resume
- Local SVG favicon, system font stack (works offline)

## Technologies Used

| Technology | File / Use |
|---|---|
| HTML5 | `index.html` — semantic structure |
| CSS3 | `style.css` — custom properties, Flexbox, Grid, media queries, print |
| PDF | `resume.pdf` — real downloadable resume (generated with ReportLab, committed) |
| Git + GitHub / Vercel | Hosting (static, no build) |

No React, Vite, Bootstrap, Tailwind, JS frameworks, or paid libraries.

## Folder Structure

```text
internship-task-3/
├── index.html
├── style.css
├── resume.pdf
├── README.md
├── vercel.json      # static deployment config (no build, clean URLs)
├── .gitignore
└── assets/
    └── favicon.svg
```

(The brief names this `day-3-resume-website/`; the submission repository is
`internship-task-3`, so the repo root uses that name with the same layout.)

## How to Run Locally

No install needed. Any of these works:

```powershell
# Option 1 — just open it
Start-Process index.html

# Option 2 — local server (recommended, avoids file:// quirks)
python -m http.server 8000
# then open http://localhost:8000

# Node alternative
npx serve .
```

## How to Deploy — GitHub Pages

1. Create a repo named `internship-task-3` on GitHub (do **not** add secrets).
2. From inside this folder:
   ```powershell
   git init -b main
   git add index.html style.css resume.pdf README.md assets
   git commit -m "Day 3: Simple Resume Website (HTML + CSS)"
   git remote add origin https://github.com/0xAbhi13/internship-task-3.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Deploy from a branch → `main` / root**.
4. Live URL: `https://0xabhi13.github.io/internship-task-3/`

## How to Deploy — Vercel

1. Push the repo as above.
2. Go to <https://vercel.com> → **Add New → Project → Import** `internship-task-3`.
3. Framework preset: **Other**. No build command, no output directory, no env vars.
4. Deploy → you get `https://internship-task-3-*.vercel.app`.

## How to Print / Export the Resume to PDF

- **Download button:** click `Download Resume` in the hero (serves the included `resume.pdf`).
- **From the page:** press `Ctrl + P` (or `Cmd + P`) → destination **Save as PDF**.
  The `@media print` stylesheet hides the header, buttons, and decorative
  background and compacts sections to fit cleanly on paper.
- **Regenerate `resume.pdf`** (optional, needs Python + ReportLab): re-run a
  ReportLab script with the same resume text and save the output as
  `resume.pdf` in the repo root.
  The committed `resume.pdf` is already valid (`%PDF-` header, `%%EOF` trailer).

## Accuracy Notes

- No phone number or email is listed anywhere — contact is via portfolio/LinkedIn.
- Skills are presented as *learning/using*, with no proficiency bars.
- Internship is described as *ongoing, project-based learning* (started 10 Oct 2026).
- Project links verified live: portfolio, personal-introduction-page
  (live + repo), tribute-page (live + repo).
