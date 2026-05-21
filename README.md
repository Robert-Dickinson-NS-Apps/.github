# Robert-Dickinson-NS-Apps

Single-file browser apps for water engineering, hydraulic modeling, and SWMM education. Every app is one HTML or React file, no build step, deployed straight to Netlify and embedded in [SWMM5.org](https://www.swmm5.org) and Google Sites.

Built by Robert (Bob) Dickinson, Autodesk Water Technologist and co-developer of EPA SWMM versions 3, 4, 5, and 5+.

---

## What lives here

Interactive first-principles deconstructions of hydraulic concepts. Each app replaces static documentation with something you can drive: move a slider, see the equation respond, watch the chart redraw in real time. The bet is that five minutes with a parameter explorer teaches more than fifty pages of manual.

The apps span four families:

**First-principles deconstructors** take one concept and expose every parameter. St. Venant continuity and momentum term by term, Manning's *n* across SWMM5 / ICM / HEC-RAS, RTK unit hydrograph convolution, Horton and Green-Ampt infiltration, force main Hazen-Williams vs Darcy-Weisbach.

**Rosetta Stones** map concepts across engines. EPANET to SWMM5 (120+ concept pairs), RDII translation, InfoSewer to ICM peaking factors.

**Engine explorers** rebuild solver behavior in the browser. SWMM5 Runoff Explorer with a Cash-Karp RK5 solver, CFL stability analyzer, ICM InfoWorks Preissmann reconstruction, SWMM4 Bulirsch-Stoer.

**Readers and converters** parse real model files without the desktop software. InfoSWMM/InfoSewer DBF readers (no ArcMap needed), XPSWMM .xp file reader, SWMM5-to-InfoDrainage .iddx converter, .inp generators.

---

## How the apps are built

| Principle | What it means |
|-----------|---------------|
| Single-file | One `.html` or `.jsx`, CDN dependencies only, no bundler |
| Physics-first | Every slider maps to a real equation; every chart shows real math |
| Immediate feedback | Change a parameter, see the result instantly |
| Export-ready | CSV export, .inp generation, copy-to-clipboard |
| Mobile-friendly | Works in the field on a phone screen |
| Onboarded | Opens with a "How to Use" modal and a guided tour, always |

Stack: React or vanilla HTML, Tailwind, Recharts / D3 for plotting, mathjs where needed. Deployed via `netlify deploy --prod`.

---

## Getting a local copy running

These are static files. No install, no server required for most of them.

```bash
git clone https://github.com/Robert-Dickinson-NS-Apps/<repo>.git
cd <repo>
# open the .html directly, or serve it:
python3 -m http.server 8000
```

For React single-file apps, open `index.html` in a browser or drop the repo into Netlify.

---

## Related work

- **[SWMM5.org](https://www.swmm5.org)** — 1,700+ posts, where most of these apps are embedded
- **[SWMM2000.com](https://www.swmm2000.com)** — the SWMM modeling forum
- **GitHub: [Dickinsonre](https://github.com/Dickinsonre)** — the main personal account, 44+ repositories
- **YouTube: [@SWMM5](https://www.youtube.com/@SWMM5)** — walkthroughs and demos

---

## About

Fifty-plus years of continuous SWMM development, from punch cards at the University of Florida in 1974 to single-file browser apps today. Co-author of the SWMM4 User's Manual (Huber, Dickinson, Barnwell, Branch, 1988), author of the original `rdii.c` RTK unit hydrograph in the EPA SWMM5 CRADA, and designer of the .xp and .xpx file formats at XP Software.

Chair of the SWMM5+ Technical Advisory Committee at CIMM.org. Member of the EWRI Stormwater Modeling Committee.

**Contact:** robert.dickinson@gmail.com

---

*Apps are educational tools. Verify all results against the production engine before using them for design.*
