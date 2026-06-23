# Guangzhou Landsat 8 Land Cover Classification Lab

This repository is a personal GIS / remote sensing lab archive for a Guangzhou Landsat 8 land-cover classification experiment.

The project is mainly used to record my ENVI workflow and store related data packages. The classification results are experimental and are not intended as a production-level land-cover map.

## Project Status

Current progress:

- Landsat 8 images loaded and checked in ENVI
- Radiometric calibration completed
- FLAASH atmospheric correction completed
- Panchromatic and multispectral image fusion completed
- Two-scene mosaic completed
- Guangzhou study-area clipping completed
- ROI samples prepared
- ROI separability checked
- Maximum Likelihood classification completed
- Neural Net classification completed
- SVM classification is in progress / to be supplemented

Current land-cover classes:

- Water
- Vegetation
- Cropland
- Urban land
- Bare land

## Repository Contents

The Git repository is kept lightweight. Large raster data files are not committed directly to Git.

Recommended local files:

- `workflow.md` - workflow notes
- `guangzhou_landsat8_report.pdf` - stage report
- `ScreenShot/` - processing screenshots

Some of these local files may not be tracked in Git if they are only used as personal records.

## Data And Large Files

Large data packages are stored in **GitHub Releases**, not in the main Git repository.

Release assets may include:

- Original Landsat 8 scene packages
- Guangzhou mosaic result package
- Study-area clipping result package
- Classification result packages

Large ENVI intermediate files such as `.dat`, `.dat.enp`, rule images, and temporary outputs are excluded from Git tracking.

## Notes

This is a course / lab-style remote sensing workflow record. The current results still have limitations:

- Guangzhou has complex urban-rural mixed land cover.
- Urban land, cropland, and bare land have similar spectral characteristics in some areas.
- Landsat spatial resolution limits detailed land-cover separation.
- Some classification outputs contain mixed pixels and salt-and-pepper noise.

Future improvements may include more refined ROI samples, post-classification filtering, accuracy assessment, and comparison of different classifiers.
