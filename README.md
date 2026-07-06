# Strength

A static web application for interactive stress–strain analysis in compression and tension.

## Overview

`index.html` is a single-page app that lets users paste or upload strain-stress data, analyze the curve, and visualize key material behavior regions.

The app automatically detects:
- Seating region
- Elastic region and elastic modulus fit
- Hardening region
- Softening region
- Densification region
- Ultimate tensile/compressive strength (UTS/UCS)

It also computes:
- Yield strain and yield stress (approximate)
- R² fit quality for the elastic region
- Energy absorbed under the curve up to the selected region

## Features

- Paste tab-delimited, comma-separated, semicolon-separated, or space-separated data
- Upload CSV / TSV files
- Choose between Compression and Tensile analysis modes
- Interactive Plotly chart with regions, elastic fit, and strength markers
- Region editor with draggable start/end sliders
- Export results as CSV
- Download the graph as PNG
- Local state persistence in browser storage

## Input format

The app expects two columns:
1. Strain
2. Stress in MPa

Header rows are optional. The first two columns are parsed and cleaned automatically.

## How to use

1. Open `index.html` in a browser.
2. Select `Compression` or `Tensile` mode.
3. Paste strain-stress data into the editor or upload a CSV/TSV file.
4. Click `Analyze Data`.
5. Review the preview table and chart.
6. Adjust the selected region and visibility toggles as needed.
7. Export results using the CSV buttons or download the graph as PNG.

## Deployment

This repository is a static site. No build step is required.

- Open `index.html` directly in a browser.
- Or host from GitHub Pages using the `main` branch root.

## Dependencies

- Plotly 2.35.2 loaded from CDN: `https://cdn.plot.ly/plotly-2.35.2.min.js`

## Repository contents

- `index.html` — the full web app
- `README.md` — project overview and usage
- `LICENSE` — license for the project

## Notes

The app is designed for material test data analysis and is optimized for research-style stress-strain interpretation with a publication-ready interactive graph.
