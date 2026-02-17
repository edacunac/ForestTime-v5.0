# ForestTime v5.0

**A mobile platform for IUFRO-standardized time studies in mechanized forest operations**

[![DOI](https://img.shields.io/badge/DOI-pending-blue)]()
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Platform](https://img.shields.io/badge/Platform-Android%207.0%2B-green.svg)]()

## Overview

ForestTime is an Android mobile application designed for conducting IUFRO-standardized time studies of mechanized forest operations. The application implements the complete time classification hierarchy defined by Björheden et al. (1995), with machine-specific sub-element decomposition for seven predefined equipment profiles.

## Features

- **Machine-specific profiles**: Harvester, Forwarder, Skidder, Processor, Feller-Buncher, Chainsaw, Yarder, plus Custom
- **IUFRO-standardized**: Full compliance with international work study nomenclature
- **Real-time sample size estimation**: Live CV and recommended n updated after each cycle
- **Automated R script generation**: Dynamically generated analysis script adapted to the machine type studied
- **Millisecond precision**: Event-based recording using monotonic system clock
- **Bilingual**: English / Spanish
- **GPS geolocation**: Automatic coordinate capture at study initiation
- **Crash recovery**: Automatic save after every event
- **Complete export**: ZIP package with events CSV, production CSV, metadata JSON, and R script

## Installation

Download the APK from the [`apk/`](apk/) folder and install on any Android 7.0+ device.

## Machine Profiles

| Machine | MW Sub-elements | Production Variables |
|---------|----------------|---------------------|
| Harvester | Move to tree, Felling, Delimbing, Bucking, Stacking | DBH, Species, Tree volume, No. of logs |
| Forwarder | Travel empty, Loading, Travel loaded, Unloading | Distance, Load volume, No. of logs |
| Skidder | Travel empty, Choking/Grapple, Skid loaded, Unhook, Decking | Skid distance, No. of pieces, Volume, Slope |
| Processor | Feed/Grab, Delimbing, Bucking, Stacking | DBH, Species, Log volume |
| Feller-Buncher | Move to tree, Felling, Accumulate, Dump bunch | N trees, DBH, Species, Slope |
| Chainsaw | Felling, Limbing, Bucking | DBH, Species, Height, Slope |
| Yarder | Outhaul, Lateral in, Hook, Inhaul, Unhook/Deck | Yarding distance, No. of logs, Volume, Slope |

## Export Format

The application exports a ZIP archive containing:

1. `events_data.csv` — Individual event records with IUFRO codes
2. `production_data.csv` — Per-cycle production variables
3. `metadata.json` — Study metadata, GPS, and computed indicators (MA, MU, CV, recommended n)
4. `analysis_ForestTime.R` — Dynamically generated R analysis script

## Example Dataset

The `supplementary/` folder contains an example dataset from a Tigercat LS855C shovel logger (Feller-Buncher profile), comprising 7,353 events and 6,426 cycles collected over 8 working days.

## Citation

If you use ForestTime in your research, please cite:

> Acuña E, Cancino J, Acuña C. ForestTime: A mobile platform for IUFRO-standardized time studies in mechanized forest operations. *International Journal of Forest Engineering*. (submitted).

## Authors

- **Eduardo Acuña** — Departamento de Manejo de Bosques y Medio Ambiente, Universidad de Concepción, Chile
- **Jorge Cancino** — Departamento de Manejo de Bosques y Medio Ambiente, Universidad de Concepción, Chile
- **Cristóbal Acuña** — Facultad de Ingeniería Agrícola, Universidad de Concepción, Chile

## Laboratory

LASeR-EF — Laboratorio de Algoritmos y Sensoramiento Remoto en Ecosistemas Forestales  
Facultad de Ciencias Forestales, Universidad de Concepción, Chile

## License

This project is licensed under the GNU General Public License v3.0 — see the [LICENSE](LICENSE) file for details.
