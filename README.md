# Land value mapping

## Description

The Land value model was developed to obtain an information layer that contributes to AI Climate Platform, a land management instrument and decision-making tool geared to Global South secondary/tertiary cities that lack local data and whose objective is to cut the time and expense involved in climate hazard mapping, assessment, and prediction, freeing up city resources for community resilience (adaptation) building.

This is a semantic segmentation model which detects and classifies different zones according to the land value.

As inputs, it uses (I) a raster dataset and (II) georeferenced information (ground truth) regarding land values across Tegucigalpa and the main cities within San Pedro Sula valley. 

The raster dataset is composed of maps of nighttime lights, land use and land cover information, Distance to centers of interest, RGB images, Identification of existing and developing corridors, and the predictions from the Informal Settlements, Susceptible Flood areas, and Susceptible landslide areas models.

## Requirements 

The tools **GDAL** y [Orfeo Toolbox](https://www.orfeo-toolbox.org/) are used in the first stage, the pre-processing of the data. In the following stages, our packages [satproc](https://github.com/dymaxionlabs/satproc) and [unetseg](https://github.com/dymaxionlabs/satproc) are used for dataset generation and for training and prediction process.

## Notebooks

This repository has a Jupyter Notebooks set, which describes the necessary steps:

1. [Training](notebooks/1_Entrenamiento.ipynb): Satellite imagery and ground truth are processed to generate the training dataset. Then, the model is trained and evaluated.
2. [Prediction](notebooks/2_Prediccion.ipynb): Prediction over the area of interest and prediction results processing.

## :handshake: Contributions

Bugs reports y *pull requests* could be done in the [issues page](https://github.com/dymaxionlabs/adefinir) of this repository. 

## :page_facing_up: License

The code is licensed under Apache 2.0. Refer to [LICENSE.txt](LICENSE.txt).
