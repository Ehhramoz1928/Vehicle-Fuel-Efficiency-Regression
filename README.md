# Vehicle Fuel Efficiency Prediction Using Multiple Linear Regression

## Project Overview
This repository contains a formal statistical analysis and multiple linear regression model designed to evaluate and predict vehicle fuel efficiency. [cite_start]The primary objective is to quantify the collective and individual impacts of specific mechanical attributes—gross horsepower and rear axle ratio—on fuel economy[cite: 7, 8]. 

[cite_start]This project demonstrates an end-to-end data science and statistical modeling workflow, pairing programmatic calculations in R with rigorous diagnostic testing and formal interpretation[cite: 7, 149].

## Dataset & Variables
[cite_start]The study utilizes data from the classic **Motor Trend Car Road Tests (`mtcars`)** dataset, consisting of 32 observations and 11 distinct automotive variables[cite: 13]. 

* [cite_start]**Dependent Variable ($Y$):** `mpg` — Fuel efficiency measured in Miles per (US) Gallon[cite: 14, 15].
* [cite_start]**Independent Variable ($X_1$):** `hp` — Gross horsepower, representing the engine's theoretical power output[cite: 14, 16].
* **Independent Variable ($X_2$):** `drat` — Rear axle ratio, describing the mechanical relationship between driveshaft and rear axle rotations (a proxy for gearing configuration)[cite: 14, 16].

## Key Statistical Findings
The multiple linear regression analysis yielded a robust, mathematically sound predictive framework with the following diagnostic outcomes:

* **Calculated Prediction Equation:** $$\text{mpg} = 10.790 + 4.698(\text{drat}) - 0.052(\text{hp})$$ [cite: 37]
* [cite_start]**Explanatory Power:** The model achieved an **Adjusted $R^2$ of 0.7233**, demonstrating that **72.33% of the total variance** in vehicle fuel efficiency is directly explained by the combination of horsepower and rear axle ratio[cite: 47]. 
* [cite_start]**Overall Model Significance:** The regression framework is highly significant, featuring an F-statistic of 41.52 and an overall $p$-value of **$2.318 \times 10^{-9}$** ($3.081 \times 10^{-9}$ depending on software precision), falling drastically below the critical threshold of $\alpha = 0.05$[cite: 11, 106, 108].
* **Individual Coefficient Evaluations:**
  * [cite_start]**Gross Horsepower (`hp`):** Statistically significant ($p$-value = $1.39 \times 10^{-5}$); each one-unit increase in horsepower corresponds to a **0.0518 mpg decrease** in fuel efficiency, assuming a constant axle ratio[cite: 57, 59, 134].
  * [cite_start]**Rear Axle Ratio (`drat`):** Statistically significant ($p$-value = $0.00388$); each one-unit increase in the rear axle ratio predicts a **4.6982 mpg increase** in fuel efficiency, assuming horsepower remains constant[cite: 54, 55, 131].
* **Assumptions Validated:** Residual plot analyses verified that the model completely satisfies the core regression assumptions of **homoscedasticity** (constant variance) and **normality of error terms**, ensuring the standard errors and confidence intervals are highly reliable[cite: 83, 89, 93].

## Repository Contents
* `Module One Problem Set Jupyter Notebook V2.html`: An executed HTML snapshot of the computational environment detailing data ingestion, vector type-casting, and regression summary tables.
* `MAT 303 Module One Problem Set Report Template (1) (1).docx`: The formal written report detailing the structural introduction, hypothesis formulation, parameter testing, and final statistical inferences[cite: 1, 6, 12, 18, 145].
* `README.md`: This document, serving as an executive summary of the repository's contents and analytical results.

## Technical Specifications
* **Language:** R
* **Interface:** Jupyter Notebook / RStudio
* **Primary Statistical Packages/Functions:** `lm()` (Linear Model compilation), `predict()`, `factor()`, `within()`, `sapply()`
