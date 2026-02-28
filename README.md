# Migration Birth Rate Analysis (R)

This repository contains an analysis of the relationship between standardized net migration rates and total fertility rates (TFR) across 217 countries over a 60-year period using World Bank data. The project fits linear, quadratic, and log-quadratic regression specifications and evaluates the role of socioeconomic controls (urbanization, female employment, GDP) in shaping fertility outcomes.

## Files

- analysis/
   - _metadata.yml
   - analysis.qmd — primary Quarto/RMarkdown analysis notebook (EDA, model estimation, figures, and tables)
- data/
   - data_constructed/
       - analytical_data.RData — cleaned, analysis-ready dataset
   - data_raw/
       - world_bank_data.csv — raw World Bank downloads      
- utils/
   - check_packages.R — helper that installs/loads required packages
   - functions.R — project-specific helper functions
- migration-birthrate-analysis.Rproj — RStudio project file
- final_paper.pdf — final report
- LICENSE — license file for repository
- README.md — this file

## Project Overview

- **Dataset**: Country-year panel drawn from the World Bank: standardized net migration (z-score), total fertility rate (TFR), GDP (2015 USD), female employment ratio, urban population percent, and other covariates.
- **Objective**: Assess how standardized net migration relates to fertility across countries and time, comparing linear, quadratic, and log-quadratic specifications and controlling for socioeconomic variables.
- **Audience**: Policy makers/analysts, demographic researchers, and the general public.

## Techniques & Tools

- Linear regression (lm) and model comparison
- Visualization: ggplot2 (line plots, LOESS/GAM smoothing, residual diagnostics)
- Summary tables: gt, modelsummary
- R packages used include tidyverse (dplyr, tidyr, ggplot2), here, gt, broom, mgcv, modelsummary, and quarto/rmarkdown

## Main Findings

- Linear and quadratic models show a modest negative relationship between standardized net migration and fertility (approx. −0.028 in linear specs).
- The log-quadratic specification reveals non-linear dynamics and can improve model fit (R2 increased from 0.400 to 0.416 in the reported results).
- Urbanization is consistently negatively associated with fertility; female employment shows mixed effects, positive in some linear/quadratic specifications but not significant in the log-quadratic model.
- Overall, migration’s impact on fertility is context-dependent and mediated by socioeconomic structure.


