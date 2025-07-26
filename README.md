# Statistical Analysis Projects

This repository contains statistical analysis projects exploring relationships between variables in various datasets using regression models, hypothesis testing, and data visualization.

## Authors

Jonah Zembower, Stanislav Chernyshov, Aidan Owens, Christian Zilli, Cole Kuczynski

## Date

May 2, 2023

## Project Overview

This collection of projects focuses on applying statistical methods to real-world data problems. Each problem involves a specific dataset and a set of questions to be answered through data analysis and modeling.

## Datasets

The repository includes the following datasets, each corresponding to a specific problem analyzed in the project:

* `Final Project Dataset-1.xlsx - Problem 1.csv`: Contains data on Load (in Newtons) and Time (in seconds) for a sled moving up a ramp.
* `Final Project Dataset-1.xlsx - Problem 2.csv`: Contains Temperature and Lifetime data for a particular bacteria, used to investigate how heat affects bacteria lifetime.
* `Final Project Dataset-1.xlsx - Problem 3.csv`: Contains data on Caiman from the Amazon Basin, including Gender, WT (kg) (weight), and Genetic Marker type (Type 1 or Type 2). Type 2 is believed to be linked to tumor growth.
* `Final Project Dataset-1.xlsx - Problem 4.csv`: Contains data related to gut bacteria, including Y1 (Lactobacillus-X ppm), Y2 (Saccharomyces diameter (micro m)), Gender, X1 (Weight lbs), X2 (Height (m)), X3 (cholesterol), and Region.

## Methodologies & Findings

Each problem involved developing statistical models and assessing their assumptions.

### Problem 1: Sled Load and Time

* **Objective**: Analyze the relationship between load on a sled and the time it takes to reach the top of a ramp.
* **Methodology**: Linear regression was used.
* **Findings**:
    * The initial regression model had a high p-value and low R-squared, indicating poor predictability.
    * After removing extreme values, the model improved with a lower p-value and an increased R-squared.
    * Assumptions for linearity, normality, and homoscedasticity were generally not met, making the model not very effective for prediction. Leverage assumption was accepted.

### Problem 2: Bacteria Lifetime and Temperature

* **Objective**: Investigate the association between temperature and the lifetime of a particular bacteria.
* **Methodology**: A logarithmic linear regression model was developed.
* **Findings**:
    * The model showed a very low p-value, high R-squared, and a high F-statistic, suggesting strong predictive potential.
    * Assumptions for linearity, normality, and leverage were accepted.
    * The homoscedasticity assumption was rejected due to non-horizontal residuals.
    * Overall, the model is considered effective for predicting bacteria lifetime.

### Problem 3: Caiman Characteristics and Genetic Markers

* **Objective**: Analyze Caiman data focusing on weight, gender, and genetic marker types, including assessing differences in average weight and variance based on gender, and the proportion of Caiman with Type 2 genetic marker. Additionally, it investigates if Caiman obesity is associated with gender or genetic markers.
* **Methodology**: Box plots, F-test, confidence intervals, and regression analysis were used.
* **Findings**:
    * **Weight by Gender**: Male Caiman were found to be generally heavier than females, with higher median and quartile values.
    * **Variance by Gender**: An F-test indicated no statistically significant difference in variance between male and female Caiman weights.
    * **Proportion of Type 2 Genetic Marker**: A 95% confidence interval for the proportion of Type 2 Caiman was found.
    * **Caiman Obesity and Gender/Genetic Marker**:
        * An initial regression model with gender and genetic marker as explanatory variables showed high p-values and low R-squared.
        * Gender was removed due to its low probability and predictiveness.
        * The refined model with only genetic marker as a predictor still showed low predictability and a high p-value.
        * Assumptions for linearity, homoscedasticity, and leverage were accepted. Normality assumption was rejected.
        * Overall, the predictability of the model for Caiman weight based on genetic markers is very low, suggesting no strong association and advising against claims that Caiman obesity is related to tumor growth.

### Problem 4: Gut Bacteria and Health Indicators

* **Objective**: Analyze relationships between gut bacteria (Saccharomyces diameter and Lactobacillus-X ppm) and health indicators (weight, height, cholesterol, region).
* **Methodology**: Regression models and scatterplots were used.
* **Findings**:
    * **Saccharomyces diameter and Cholesterol**:
        * The regression model showed a very low p-value, high R-squared, and high F-statistic, suggesting a promising relationship.
        * The linearity assumption was not met (U-shaped residual plot), but normality, and leverage assumptions were accepted.
        * A possible relationship between cholesterol and average Saccharomyces diameter can be concluded.
    * **Lactobacillus-X ppm and Health Indicators**:
        * An initial regression model with region dummy variables, weight, height, and cholesterol showed statistical significance with a high R-squared and F-statistic.
        * Autocorrelation checks did not warrant variable removal.
        * Subset selection led to the removal of D1 (Africa/North and South America), Height, and Cholesterol.
        * The refined model with Weight, D2 (Asia), and D3 (Europe) had a slightly reduced R-squared but an increased F-statistic.
        * Linearity and leverage assumptions were accepted. Normality and homoscedasticity assumptions were rejected.
        * D2 (Asia), D3 (Europe), and Weight (lbs) were identified as important explanatory variables for predicting Lactobacillus-X ppm.
    * **Large-diameter Saccharomyces and Low Weight**:
        * Initial scatterplot showed no clear association.
        * The regression model confirmed no strong relationship with a very high p-value, and very low R-squared and F-statistic.
        * All four assumptions (linearity, normality, homoscedasticity, and leverage) were accepted.
        * Despite meeting assumptions, the model's predictability is worrying, and it cannot be concluded that large-diameter Saccharomyces are associated with low weight.

## Files in the Repository

* `Final Project Dataset-1.xlsx - Problem 1.csv`: Sled load and time data.
* `Final Project Dataset-1.xlsx - Problem 2.csv`: Bacteria lifetime and temperature data.
* `Final Project Dataset-1.xlsx - Problem 3.csv`: Caiman data.
* `Final Project Dataset-1.xlsx - Problem 4.csv`: Gut bacteria and health indicators data.
* `Final Project.pdf`: The complete project report in PDF format, detailing the analysis and findings for all problems.
* `SMA 265 Final Project SP2023.docx`: The project prompt outlining the problems and requirements.
