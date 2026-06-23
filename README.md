# Guangzhou Landsat 8 Land Cover Classification Lab

This repository is a lightweight archive for a GIS / remote sensing lab project using Landsat 8 imagery of Guangzhou.

The work was mainly completed in ENVI. It records the basic processing workflow from image preprocessing to supervised classification. The result is an experimental course-style output, not a production-level land-cover map.

## Workflow

Completed / recorded steps:

- Opened and checked two Landsat 8 scenes in ENVI
- Radiometric calibration
- FLAASH atmospheric correction
- Panchromatic and multispectral image fusion
- Seamless mosaic of the two scenes
- Guangzhou study-area clipping with boundary data
- ROI sample selection
- ROI separability check
- Supervised classification experiments

Classification methods used / tested:

- Maximum Likelihood
- Neural Net
- Support Vector Machine

Final land-cover classes used in this lab:

- Water
- Vegetation
- Cropland
- Urban land
- Bare land

## Repository Contents

The main Git repository is kept small. Large raster data and compressed source images are not committed directly to Git.

Tracked files in the repository:

- `README.md` - project overview and data notes
- `.gitignore` - excludes large ENVI raster files and temporary outputs

Local working files may include:

- `workflow.md` - process notes
- `guangzhou_landsat8_report.pdf` - stage report
- `ScreenShot/` - ENVI operation screenshots
- `FinalData/` - local ENVI outputs and intermediate files

These local working files are mainly for personal record keeping and may not all be uploaded to the Git repository.

## Data In Releases

Large data files are stored in GitHub Releases instead of the main branch.

| Release | File | Description |
| --- | --- | --- |
| [Guangzhou_Shp](https://github.com/Wukeeeeee/Guangzhou-landsat8-lab/releases/tag/Guangzhou_Shp) | `CantonShp.zip` | Guangzhou boundary shapefile used for study-area clipping |
| [Landsats8_Data_122043](https://github.com/Wukeeeeee/Guangzhou-landsat8-lab/releases/tag/Landsats8_Data_122043) | `LC81220432021019LGN00.zip` | Original Landsat 8 scene package, path/row 122/043 |
| [Landsats8_Data_122044](https://github.com/Wukeeeeee/Guangzhou-landsat8-lab/releases/tag/Landsats8_Data_122044) | `LC81220442021019LGN00.zip` | Original Landsat 8 scene package, path/row 122/044 |

Processed ENVI files such as `.dat`, `.hdr`, `.enp`, rule images, and temporary outputs are intentionally excluded from Git because they are too large for normal repository tracking.

## Notes

This project is best understood as a personal learning archive for a GIS coursework / lab workflow. The classification result still has visible limitations:

- Guangzhou contains complex urban-rural mixed land cover.
- Urban land, cropland, and bare land can be spectrally similar in Landsat imagery.
- Landsat spatial resolution makes detailed urban green space and mixed pixels hard to separate.
- Some classification results may contain salt-and-pepper noise and need post-processing or accuracy assessment.

Future improvements could include refined ROI samples, post-classification filtering, confusion matrix accuracy assessment, and comparison between classifiers.
