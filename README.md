# Cepheid-Wesenheit-Analysis

## Overview

This repository contains code and analysis for estimating the period-luminosity relationship of OGLE-III classical Cepheids using the Wesenheit index. Cepheids are valuable astronomical objects for distance measurement, and the Wesenheit index provides an advantage by being insensitive to extinction.

## Data

The dataset used in this analysis includes the Wesenheit index of fundamental-mode ('F') and first overtone ('1') classical Cepheids from OGLE-III. The data columns include:
- 'name': Identifier of the star
- 'RA0': Celestial coordinates in decimal hours
- 'Decl0': Celestial coordinates in decimal degrees
- 'Mode': Mode of the Cepheid ('F' or '1')
- 'Cloud': Magellanic Cloud to which the star belongs ('LMC' or 'SMC')
- 'logP1': Base-10 logarithm of the period in days
- 'VI': Color V-I
- 'W': Wesenheit index

## Analysis Steps

### 1. Data Exploration and Visualization
- Scatter plots of Wesenheit index ('W') against the base-10 logarithm of the period ('logP1') for different subsets:
  - LMC Cloud, Mode F
  - LMC Cloud, Mode 1
  - SMC Cloud, Mode F
  - SMC Cloud, Mode 1

### 2. Regression Analysis
- Linear regression is applied to estimate straight lines for each subset.
- Regression lines and data points are plotted for visual representation.

### 3. Residual Analysis
- Residuals are computed for each sample by subtracting the predicted values from the observed values.
- Histograms are generated to assess the normality of residuals using the Shapiro-Wilk test.

### 4. Spatial Distribution of Residuals
- Scatter plots of residuals against celestial coordinates (RA and Dec) are created, color-coded by the sign of residuals.

## Results

- Residuals do not appear to follow a normal distribution based on Shapiro-Wilk test results.
- Spatial distribution of residuals reveals patterns that may be related to celestial coordinates.

For a detailed walkthrough and demonstration, refer to the provided code and analysis in the Jupyter notebook.

## Additional Resources

- [YouTube Video](https://www.youtube.com/watch?v=iyisAjHdhas) on classical Cepheids and their significance in measuring distances.

Feel free to explore and contribute to this repository for further insights into Cepheid variable stars and their period-luminosity relationship.
