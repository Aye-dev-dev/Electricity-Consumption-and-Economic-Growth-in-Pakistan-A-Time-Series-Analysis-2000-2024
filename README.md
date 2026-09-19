# How Electricity Fuels Pakistan's Economic Growth: A Time-Series Analysis

**Authors:** Ayesha Ashraf & Muhammad Abdullah

A time-series econometric study examining the relationship between electricity consumption and GDP growth in Pakistan (2000–2024), set within a Cobb-Douglas framework.

## Overview

Electricity is a fundamental driver of economic growth — powering industries, households, and innovation. For Pakistan, electricity consumption is often treated as a proxy for industrialization, infrastructure expansion, and development progress. But the direction of the relationship is debated: does electricity consumption drive GDP growth, or does GDP growth drive electricity demand?

This study uses annual time-series data (2000–2024) to examine that relationship, controlling for inflation and unemployment, and applying a full diagnostic-correction pipeline to address the econometric issues common in macroeconomic time series.

## Research Question & Hypotheses

**Research Question:** Does electricity consumption drive economic growth, or does economic growth drive electricity consumption?

- **H0:** Electricity consumption positively affects GDP growth.
- **H1:** GDP growth positively affects electricity consumption.

## Model

GDP_Growth(t) = β0 + β1·ln(Electricity_t) + β2·(Inflation_t) + β3·(Unemployment_t) + ε_t

| Variable | Description |
|---|---|
| GDP_Growth(t) | Annual GDP growth rate |
| ln(Electricity_t) | Log of electricity consumption |
| Inflation_t | Annual inflation rate |
| Unemployment_t | Unemployment rate |
| ε_t | Random error term |

## Methodology

- **Data:** Annual time-series data for Pakistan (2000–2024) — GDP growth, electricity consumption, inflation, and unemployment
- **Stationarity testing:** Augmented Dickey-Fuller (ADF) unit root tests; non-stationary variables converted to first differences
- **Correlation analysis:** Checked for multicollinearity among predictors
- **Estimation:** OLS regression, with corrections applied across five specifications:
  1. OLS (baseline)
  2. OLS with robust standard errors
  3. Newey-West (lag 2), correcting for autocorrelation
  4. Prais-Winsten, correcting for serial correlation
  5. First-difference model, addressing non-stationarity
- **Diagnostics:** Heteroskedasticity, residual normality, and multicollinearity tests

## Key Findings

Contrary to the initial hypothesis, **electricity consumption did not show a statistically significant relationship with GDP growth** in any specification — the coefficient on ln(electricity) remained insignificant across the OLS, robust, Newey-West, and Prais-Winsten models.

**Inflation emerged as the more robust and significant driver** once autocorrelation and non-stationarity were corrected for:
- OLS (uncorrected): insignificant
- Newey-West: significant (p < 0.1)
- Prais-Winsten: significant (p < 0.05)
- First-difference: strongly significant (p < 0.01), with the coefficient strengthening from –0.69 to –1.07 across corrections

Model fit also improved substantially after correction, with R² rising from 0.136 (baseline OLS) to 0.328 (first-difference model) — suggesting the uncorrected OLS model understated the true relationships due to serial correlation and non-stationarity in the data.

Unemployment remained insignificant and inconsistent across all specifications.

## Conclusion & Policy Implications

The results suggest that while Pakistan's electricity consumption has trended upward over the study period, its statistical link to GDP growth is weaker than commonly assumed once proper time-series corrections are applied — pointing to the likely role of omitted variables (e.g., capital formation, trade openness, energy pricing) not captured in this model.

**Policy recommendations:**
- Continue investment in electricity infrastructure — generation capacity, grid reliability, and rural electrification — as a development priority in its own right, independent of this study's statistical findings on GDP linkage
- Integrate energy policy with broader industrial and digital growth strategy
- Monitor inflation and labor market conditions, given inflation's demonstrated significance in the corrected models
- Improve future model specifications by incorporating capital formation, trade openness, and energy pricing data

## Repository Contents

| File | Description |
|---|---|
| `relationship_between_electricity_consumption_and_gdp_growth.docx` | Full research paper |
| `A_time_series_analysis.pptx` | Presentation summarizing methodology, results, and policy implications |

## Tools Used

Time-series econometrics (OLS, Newey-West, Prais-Winsten, first-differencing), stationarity and diagnostic testing (ADF, heteroskedasticity, multicollinearity)

## Limitations

This study is based on a relatively small annual sample (n = 25 after first-differencing), which limits statistical power. Results should be interpreted as suggestive rather than conclusive, and the model likely omits relevant structural variables (capital formation, trade openness, energy pricing) that could explain more of the variation in GDP growth.

---

*Co-authored as part of independent undergraduate research at the Lahore School of Economics.*
