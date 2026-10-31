# Explore

Interactive, self-contained learning simulations built for junior and O/L-level students — explore planets, the Earth, continents, countries, cells, atoms, forces, sentences, and a prescribed novel, all in the browser with no installs.

**Live site:** https://altovian-dev.github.io/explore/world/

## About

Explore is a small, hand-built collection of single-file HTML simulations. Each one is a self-contained page — markup, styles, and JavaScript all in one `.html` file — so any sim can be opened directly in a browser or dropped into another site with no build step and no dependencies to install. `world/index.html` is the landing page that links out to every sim below.

## What's inside

| Sim | File | Subject |
|---|---|---|
| Star Cadet Academy | `world/space-learning-games.html` | Grade 1 Games — twelve space-themed math & reading missions, no timers or failure states |
| World Map Explorer | `world/World_Map_Explorer_Prototype.html` | Geography & Space — zoomable, clickable world map (countries, rivers, mountains, languages, animal habitats, World Cup participation) |
| World Countries Trivia | `world/World_Countries_Trivia_Game.html` | Geography & Space — shuffled quiz on all 196 countries (flags, capitals, landmarks, food, language, traditions) |
| Solar System Explorer | `world/solar_system.html` | Astronomy — 3D solar system to orbit and zoom, with per-body stats and a compact/real-scale toggle |
| Plant & Animal Cell Explorer | `world/biology_cell_explorer.html` | O/L Biology — click organelles for their function, compare plant vs. animal cells, step through mitosis |
| Atomic Structure & Periodic Trends | `world/chemistry_atomic_structure_explorer.html` | O/L Chemistry — Bohr models, electron configurations, periodic table colored by category/ionization energy/electronegativity |
| Forces & Motion Lab | `world/physics_forces_motion_lab.html` | O/L Physics — adjust mass, force, and friction to explore Newton's laws; run cart collisions and check momentum conservation |
| Sentence Structure Lab | `world/english_sentence_structure_lab.html` | O/L English — sentence types and clauses, active/passive voice and direct/indirect speech flip cards |
| Bringing Tony Home — Review | `world/literature_bringing_tony_home_review.html` | O/L Literature — review of Tissa Abeysekara's prescribed novella: plot timeline, characters, themes, self-test quiz |

## Tech stack

- Vanilla HTML, CSS, and JavaScript — no framework, no bundler, no `package.json`
- Each sim is a single `.html` file: inline `<style>` and `<script>`, so it works standalone
- Google Fonts (Space Grotesk / Inter / JetBrains Mono) loaded from `fonts.googleapis.com`
- A couple of sims load a visualization library from a CDN (e.g. D3.js, Three.js) via `<script src>`
- No backend, no database, no build step — deploys as static files

## Project structure

```
.
├── README.md
└── world/
    ├── index.html                              # landing page linking to every sim
    ├── space-learning-games.html
    ├── World_Map_Explorer_Prototype.html
    ├── World_Countries_Trivia_Game.html
    ├── solar_system.html
    ├── biology_cell_explorer.html
    ├── chemistry_atomic_structure_explorer.html
    ├── physics_forces_motion_lab.html
    ├── english_sentence_structure_lab.html
    └── literature_bringing_tony_home_review.html
```

## Running locally

No install needed — just open a file in a browser:

```bash
git clone https://github.com/altovian-dev/explore.git
cd explore
open world/index.html   # or: python3 -m http.server, then visit localhost:8000/world/
```

Serving over a local HTTP server (rather than a `file://` URL) is recommended, since a couple of sims load fonts and libraries from external CDNs that some browsers restrict on `file://` pages.

## Contributing

To add a new sim:

1. Build it as a single self-contained `.html` file under `world/`, following the structure of an existing sim (inline styles/script, Google Fonts links, no external framework).
2. Add a card for it to `world/index.html`, linking to the new file.
3. Open a pull request.

## License

No license file is currently included — all rights reserved by default. Contact the repo owner before reusing content outside this project.
