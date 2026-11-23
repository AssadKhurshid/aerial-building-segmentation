# aerial-building-segmentation

Find building footprints in aerial photos and export them as map polygons (GeoJSON). The model is tested on a city it never saw during training, which is the real question for mapping work: does it generalise?

> Work in progress. Results land with milestone 3.

## Results
| Model | Train cities | Test city | IoU |
| --- | --- | --- | --- |
| _tbd_ | Austin, Chicago, Kitsap, West Tyrol | Vienna (held out) | |

## Run it
```bash
pip install -e ".[dev]"
pytest
```

## How it works
_tbd_

## Limitations
_tbd_

## Data
[Inria Aerial Image Labeling Dataset](https://project.inria.fr/aerialimagelabeling/) (Maggiori et al., 2017), research-use licence. Not stored in this repo.
