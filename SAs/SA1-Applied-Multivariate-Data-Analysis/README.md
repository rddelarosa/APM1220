# Multivariate Analysis of the Physicochemical Characteristics of Vinho Verde Wines

## Research Questions

# This project examines the chemical properties of Portuguese Vinho Verde wines and aims to answer three main research questions:

1. **MANOVA:** Is there a significant difference between red and white wines based on fixed acidity, volatile acidity, residual sugar, and chlorides when these variables are considered together?
2. **PCA:** Can the 11 physicochemical variables be reduced to a smaller number of principal components while still explaining a large part of the variation in the data?
3. **EFA:** What underlying factors can help explain the relationships among the physicochemical properties of wine?

## Dataset Description

This study uses the combined Wine Quality Dataset, which contains chemical measurements of Portuguese Vinho Verde wines. It has 6,497 observations, including 1,599 red wine samples and 4,898 white wine samples. The dataset includes 11 continuous physicochemical variables, such as acidity, residual sugar, chlorides, sulfur dioxide, density, pH, sulphates, and alcohol. It also includes wine color and a numerical quality score.

## Dataset Source

- **Source:** UCI Machine Learning Repository
- **URL:** [https://archive.ics.uci.edu/dataset/186/wine+quality](https://archive.ics.uci.edu/dataset/186/wine+quality)
- **Original Study:** Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009). Modeling wine preferences by data mining from physicochemical properties. *Decision Support Systems, 47*(4), 547–553.
- **License:** Creative Commons Attribution 4.0 International (CC BY 4.0).

## Statistical Methods

The following statistical methods were used in the analysis:

- **Exploratory Data Analysis (EDA):** Boxplots, density plots, and correlation matrices were used to examine the data, identify possible outliers, and check relationships between variables.
- **Multivariate Analysis of Variance (MANOVA):** Pillai's Trace was used to test whether red and white wines differ based on the four selected chemical properties. Follow-up ANOVAs were also performed to examine each variable separately.
- **Principal Component Analysis (PCA):** Correlation matrices, eigenvalues, and scree plots were used to identify a smaller number of components that explain the variation in the 11 variables.
- **Exploratory Factor Analysis (EFA):** Principal Axis Factoring with Oblimin rotation was used to explore groups of related variables and identify possible underlying factors.

## Summary of Major Findings

- **MANOVA:** The results showed a significant difference between red and white wines based on the four selected chemical properties. The reported Pillai's Trace was 0.631, indicating a clear difference between the two groups when the variables were considered together.
- **PCA:** The 11 physicochemical variables were summarized into three principal components, which explained 64.36% of the total variation. These components were mainly related to sulfur dioxide and acidity, density and alcohol, and other acidity characteristics.
- **EFA:** The analysis suggested three possible factors related to sulfur dioxide and sweetness, density and alcohol, and acidity and pH. However, these results should be interpreted carefully because the KMO value was low and the analysis produced an estimation issue.
- **Overall Findings:** The results suggest that several chemical properties are related to one another and that red and white wines have different chemical profiles. PCA and EFA provided ways to summarize these relationships, although the EFA results may need further checking.

## Software Used

- **Programming Language:** R
- **Environment:** Kaggle Notebooks
- **Packages Used:**
  - `tidyverse` – Data manipulation and visualization
  - `corrplot` – Correlation matrices
  - `psych` – Factor analysis and descriptive statistics
  - `factoextra` – PCA visualization
  - `effectsize` – Effect size calculations
  - `heplots` – Box's M test

## Instructions for Reproducing the Analysis

1. Clone the repository to your local machine using the following command:

   `git clone <repository_url>`

2. Make sure R and RStudio are installed, along with the required packages.

3. Check that the project folders are arranged as follows:
   - `/data/` contains `winequality-red.csv` and `winequality-white.csv`.
   - `/code/` contains `SA1_Wine_Analysis.R`.

4. Open `SA1_Wine_Analysis.R` in RStudio.

5. Set the working directory to the location of the script or update the file paths to match your folder setup.

6. Run the script from top to bottom to reproduce the data cleaning, graphs, statistical analyses, and diagnostic checks.
