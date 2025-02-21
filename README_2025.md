# Land Value Mapping

## Table of Contents
- [Overview](#overview)
- [Installation & Setup](#installation--setup)
  - [Prerequisites](#prerequisites)
  - [Installing Dependencies](#installing-dependencies)
- [Development & Usage](#development--usage)
  - [Notebooks](#notebooks)
  - [Running the Model](#running-the-model)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

The **Land Value Model** is a semantic segmentation model designed to assess and classify different zones based on land value. It contributes to the **AI Climate Platform**, a decision-making tool targeting secondary and tertiary cities in the **Global South** that lack local data. The model aims to **reduce the time and cost** involved in climate hazard mapping, freeing up city resources for **community resilience (adaptation) efforts**.

The model uses:
- **Raster datasets**, including nighttime lights, land use/land cover, distance to key locations, RGB imagery, and identified corridors.
- **Georeferenced land value information**, covering **Tegucigalpa** and **San Pedro Sula Valley**.
- **Predictions from related models**, including **Informal Settlements, Susceptible Flood Areas, and Susceptible Landslide Areas**.

---

## Installation & Setup

### Prerequisites
Ensure you have the following installed:
- [Docker](https://docs.docker.com/get-docker/) *(for containerized execution)*
- [GDAL](https://gdal.org/) *(for geospatial data processing)*
- [Orfeo Toolbox](https://www.orfeo-toolbox.org/) *(for advanced raster processing)*
- Python 3.8+
- [satproc](https://github.com/dymaxionlabs/satproc) *(for dataset processing)*
- [unetseg](https://github.com/dymaxionlabs/unetseg) *(for model training and segmentation)*

### Installing Dependencies
To install required dependencies:
```sh
pip install -r requirements.txt
```
For geospatial libraries (GDAL & Orfeo Toolbox), follow their respective installation guides.

---

## Development & Usage

### Notebooks
This repository contains **Jupyter Notebooks** detailing essential steps:

1. **[Training](notebooks/1_Entrenamiento.ipynb)**: Processes satellite imagery and ground truth data to generate the training dataset. The model is then trained and evaluated.
2. **[Prediction](notebooks/2_Prediccion.ipynb)**: Runs predictions over the area of interest and processes the results.

To run the notebooks:
```sh
jupyter notebook
```

### Running the Model
To train the model manually:
```sh
python train.py --config config.yaml
```
To make predictions:
```sh
python predict.py --input input_data.tif --output predictions.tif
```

---

## Contributing
Bug reports and *pull requests* are welcome on the [issues page](https://github.com/dymaxionlabs/adefinir).

To contribute:
1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature-branch`)
3. **Commit your changes** (`git commit -m "Description of changes"`)
4. **Push the branch** (`git push origin feature-branch`)
5. **Submit a pull request**

---

## License
The code is licensed under **Apache 2.0**. See [LICENSE.txt](LICENSE.txt) for details.
