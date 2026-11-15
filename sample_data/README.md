# Sample Data Directory

This directory contains synthetic sample data files that mimic the structure of the original dataset provided by Fater S.p.A.

The files are committed. If they are missing, the Jupyter notebook (`Fater_Public.ipynb`) generates them:

1. `stores_sample.csv` - Synthetic data mimicking store information
2. `sociodemographic_sample.csv` - Synthetic demographic information by district
3. `shapes_sample.geojson` - Synthetic geographic boundaries for districts

These files are generated programmatically with random data that maintains the same structure as the original proprietary dataset but does not contain any actual data from the original challenge.

## Note on Data Usage

This synthetic data is provided for demonstration purposes only and to show the analysis methodology. It is not derived from or representative of the original proprietary data provided by Fater S.p.A. for the challenge. The synthetic district polygons overlap in places and most stores fall outside every polygon, so the outputs show the method only.
