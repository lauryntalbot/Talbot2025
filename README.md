# Glider Spectral Analysis and Transfer Functions

This repository contains the code used to preprocess glider observations, perform spectral analyses, and construct transfer functions for the analyses presented in:

**Talbot, L. C., Klymak, J. M., Ross, T., & Han, G.** (2025).  
*Contrasting stirring regimes in the Northeast Pacific*.  
*Journal of Geophysical Research: Oceans*, in review.

The repository is organized to reflect the full analysis workflow, from raw glider data preprocessing through to the figures shown in the manuscript.


---

## 1. Glider Data Pre-processing  
**`CPROOF_delayed_grid_sections_calculation.ipynb`**

This notebook documents the preprocessing applied to the raw glider observations prior to analysis, including:

- Vertical gridding and interpolation of delayed-mode glider data  
- Manual identification and removal of spurious spikes and sensor artefacts  
- Quality control decisions applied before any spectral analysis  

This notebook provides transparency and reproducibility for how the analyzed glider sections were constructed from the original observations.

---

## 2. Main Analysis and Figures  
**`Paper_code.ipynb`**

This notebook contains the core analysis and plotting routines used to generate the figures presented in the manuscript, including:

- Processed glider sections and anomaly calculations  
- Statistical summaries and diagnostics  
- Final figures used in the paper  

This is the primary notebook to run in order to reproduce the manuscript figures from the preprocessed data.

---

## 3. Spectral Analysis  
**`T_spectra-2025.ipynb`**

This notebook contains the spectral analysis methods applied to the glider data, including:

- Along-track spectral calculations  
- Whitening and normalization procedures  
- Comparisons across spatial regimes and missions  

Methodological details, parameter choices, and interpretation are documented within the notebook.

---

## 4. Transfer Functions  
**`transfer_functions.ipynb`**

This notebook documents the derivation and application of transfer functions used in the analysis, including:

- Construction of transfer functions relevant to the observing system  
- Application to spectral quantities  
- Sensitivity tests and validation  

This notebook complements the spectral analysis and provides the theoretical and computational basis for the transfer-function corrections discussed in the manuscript.

---

## Data Availability

The data used in this study are publicly available from the following sources:

- **Canadian-Pacific Robotic Ocean Observing Facility (C-PROOF)**  
  Glider observations were collected and made available by the Canadian-Pacific Robotic Ocean Observing Facility (C-PROOF) and are accessible at  
  https://cproof.uvic.ca  
  DOI: **10.82534/44DS-K310**

- **Copernicus Marine Service**  
  This study was conducted using E.U. Copernicus Marine Service Information:  
  https://doi.org/10.48670/moi-00021  
  https://doi.org/10.48670/moi-00149

- **Argo Program**  
  Argo float data were collected and made freely available by the International Argo Program and the national programs that contribute to it:  
  http://www.argo.ucsd.edu  
  http://argo.jcommops.org  

  The Argo Program is part of the Global Ocean Observing System.

Due to data volume and preprocessing steps, the full processed datasets are not included in this repository. The notebooks provided here document the analysis workflow and parameter choices in sufficient detail to reproduce the results given access to the underlying data.

---

## Code Availability

All code used for data preprocessing, spectral analysis, and transfer-function calculations is provided in this repository. The notebooks are organized to follow the analysis pipeline described in the manuscript.

---

## Requirements

The analysis was developed in Python and relies on standard scientific libraries, including:

- `numpy`
- `scipy`
- `xarray`
- `matplotlib`
- `gsw` and/or `seawater`

Exact environment details can be added if needed.

---

## Notes

This repository reflects the analysis state used in the submitted manuscript. Minor updates may occur prior to final publication.
