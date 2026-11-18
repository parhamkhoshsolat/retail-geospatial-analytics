# Retail Geospatial Analytics: Fater S.p.A. Challenge

A four-person university team on a Fater S.p.A. challenge: we mapped stores to districts and compared districts by store potential per resident.

<p>
  <a href="https://www.parhamkhoshsolat.com/projects/retail-geospatial"><img src="https://img.shields.io/badge/Write--up-portfolio-5dc6ff?style=flat-square&labelColor=0a1422" alt="Write-up: portfolio"></a>
  <img src="https://img.shields.io/badge/2024-team_of_4-5dc6ff?style=flat-square&labelColor=0a1422" alt="2024: team of 4">
  <img src="https://img.shields.io/badge/Data-synthetic-5dc6ff?style=flat-square&labelColor=0a1422" alt="Data: synthetic">
</p>

## Overview

Course-linked industry challenge with Fater S.p.A. (the Procter & Gamble and Angelini joint venture). A GeoPandas spatial join (point-in-polygon, EPSG:4326) attaches each store to its district; store counts and Fater's per-store potential score are aggregated by district and divided by population, so districts of different sizes can be compared. Output: a choropleth of potential per resident plus Folium maps of stores and districts.

## What I did

I did the statistics and analysis part: the spatial join, the per-resident metric and the maps. The original pipeline read stores from MySQL; the public notebook keeps that code for reference only and runs on CSV and GeoJSON files.

## Results

The real results belong to Fater and are not public. This repository reruns the same method on synthetic data with the original structure, so no number or map here is a result. Limits of the synthetic run:

- The district polygons and population table are synthetic stand-ins keyed by `microcode`; no official census data is used in this repository.
- Only 8 of the 50 synthetic stores fall inside any district polygon, so 13 of the 20 districts show zero potential.
- Two synthetic polygons overlap, so one store (49) is counted in two districts. The code has no guard against double counting; real, non-overlapping district boundaries would avoid it.
- The committed `sample_data/shapes_sample.geojson` was generated before Python's `random` module was seeded, so it cannot be regenerated exactly; reruns read the committed file. The generator is now seeded for new files.
- The synthetic `Comune` values do not match the Rome-area coordinates, and male plus female population does not add up to the total. These columns are not used in the analysis.

## Run it

```bash
git clone https://github.com/parhamkhoshsolat/retail-geospatial-analytics.git
cd retail-geospatial-analytics
pip install -r requirements.txt
jupyter notebook Fater_Public.ipynb
```

## Project layout

```
├── Fater_Public.ipynb    # analysis notebook (synthetic data)
├── sample_data/          # synthetic data matching the original structure
├── visualizations/       # output maps and charts
└── requirements.txt
```

## Team & course

Statistical Learning and Data Analysis, University of Naples Federico II. Supervisor: Prof. Roberta Siciliano. Team: Parham Khosh Solat, Shayan Ekramnia, Farshad Farahtaj, Sara Aboudarda.

The original dataset was provided by Fater S.p.A. for educational use only; no proprietary data is included here, and all rights to it remain with Fater S.p.A.

## License

MIT. See [`LICENSE`](LICENSE).

---

Part of my portfolio: [parhamkhoshsolat.com](https://www.parhamkhoshsolat.com)
