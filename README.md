# A Pipeline for Exoplanet Detection and Characterization Using TESS Space Photometry

[![Open In Colab]((https://colab.research.google.com/drive/1i4WlNTO_PiYi3ADGn-oKb-Ce_b8GJYjH?authuser=2))]

## Abstract
This repository features an automated Python pipeline developed to analyze public space photometry data from NASA's Transiting Exoplanet Survey Satellite (TESS). By implementing the Box Least Squares (BLS) algorithm coupled with an adaptive digital filtering framework, the pipeline isolates periodic transit signals. A rigorous manual vetting protocol was established to mitigate instrumental artifacts and geometric false positives. 

The project successfully isolated **15 high-priority exoplanet candidates** and characterized **3 exotic stellar systems**, including an EW-type contact binary and an asymmetric transit profiling an exocometary dust tail.

---

## Consolidated Catalogue of Results
Below are the derived physical parameters extracted from the automated survey, cross-referenced with stellar host properties from the TESS Input Catalogue (TIC):

| TIC ID | Period $P$ (days) | Radius $R_p$ | Semimajor Axis $a$ (AU) | Flux $S$ ($S_{\oplus}$) | Stellar $T_{eff}$ (K) | Physical Classification |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| **TIC 100757807** | 19.3786 | $7.11 \ R_{\oplus}$ | 0.1435 | 63.12 | 5420 | Warm Neptunian body |
| **TIC 110795273** | 9.4634 | $0.78 \ R_J$ | 0.0861 | 107.98 | 5810 | Dense Hot Jupiter |
| **TIC 123133954** | 18.9948 | $5.08 \ R_{\oplus}$ | 0.1335 | 39.27 | 4860 | High-value Temperate Sub-Neptune |
| **TIC 128558444** | 1.5511 | $4.02 \ R_{\oplus}$ | 0.0260 | 1326.45 | 5200 | Ultra-Short Period (USP) Candidate |
| **TIC 144628120** | 3.2384 | $1.39 \ R_J$ | 0.0449 | 893.62 | 6300 | Inflated Hot Jupiter |
| **TIC 149833117** | 4.0517 | Variable | 0.0542 | — | 5920 | Asymmetric Transit (**Exocomet Tail**) |
| **TIC 164260243** | 1.8475 | Stellar | 0.0315 | — | 6110 | **EW-Type Contact Binary** |

*(Note: The complete list of the 18 analyzed objects can be consulted in the main PDF document).*

---

## Key Features of the Python Pipeline
* **Data Ingestion:** Automated downloading of TESS light curves using the `lightkurve` API.
* **Signal Processing:** Adaptive flattening and outlier removal to eliminate stellar variability and red noise.
* **Periodicity Search:** Implementation of the Box Least Squares (BLS) periodogram to extract period ($P$), transit depth ($\delta$), and duration ($\Delta t$).
* **Diagnostic Visualization:** Automated generation of phase-folded light curves and SDE power spectra grids.

## How to Run
You don't need to install anything locally. Just click on the **Open in Colab** badge at the top of this README to launch the interactive pipeline tutorial in your browser.

## Acknowledgments
Data collected by the TESS mission were obtained from the Barbara A. Mikulski Archive for Space Telescopes (MAST) at STScI.
