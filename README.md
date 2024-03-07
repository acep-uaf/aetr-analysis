# Data Visualization and Analysis

## Introduction
Contains code, figures, appendix tables, and source data for the Capacity, Generation, and Consumption sections of the Alaska Electricity Trends Report (forthcoming, 2024). This repository is complimentary to [acep-uaf/es_db](https://github.com/acep-uaf/es_db).

## File notes
This repository calls on three main Jupyter Notebooks to create all figures and statistics used in the Capacity, Generation, and Consumption sections of the report.

|Element|Description|
|:-|:-|
|`./figures/` | This folder contains PNG and EPS/PDF files for all figures. PNG files are mostly 6.5in $\times$ 4in @ 600dpi. The EPS/PDF files are vector graphics and should be used for publication. Github automatically converts EPS to PDF on upload. Additionally, `energy-regions-flow-chart.drawio` and it's respective PNG are for the diagram mapping AEA to ACEP energy regions. It can be uploaded to [draw.io](draw.io) and modified.|
| `./tables/`| This folder contains CSV outputs for some of the figures in the report. These are meant to be used in the creation of appendix tables. |
| `capacity.ipynb`| Builds the figures and statistics for the Capacity section of the report. |
|`net-generation.ipynb` | Builds the figures and statistics for the Generation section of the report. |
|`consumption.ipynb` | Builds the figures and statistics for the Consumption section of the report. |


## Setup

A virtual environment for this repository may be required. I have included a list of packages I used in my virtual environment in `requirements.txt`. This can be installed *inside* your virtual envrionment with `$ pip install -r requirements.txt`.

## Repository standards

Please adhear to the following standards for this repository:

| Topic | Repository standard |
|:-|:-|
|Filenames | Lowercase with hyphens: `filename-test.txt`|
| Dates | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) Short or Long |

