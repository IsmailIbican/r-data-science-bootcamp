# Introduction to R

This directory lays the foundation of my R programming skills. It covers everything from basic atomic vectors to advanced data wrangling using the `tidyverse` ecosystem.

## Content Breakdown

### 1. `introduction_to_R.qmd` (Practice R)
* **Topics:** Data Cleaning, Piping (`|>`), and Aggregation.
* **Key Techniques:**
    * **Data Wrangling:** Using `dplyr` verbs like `select`, `filter`, `mutate`, `arrange`, and `group_by`.
    * **Custom Functions:** Writing functions for reproducible logic.
    * **Visualizing Distributions:** Basic histograms and boxplots using `ggplot2`.
* **Dataset Used:** * `student_mini.csv` (Custom practice dataset for GPA analysis).
    * `iris` (Built-in R dataset).

### 2. `basics_of_R.qmd`
* **Topics:** Variables, Atomic Vectors, Arithmetic Operations.
* **Key Functions:** `c()`, `seq()`, `rep()`, `typeof()`.
* **Description:** A cheat sheet for R's syntax rules and basic data types (Numeric, Character, Logical).

### 3. `lists_and_statements.qmd`
* **Topics:** Control Structures and Complex Data Types.
* **Key Concepts:**
    * **Lists:** Handling mixed data types in a single object.
    * **Control Flow:** Implementation of `if-else` logic and loops (`for`, `while`).

## Libraries Used
```r
library(readr)   # For reading CSV files
library(dplyr)   # For data manipulation
library(ggplot2) # For basic plotting
library(broom)   # For tidying model outputs