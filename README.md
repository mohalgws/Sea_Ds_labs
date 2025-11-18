# COVID-19 Data Visualization (R Project)

## Overview

This project analyzes and visualizes country-wise COVID-19 data. Using R, it produces a series of informative plots to understand the global distribution and major trends related to confirmed cases, deaths, recoveries, and actives cases. All code and visualizations are designed for clarity and easy reproducibility.

## Dataset

- **Filename:** `country_wise_latest.csv`
- **Source:** Provided as part of course assignment.
- **Description:** This dataset contains COVID-19 statistics per country, including confirmed cases, deaths, recoveries, active cases, and new cases.

## Visualizations Created

1. **Pie Chart:**  
   - Displays the top 6 countries by confirmed cases, showing count and percent contribution.
2. **Stacked Bar Chart:**  
   - Compares confirmed, deaths, recovered, and active cases for the top 6 countries, using color-coded stacks.
3. **Scatter Plot:**  
   - Shows the relationship between confirmed cases and deaths for all countries.
4. **Line Chart:**  
   - Plots confirmed cases for the top 6 countries to compare their trends.

All plots are saved in `covid_visualizations.pdf`.

## How to Reproduce

1. Place `country_wise_latest.csv` in your working directory.
2. Open the R script and run all code blocks, making sure packages `readr` (and `plotrix` if using 3D pie) are installed.
3. The plots will be saved to a single PDF file as specified by the code.

## Key Insights

- The pandemic is heavily concentrated in a few countries, which dominate global statistics for cases and deaths.
- There are substantial differences in recovery and active case rates among nations with high case counts.
- Scatter and line plots reveal that higher confirmed cases often mean higher deaths, but with country-specific exceptions.
- Bar and pie charts visually highlight the disproportionate burden shouldered by the leading nations in the pandemic.

## Files Included

- `country_wise_latest.csv` — Main data source.
- `covid_visualizations.pdf` — All generated visualizations.
- `README.md` — Project overview and instructions.

## Author/Submitter

- *Mohal Manohar Gawas*
