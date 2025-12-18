# Statistical Models & Machine Learning

This module contains advanced predictive modeling and statistical inference projects. It demonstrates the application of Supervised Learning algorithms and Hypothesis Testing using R.

## Datasets Used

| Dataset | Source / Description | Used In |
| :--- | :--- | :--- |
| **Meta Ads Data** | [Marketing Data Science Blog](https://blog.marketingdatascience.ai/linear-regression-the-classic-machine-learning-algorithm-you-need-to-know-1fe0b48b06a3) | **Linear Regression** (Predicting Clicks from Impressions) |
| **Early Stage Diabetes** | [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Early+stage+diabetes+risk+prediction+dataset.) | **Classification Trees** (Risk Prediction) |
| **Credit Card Clients** | [UCI Repository / Kaggle](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset) | **KNN Classification** (Default Prediction) |
| **Ames Housing** | [AmesHousing R Package](https://cran.r-project.org/web/packages/AmesHousing/index.html) | **Regression Trees & Bagging** |
| **Hitters** | [ISLR R Package](https://cran.r-project.org/web/packages/ISLR/index.html) | **Model Selection** (Subset Selection) |
| **Smarket** | [ISLR R Package](https://cran.r-project.org/web/packages/ISLR/index.html) | **KNN** (Stock Market Direction) |

## Projects & Algorithms

### 1. Statistical Inference
* **`hypothesis_test.qmd`**
    * **Tests Implemented:** * **Z-Test & T-Test:** One-sample, Two-sample (Independent), and Paired T-tests.
        * **ANOVA:** Comparing means across multiple groups.
        * **Normality Checks:** Shapiro-Wilk Test and Q-Q Plots.
        * **Variance Homogeneity:** Bartlett’s Test / F-test.

### 2. Regression Analysis
* **`introduction_to_linear_regression.qmd`**
    * **Algorithm:** Simple Linear Regression (OLS).
    * **Goal:** Predicting Ad Clicks based on Impressions using `Meta Ads Data`.
    * **Techniques:** Residual analysis (Homoscedasticity check), $R^2$ interpretation, and confidence intervals.
* **`regression_trees.qmd`**
    * **Algorithm:** Regression Trees (CART) & **Bagging**.
    * **Goal:** Predicting House Prices in Ames, Iowa.
    * **Techniques:** * **Hyperparameter Tuning:** Grid Search for `minsplit` and `maxdepth`.
        * **Pruning:** Using Cost Complexity (`cp`) to avoid overfitting.
        * **Bagging:** Using `ipred::bagging` to reduce variance and improve RMSE.
    * **Model Selection:** Implementing Forward/Backward Stepwise Selection and Best Subset Selection using the `leaps` package.

### 3. Classification Models
* **`decision_trees_KNN.qmd`**
    * **Decision Trees:** * Built using `rpart` and tuned with `caret`.
        * Visualized using `rattle::fancyRpartPlot`.
        * Applied on **Diabetes Dataset** to predict positive/negative cases.
    * **K-Nearest Neighbors (KNN):**
        * Applied on **Credit Card** and **Stock Market** data.
        * Includes Data Normalization (Scaling) and Dummy Variable creation.
        * Cross-Validation to find the optimal $k$ value.


## Libraries Used
```r
# Machine Learning & Modeling
library(caret)       # Unified interface for ML models
library(rpart)       # Recursive Partitioning (Trees)
library(ipred)       # Bagging
library(class)       # KNN Algorithm
library(leaps)       # Subset selection (Stepwise)
library(rsample)     # Data splitting

# Visualization & Helpers
library(rpart.plot)  # Plotting trees
library(rattle)      # Fancy tree plots
library(broom)       # Tidy model output
library(flextable)   # Professional tables