# TSAR Project Assignment Part 3 - Group 3
## Time Series Forecasting of US Employment (Mining & Logging)
This folder contains the complete time series forecasting analysis for the **Time Series Analysis with R (TSAR)** course (Part 3 Project Assignment). 
### Group Members
*   **Arpad Broglie** (arpad.broglie@students.fhnw.ch)
*   **Teodor Glisic** (teodor.glisic@students.fhnw.ch)
---
### Project Overview
The analysis models and forecasts monthly US employment numbers in the **Mining and Logging** sector (Series ID: `CEU1000000001`) from January 1939 to September 2019. The project compares two benchmark forecasting methods trained on the first 80% of the historical timeline and evaluated on the remaining 20% test window.
#### Models Estimated:
1.  **Model 1 (Mean Method):** A baseline model setting all future forecasts to the historical training average ($\approx 808.6$ thousand employees).
2.  **Model 2 (Seasonal Naïve with Drift):** A trended seasonal benchmark model incorporating the historical monthly decline rate ($b = -4.44$ thousand/month) alongside annual seasonal cycles.
---
### Directory Contents
*   **`P3-3.qmd`**: The primary Quarto markdown source file. It handles library loads, dataset loading, model training, residual diagnostics (ACF, Ljung-Box test), test-set accuracy evaluations, and final model comparisons.
*   **`P3-3.pdf`**: The rendered PDF report ready for submission.
*   **`P3-3.html`**: The interactive HTML version of the report.
*   **`us_employment_filtered.rds`**: The pre-filtered `tsibble` dataset containing the target job sector.
*   **`us_employment.rds`**: The full U.S. employment dataset.
*   **`Series_IDs.pdf` & `TSAR_Project_Assignment_Part3.pdf`**: Assignment guidelines and sector references.
---
### Reproduction Instructions
#### Prerequisites
Ensure you have **R (>= 4.0)** and **Quarto** installed. The report relies on the following R packages, which are automatically installed if missing:
```R
install.packages(c("dplyr", "tidyr", "ggplot2", "fpp3"))
```
#### Rendering the Report
To regenerate the HTML and PDF output files, open RStudio and click the **Render** button in the source editor of `P3-3.qmd`, or execute the following command in your terminal/R console:
```bash
quarto render P3-3.qmd
```
