# aerial-building-segmentation

What: segment building footprints in 0.3 m aerial RGB tiles with a U-Net, measure IoU on a
city the model never saw, and export buildings as GeoJSON polygons.
Done when: IoU on held-out city (Vienna), tile -> GeoJSON, Colab notebook.

Data: Inria Aerial Image Labeling (5 cities, research-use licence, ~26 GB).
Train on Austin, Chicago, Kitsap, West Tyrol; hold out Vienna (Inria test labels aren't public).
Data script supports a subset (N tiles per city). Tests use synthetic tiles; CI never downloads data.
Never Fraunhofer or BTU data or code. No data or weights in git.

Package: src/abseg/   Tests: tests/   Configs: configs/
Commands:
- install: pip install -e ".[dev]"
- test:    pytest
- lint:    ruff check .

Milestones (tick them in the 365 Build Log):
1. Data script: download + tile to 512 px patches, split by city, subset option
2. Baseline U-Net (ResNet34 encoder) on Colab/Kaggle, val IoU
3. IoU on Vienna (held-out city) in results table
4. Inference CLI: full tile -> sliding-window mask -> polygons -> GeoJSON
5. Notebook + README (demo image, results, limitations). Optional demo on an open
   German orthophoto (check its licence first; resample 0.2 m to 0.3 m)

Current status: skeleton created. Next: milestone 1.
