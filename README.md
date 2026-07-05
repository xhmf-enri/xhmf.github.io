# XHMF Website — Cinematic Rebuild

A modern, cinematic rebuild of the Xheladin & Xhufe Morina Foundation website — full-bleed brain/neuroscience photography, bold lowercase typography, film-grain texture, and vintage color grading inspired by editorial sites like wearebrand.io.

## What's inside

```
xhmf-site/
├── index.html                  ← Home (full-bleed cinematic hero)
├── about.html                  ← About / Team (brain-scan header)
├── news_updates.html           ← Mission (EEG header)
├── enri.html                   ← Research (neurons header)
├── braincamp.html              ← BrainCamp program (neurons header)
├── brainbook.html              ← BrainBook (neurons header)
├── bci-initiative.html         ← BCI Initiative (EEG header)
├── climatecamp.html            ← ClimateCamp (climate header)
├── scholarships.html           ← Scholarship recipients (brain-scan header)
├── events.html                 ← Events (neurons header)
├── partnerships.html           ← Partners (neurons header)
├── testimonials.html           ← Testimonials (neuron-macro header)
├── media.html                  ← Press & media (EEG header)
├── information-for-students.html  ← Student resources (EEG header)
├── application.html            ← Application form (brain-scan header)
├── robots.txt
├── sitemap.xml
└── assets/
    ├── style.css               ← All styling (also inlined into each HTML)
    ├── main.js                 ← Interactions (also inlined into each HTML)
    ├── logo.svg + logo.png     ← Your real XHMF logo (also inlined)
    ├── founder.jpg             ← Dr. Egzona Morina photo
    ├── hero-bg.jpg             ← Cinematic brain hero image
    ├── neurons.jpg             ← Glowing neurons
    ├── brain-scan.jpg          ← MRI slices
    ├── eeg.jpg                 ← EEG monitor
    ├── neuron-macro.jpg        ← Single neuron macro
    ├── climate.jpg             ← Climate scene
    ├── ucl.png, fens.jpg, gcha.png  ← Partner logos
```

## Design system

- **Typography:** Space Grotesk (bold lowercase display) + Inter (body)
- **Color palette:** Brand teal `#28D5BC` + coral `#FA798E` on warm cream `#fbf8f1` + ink `#1a1a1a`
- **Film grain:** Animated SVG noise overlay (opacity 0.18, mix-blend overlay) — gives the "old camera" feel
- **Vintage color grading:** `sepia(0.15) saturate(1.2) contrast(1.1) brightness(0.85)` on all photos
- **Warm vignette:** Subtle radial darkening at edges
- **Navigation:** Transparent over hero, blurs to solid cream on scroll
- **Page headers:** Full-bleed cinematic photography with dark gradient overlay

## How to upload to GoDaddy

### Option A — cPanel File Manager (easiest)

1. Log in to your GoDaddy account → **Web Hosting** → **Manage**.
2. Click **cPanel Admin** → **File Manager**.
3. Open the `public_html` folder.
4. **Back up your old site first** — select all existing files, right-click → **Compress** → name it `old-site-backup.zip`, download it.
5. Delete the old files inside `public_html` (except `cgi-bin` if present).
6. Click **Upload** and upload everything inside `xhmf-site/` (HTML files, the `assets` folder, `robots.txt`, `sitemap.xml`) directly into `public_html`. Don't put them in a subfolder.
7. Visit `https://xhmf.org` — your new site is live.

### Option B — FTP (FileZilla)

1. In GoDaddy cPanel, find your FTP credentials (cPanel → FTP Accounts).
2. Connect with: host `ftp.xhmf.org`, your cPanel username and password.
3. Open `public_html` on the right side.
4. Navigate to your extracted `xhmf-site/` folder on the left.
5. Select all files and drag them into `public_html`.

## Updating content

Every page is self-contained HTML — open in any text editor (VS Code, Notepad++, TextEdit) and edit text directly. The CSS and JS are inlined into each file, so changes to style.css need to be re-applied (or just edit the `<style>` block in the specific page).

### Common edits

- **Donation link:** Search for `paypal.com/donate` and replace with your real donation URL.
- **Application form:** Currently a demo. To receive submissions, sign up at [Formspree](https://formspree.io) (free), then change `<form class="form-card reveal" data-demo>` to `<form class="form-card reveal" action="https://formspree.io/f/your-id" method="POST">` and remove `data-demo`.
- **BrainCamp dates:** Edit `braincamp.html` and `index.html`.
- **Hero image:** Replace `assets/hero-bg.jpg` with any 1344×768+ image.

## Features

- ✅ Cinematic full-bleed hero with brain imagery on every page
- ✅ Bold lowercase typography (wearebrand.io-inspired)
- ✅ Animated film-grain texture overlay site-wide
- ✅ Vintage color grading (sepia + warm tones)
- ✅ Warm vignette at edges
- ✅ Transparent navigation that blurs on scroll
- ✅ Fully self-contained — every page is one HTML file (CSS, JS, logo all inlined)
- ✅ Works perfectly when opened directly from file system
- ✅ Fully responsive (mobile, tablet, desktop)
- ✅ SEO meta tags, Open Graph, sitemap.xml, robots.txt
- ✅ Real founder photo, real partner logos, real XHMF logo
- ✅ Custom AI-generated neuroscience imagery (brain, neurons, EEG, MRI)
- ✅ Reduced-motion friendly (accessibility)

## Tech notes

- Fonts load from Google Fonts CDN (cached after first visit).
- All images are pre-generated and bundled — no external image dependencies.
- The film-grain animation is pure CSS (no JS) and pauses for users with `prefers-reduced-motion`.
- Total site is ~1.1MB (mostly the photographic backgrounds).

---

Built July 2026.
