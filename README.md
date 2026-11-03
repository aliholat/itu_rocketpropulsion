# IGNITION — UZB441E Rocket Propulsion Midterm Lab

Static, interactive exam-preparation website for **ITU UZB441E Rocket Propulsion, Midterm 1 (5 November 2026)**. Works on GitHub Pages with no backend, account or database.

## IMPORTANT: Lecture notation comes first

The site now has two **separate** equation banks:

- **LECTURE SLIDE EQUATIONS (69 cards)** — written with the lecturer's primary symbols **k**, **p₁**, **T₁**, **Aₜ**, **pₜ**, **A₂**, **p₂**, **p₃**, **uₜ**, **u₂**, **Iₛ**, **V** (specific volume), **Cꜰ**, **c*** and **ε**. Page references point to the actual class presentations.
- **ADDITIONAL / ALTERNATIVE (34 cards)** — common textbook forms using **γ**, **A***, **pₑ**, **p₀**, **vₑ**, **Isp**. These are not mixed with the main slides. Note that the lecturer occasionally uses `p₀,T₀` explicitly for stagnation quantities on lecture 03 page 4; this is preserved where it occurs.

**Priority formula:** `Aₜ/Aᵧ` from lecture 03 page 10, expressed as the full pressure-ratio relation, is the first card in **Derivations → 03 · Area / sizing**. The derivation has **34 numbered individual steps**, beginning with continuity and continuing through isentropic thermodynamics, exit/throat velocities, exponent manipulation and area-ratio verification.

Other important relationships such as **area–Mach**, **choked mass flow**, **critical throat conditions**, **exhaust velocity**, **thrust**, **thrust coefficient**, **characteristic velocity**, **propulsive efficiency** and **sound speed** have expanded no-skipped-algebra breakdowns. The lecture bank now contains **364 numbered derivation steps** in total, plus textual physical explanations, units, conditions and common exam traps. Self-evident definitions naturally require fewer steps than multistage derivations.

**Course-specific mass ratio:** lecture 02 p.2 uses **MR = m_f/m₀**, with **ζ = 1 − MR**. That is deliberately different from some books' inverse convention.

## Deploy to GitHub Pages (Türkçe)

1. Bu ZIP'i çıkar. ZIP dosyasını GitHub'a tek bir dosya olarak yükleme.
2. GitHub'da **New repository** oluştur (ör. `rocket-propulsion-midterm`). İstersen Public yap.
3. **Add file → Upload files** ile `index.html`, `styles.css`, `content.js`, `slides.js`, `deep-derivations.js`, `app.js`, `README.md` dosyalarını **ve `vendor/` klasörünün içindeki iki dosyayı** yükle. Dizin yapısını koru: `index.html` en üst dizinde kalmalı, MathJax dosyası `vendor/mathjax-tex-svg.js` yolunda olmalı.
4. **Commit changes** seç.
5. **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save** seç.
6. Site adresi `https://GITHUB_KULLANICI_ADIN.github.io/rocket-propulsion-midterm/` biçiminde olur.
7. Daha sonra içeriği güncellemek için ilgili dosyaları repository'de değiştirip **Commit changes** yapman yeterli.

İpucu: Bir formülü geliştirmek istersen asıl kartlar `slides.js`, genişletilmiş ayrıntılı çözümler `deep-derivations.js`, ek kitap formülleri `content.js` içindedir.

## Layout

```text
index.html
styles.css
content.js
slides.js
deep-derivations.js
app.js
README.md
vendor/
    mathjax-tex-svg.js
    LICENSE-MathJax.txt
```

## Modules

- Overview + 11-topic navigation
- Derivations (lecture and alternative notation, with individual expandable step-by-step solutions)
- Engine and nozzle schematics (original SVG drawings)
- Interactive flow graphs (k, pressure, area, nozzle effects, thrust and efficiencies)
- Worked numerical examples (including Sutton 3-1, 3-2, 3-3, 3-4)
- Typical propulsion performance range comparison
- Conceptual questions, exam traps and model assumptions
- Multiple-choice exam practice and open-response prompts
- Flashcards
- Ideal choked-nozzle performance calculator with worked equation chain
- Printable 69-equation lecture formula sheet and separate alternative sheet
- Search, progress tracking in local browser storage, responsive layout

## Offline usage

The MathJax **SVG** typesetting engine is bundled locally in `vendor/` (Apache 2.0; license enclosed), so mathematical equations render without internet as long as relative files are preserved. The optional Google Fonts request can fail offline without preventing the site from working. On your computer you can serve the folder with `python -m http.server 8000` and open `http://localhost:8000`.

## Coverage and model caveats

Main sources are 2026 lecture PDF sets **01 — Introduction**, **02 — Definitions & Fundamentals**, **03 — Nozzle Theory and Thermodynamic Relations**, plus the course syllabus. The **first midterm** takes place before the syllabus's Flight Performance block; that block is not a primary study module. Graphs and calculator mainly assume steady, constant-k, inviscid, adiabatic, shock-free, quasi-one-dimensional perfect-gas flow. If actual flow separates or shocks inside a nozzle, ideal performance predictions will fail. Different slides use slightly different station conventions; each formula includes its source page to clarify.

This is an original independent educational aid, not a copy of official course slides or an official answer key. Figures and explanations are authored for study. Always check the question's assumptions, units and section definitions.
