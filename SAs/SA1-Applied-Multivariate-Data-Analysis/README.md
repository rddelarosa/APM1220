# Multivariate Analysis of the Physicochemical Characteristics of Vinho Verde Wines

## Research Questions

This project investigates the physicochemical properties of Portuguese Vinho Verde wines to answer three primary research questions:

1. **MANOVA:** Do red and white wines differ significantly in their overall physicochemical characteristics when several characteristics (fixed acidity, volatile acidity, residual sugar, and chlorides) are considered simultaneously?
2. **PCA:** Can the 11 physicochemical measurements of wine be summarized using a smaller number of principal components while retaining a substantial proportion of the total variability?
3. **EFA:** What underlying latent dimensions or factors explain the relationships among the physicochemical characteristics of wine?

## Dataset Description

The analysis utilizes the combined Wine Quality Dataset, which contains physicochemical measurements of Portuguese Vinho Verde wines. The dataset comprises 6,497 total observations, consisting of 1,599 red wine samples and 4,898 white wine samples. It includes 11 continuous physicochemical variables (e.g., acidity, sugar, chlorides, sulfur dioxide, density, pH, sulphates, alcohol), a categorical wine color variable, and an integer-based sensory quality score.

## Dataset Source

* **Source:** UCI Machine Learning Repository
* **URL:** [https://archive.ics.uci.edu/dataset/186/wine+quality](https://archive.ics.uci.edu/dataset/186/wine+quality)

* **Original Study:** Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009). Modeling wine preferences by data mining from physicochemical properties. *Decision Support Systems*, 47(4), 547-553.
* **License:** Creative Commons Attribution 4.0 International (CC BY 4.0).



## Statistical Methods

The following multivariate techniques were applied to the dataset:

* **Exploratory Data Analysis (EDA):** Boxplots, density plots, and correlation matrices to assess distributions, outliers, and multicollinearity.
* **Multivariate Analysis of Variance (MANOVA):** Pillai's Trace and follow-up univariate ANOVAs to test for significant differences between red and white wine profiles.
* **Principal Component Analysis (PCA):** Dimensionality reduction utilizing correlation matrices, eigenvalues, and scree plots to identify composite chemical profiles.
* **Exploratory Factor Analysis (EFA):** Principal Axis Factoring with Oblimin rotation to uncover latent chemical structures and shared variance.

## Summary of Major Findings

* **MANOVA:** Red and white wines exhibit fundamentally distinct physicochemical profiles. Wine color accounts for approximately 63% of the multivariate variance, driven significantly by differences in fixed acidity, volatile acidity, residual sugar, and chlorides.
* **PCA:** The 11 physicochemical measurements can be effectively reduced to three principal components that explain 64.36% of the total variance. These components capture the "Sulfite/Acidity Profile", "Body/Alcohol Profile", and "pH Profile" of the wines.
* **EFA:** Three underlying latent factors govern the chemical relationships within the dataset: a "Sulfite and Sweetness Factor", a "Body and Alcohol Factor", and an "Acidity and pH Factor."
* **Integration:** Both PCA and EFA confirm that wine chemistry is highly structured, primarily balancing preservation requirements (sulfites/sugar), physical body (density/alcohol), and tartness (acidity/pH).

## Software Used

* **Language:** R
* **Environment:** RStudio / Kaggle Notebooks
* **Key Packages:** `tidyverse` (data manipulation and visualization), `corrplot` (correlation matrices), `psych` (EFA and descriptive statistics), `factoextra` (PCA visualization), `effectsize` (MANOVA effect sizes), and `heplots` (Box's M test).

## Instructions for Reproducing the Analysis

1. Clone this repository to your local machine: `git clone <repository_url>`
2. Ensure R and RStudio are installed, along with the required packages listed above.
3. Verify the directory structure matches the expected format:
* `/data/` containing `winequality-red.csv` and `winequality-white.csv`
* `/code/` containing `SA1_Wine_Analysis.R`


4. Open the `SA1_Wine_Analysis.R` script in RStudio.
5. Set your working directory to the source file location or update the data import paths to match your local directory structure.
6. Run the script sequentially from top to bottom to reproduce the data cleaning, visualizations, statistical outputs, and model diagnostics.
