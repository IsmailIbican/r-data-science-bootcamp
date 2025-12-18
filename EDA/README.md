# Exploratory Data Analysis (EDA)

This directory focuses on extracting meaningful insights from raw data through cleaning, transformation, and visualization.

## Projects & Analyses

### 1. `correlation_and_plots.qmd` (Birth Weight Analysis)
* **Dataset:** `birthwt` (from `MASS` package) - *Risk Factors Associated with Low Infant Birth Weight*.
* **Goal:** To analyze the correlation between mother's habits (smoking, hypertension) and infant birth weight.
* **Key Techniques:**
    * **Factor Recoding:** Using `plyr::mapvalues` to convert integer codes to meaningful labels.
    * **Statistical Summaries:** Using `tapply()` and `aggregate()` for grouped statistics.
    * **Visualization:** Creating faceted scatterplots and histograms to visualize distributions across groups.

### 2. `little_project_diamond_dataset.qmd`
* **Dataset:** `diamonds` (from `ggplot2` package).
* **Goal:** To investigate the relationship between diamond price and its features (Carat, Cut, Color).
* **Highlights:**
    * **Log-Log Transformation:** Applied `log()` transformation to Price and Carat variables to linearize the exponential relationship for better modeling.
    * **Outlier Detection:** Implemented IQR (Interquartile Range) method to detect and count outliers in numeric columns.
    * **Detailed Plotting:** Boxplots for price distribution by clarity and bar charts for color frequency.

## Libraries Used
```r
library(ggplot2) # Advanced visualization
library(dplyr)   # Data manipulation
library(MASS)    # Access to birthwt dataset
library(psych)   # For describe() function
library(plyr)    # For mapvalues()
library(knitr)   # For pretty tables (kable)