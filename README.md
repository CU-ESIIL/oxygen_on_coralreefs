[![DOI](https://zenodo.org/badge/733258046.svg)](https://zenodo.org/doi/10.5281/zenodo.11166823)

# Oxygen on Coral Reefs

This repository supports Wyatt Million's ESIIL project, **Leveraging dissolved oxygen to predict coral ecology**. It is both a research repository and the source for the public MkDocs website at https://cu-esiil.github.io/oxygen_on_coralreefs.

The repository and website are meant to work as one connected system:

- The repository is where data, code, notes, and synthesis products are organized and versioned.
- The website is where project context, methods, resources, and outputs are shared.
- GitHub connects them through commits, version history, and automated publishing.

## Project

This project synthesizes in situ dissolved oxygen datasets with historical coral bleaching, reef health, and species distribution datasets. The goal is to identify features of reef oxygen dynamics that can help predict species occurrences and bleaching events on tropical coral reefs.

Oxygen availability has often been left out of reef health prediction, even though ocean deoxygenation is intensifying and corals depend on oxygen for energy production. Incorporating oxygen dynamics may improve reef ecology, conservation planning, restoration decisions, and environmental stress forecasting.

## How this repository is organized

```text
.
├── README.md              # Repository overview and setup notes
├── mkdocs.yml             # Website navigation, theme, plugins, and edit links
├── docs/                  # Markdown source for the public website
├── scripts/               # Build helpers and site health checks
├── templates/             # Reusable meeting-note templates
├── data/                  # Project data and data documentation
├── docker/                # Optional runtime and environment setup
└── Research_Statement_WM.pdf
```

Use these rules of thumb when deciding where to put something:

- Top-level files and folders are for project configuration, automation, contribution guidance, licensing, environment setup, and repo-wide metadata.
- `docs/` is for public website pages and assets. Markdown files here become website pages through MkDocs.
- `mkdocs.yml` controls how the website is rendered, including navigation, theme settings, plugins, and GitHub edit links.
- Scientific working materials belong in working folders such as `data/`, notebooks, scripts, workflows, outputs, and figure directories.

## Common places to edit

- `docs/index.md` is the homepage for the public site.
- `docs/work-plan.md` tracks milestones, meetings, and outputs.
- `docs/how-this-group-works.md` holds collaboration norms, data references, code organization, and methods guidance.
- `docs/esiil-resources/` contains ESIIL training and code-of-conduct pages.
- `docs/instructions/` contains practical instructions for GitHub, persistent storage, project phases, and landmarks.
- `docs/assets/images/slots/` contains named image slots for the homepage and other shared visuals.
- `docs/assets/images/process/` contains folder-driven process galleries that render automatically on the site.

## Preview locally

```bash
pip install -r requirements.txt
python scripts/generate_image_slots.py
python scripts/site_health.py
mkdocs serve
```

## Build site

```bash
python scripts/generate_image_slots.py
python scripts/site_health.py
mkdocs build --strict --clean
```

## Swapping homepage images

The site uses semantic image slots so project contributors do not need to edit Markdown links every time an image changes.

1. Open the relevant folder in `docs/assets/images/slots/`.
2. Delete the old image file.
3. Add one new `.png`, `.jpg`, `.jpeg`, `.webp`, or `.svg` file.
4. Run `python scripts/generate_image_slots.py`.
5. Commit the image change and the regenerated slot references.

## GitHub Pages

This site is automatically built and deployed using GitHub Actions. The build generates image slot references, writes a non-blocking site health report, and then runs `mkdocs build --strict --clean`.
