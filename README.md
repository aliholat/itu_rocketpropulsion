# IGNITION — UZB441E Rocket Propulsion Midterm Lab

Interactive static study website for the **ITU UZB441E first midterm — 05 November 2026**. Built as a simple GitHub Pages project with HTML, CSS and vanilla JavaScript. No server, database, framework, installation or API key required.

## Files

- `index.html` — application skeleton and MathJax loader
- `styles.css` — responsive dark interface, diagrams, print layout
- `content.js` — exam notes: derivations, conceptual Q&A, calculations and quizzes
- `app.js` — navigation, SVG schematics/graphs, quizzes, calculator and persistence

## GitHub Pages (Türkçe kurulum)

1. [github.com](https://github.com/) hesabına gir ve **New repository** oluştur. Örneğin ad: `rocket-propulsion-midterm`. Repository **Public** olabilir.
2. Repository sayfasında **Add file → Upload files** seçeneği ile bu klasörün içindeki **dört dosyanın kendisini** (`index.html`, `styles.css`, `content.js`, `app.js`) yükle. ZIP dosyasını tek başına yükleme; ZIP'i bilgisayarında aç ve dosyaları ayrı ayrı yükle. `index.html` depo ana dizininde olmalı.
3. **Commit changes** butonuyla kaydet.
4. **Settings → Pages → Build and deployment** yolunda **Source: Deploy from a branch** seç. **Branch: main** ve **Folder: /(root)** olarak ayarlayıp **Save** de.
5. Yayın adresin `https://KULLANICI_ADIN.github.io/rocket-propulsion-midterm/` biçiminde olur. GitHub'ın Pages sayfasında gerçek bağlantıyı görebilirsin.
6. Sonraki güncellemede `content.js` veya diğer dosyaları repository üzerinden değiştirip commit et. Aynı adres güncel sürümü açar.

## Features

- 34 openable, step-by-step equation derivations with assumptions and exam traps
- Original labeled SVG diagrams: C–D nozzle, liquid bipropellant, solid, hybrid, electric ion thruster, expansion regimes
- γ-adjustable quasi-1D graphs: area–Mach, isentropic ratios, choked mass flux, ideal CF versus back pressure
- Worked examples, including lecture Sutton 3-3 and 3-4
- Typical Isp and propulsion-system thrust-to-weight lecture table
- High-yield conceptual questions and 12 lecture nozzle-model assumptions
- Interactive auto-scoring quiz, written prompts and flip flashcards
- Live ideal choked-nozzle performance calculator
- Printable formula sheet via Ctrl+P or browser Print → Save as PDF
- Local browser storage only for mastery and multiple-choice answers; no account needed
- Search with `/` key. Mobile responsive.

## Scope and caveats

The main scope comes from `01-Introduction3`, `02-DefinitionsFundamentals`, `03-NozzleThermodynamicRels2` and the UZB441E 2026–27 syllabus, with worked examples aligned to Sutton & Biblarz (2016). **Flight Performance**, scheduled for after Midterm 01, is not treated as a primary module; the ideal rocket equation appears as an explicit bonus derivation. This study aid is a new explanatory resource; it is not an official answer key. Verify against lecture conventions.

Most plots and the calculator assume a steady, adiabatic, inviscid, frozen-composition, perfect-gas, quasi-1D isentropic nozzle. The ideal exit Mach solution may be invalid when internal shocks or separation occur. The pressure-change calculation and pressure-vs-altitude interpretations have stated fixed-engine assumptions.

The website runs in your browser; its typeset LaTeX equations load **MathJax from a CDN** and fonts load via Google Fonts. An internet connection is therefore needed for polished mathematical notation. The text, calculations, diagrams and quizzes do not require a backend. The site can be served locally with `python -m http.server 8000` and opened at `http://localhost:8000`.

© Educational original notes and diagrams; not an official ITU website.
