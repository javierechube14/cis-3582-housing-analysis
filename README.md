# Ideological vs. Generational Cleavages in Spanish Housing Policy (CIS Study No. 3582)

[![R](https://img.shields.io/badge/R-4.x-276DC3?logo=r&logoColor=white)](https://www.r-project.org/)
[![Quarto](https://img.shields.io/badge/Quarto-Reproducible_Report-75AADB?logo=quarto&logoColor=white)](https://quarto.org/)
[![Data](https://img.shields.io/badge/Data-CIS_Barometer_3582-1E3A8A)](https://www.cis.es/)

## Overview
Public discourse surrounding the Spanish housing crisis frequently frames the conflict as a purely **generational divide** between younger renters and older homeowners. Using microdata from the **Centro de Investigaciones Sociológicas (CIS) Barometer Study No. 3582** (October 2026; $N = 5,024$), this reproducible study tests whether public preferences over housing policy are driven primarily by generational cohorts or by ideological self-placement.

## Key Empirical Findings
1. **Ideology Dominates Over Generation:** Ideological self-placement (`ESCIDEOL`) exhibits a substantial association with normative housing framing ($\chi^2 = 644.39, p < 0.001, V = 0.262$), whereas generational cohort shows a negligible effect size ($V = 0.044$). While **97%** of left-leaning respondents prioritize housing as a constitutional right over a market asset, that share drops to **65%** among right-leaning respondents.
2. **Null Generational Net Effects:** In a multivariate binary logistic regression controlling for ideology, gender, and educational attainment—and verified via post-stratification survey weighting (`pesocca`)—**no age cohort differs significantly from young adults aged 18–29** ($p > 0.09$ across all cohorts).
3. **Gender & Educational Cross-Pressures:** Holding ideology and age constant, women have more than twice the relative odds of prioritizing the constitutional right frame compared to men ($OR = 2.05$ weighted), whereas respondents with university degrees align comparatively more with market-oriented certainty ($OR = 0.54$ weighted).

## Repository Structure
* `housing_cis_3582.qmd` — Full reproducible Quarto source document containing data cleaning, bivariate tests ($\chi^2$, Cramér's $V$), unweighted and survey-weighted logistic regressions, and `ggplot2` visualizations.
* `housing_cis_3582.html` — Self-contained rendered HTML report.
* `3582.sav` — Original SPSS microdata file from CIS Study No. 3582.

## Methodology & Tech Stack
* **Statistical Methods:** Cross-tabulations, Pearson's $\chi^2$, Cramér's $V$, Binary Logistic Regression (`glm`), and Survey-Weighted Quasibinomial Robustness Checks (`pesocca`).
* **R Packages:** `tidyverse`, `haven`, `broom`, `scales`, `knitr`, `patchwork`.
