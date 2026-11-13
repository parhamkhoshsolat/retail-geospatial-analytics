# Retail Geospatial Analytics: Fater S.p.A. Challenge

A four-person university team on a Fater S.p.A. challenge: we mapped stores to census districts and compared districts by store potential per resident.

<p>
  <a href="https://www.parhamkhoshsolat.com/projects/retail-geospatial"><img src="https://img.shields.io/badge/Write--up-portfolio-5dc6ff?style=flat-square&labelColor=0a1422" alt="Write-up: portfolio"></a>
  <img src="https://img.shields.io/badge/2024-team_of_4-5dc6ff?style=flat-square&labelColor=0a1422" alt="2024: team of 4">
  <img src="https://img.shields.io/badge/Data-synthetic-5dc6ff?style=flat-square&labelColor=0a1422" alt="Data: synthetic">
</p>

## Overview

Course-linked industry challenge with Fater S.p.A. (the Procter & Gamble and Angelini joint venture). A GeoPandas spatial join (point-in-polygon, EPSG:4326) attaches each store to its census district; store counts and Fater's per-store potential score are aggregated by district and divided by population, so districts of different sizes can be compared. Output: a choropleth of potential per resident plus Folium maps of stores and districts.

## What I did

I did the statistics and analysis part: the spatial join, the per-resident metric and the maps. Store data came from a MySQL database.

## Results

The real results belong to Fater and are not public. This repository reruns the same method on synthetic data with the original structure.

## Run it

```bash
git clone https://github.com/parhamkhoshsolat/retail-geospatial-analytics.git
cd retail-geospatial-analytics
jupyter notebook Fater_Public.ipynb
```

## Project layout

```
├── Fater_Public.ipynb    # analysis notebook (synthetic data)
├── sample_data/          # synthetic data matching the original structure
└── visualizations/       # output maps and charts
```

## Team & course

Statistical Learning and Data Analysis, University of Naples Federico II. Supervisor: Prof. Roberta Siciliano. Team: Parham Khosh Solat, Shayan Ekramnia, Farshad Farahtaj, Sara Aboudarda.

The original dataset was provided by Fater S.p.A. for educational use only; no proprietary data is included here, and all rights to it remain with Fater S.p.A.

## License

MIT. See [`LICENSE`](LICENSE).

---

Part of my portfolio: [parhamkhoshsolat.com](https://www.parhamkhoshsolat.com)
