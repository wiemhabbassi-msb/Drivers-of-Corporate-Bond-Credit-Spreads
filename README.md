# Determinants of Corporate Bond Credit Spreads

Stata project that examines which factors explain differences in firms' borrowing costs (corporate bond credit spreads).

## About

- **Goal:** find what drives credit spreads (cost of debt)
- **Dependent variable:** credit spread (`sprben_matlab`)
- **Data:** 3,496 bond observations, 39 variables (3,408 used in the main regression)
- **Course:** Advanced Econometrics, Professor Anis Samet

## Hypotheses

- **H1:** Higher leverage increases spreads (not supported, p = 0.663)
- **H2:** Higher profitability lowers spreads (supported)
- **H3:** Better credit rating lowers spreads (supported)
- **H4:** Stronger debt enforcement lowers spreads (supported)
- **H5:** Longer maturity increases spreads (supported)

## What We Did

- Descriptive statistics, histogram and scatter plots
- Pairwise correlations and multicollinearity check (VIF, mean 1.06)
- OLS regression of credit spread on the main variables
- Heteroskedasticity test (Breusch-Pagan) and robust standard errors
- Robustness checks:
  - alternative leverage measure
  - firm size control
  - civil law dummy
  - callable bonds
  - country-clustered standard errors
  - country fixed effects

## Results

- **Credit rating** is the strongest driver (about -33 per rating notch)
- Profitability and debt enforcement lower spreads; longer maturity raises them
- Leverage is not significant in the main model
- Main model: adjusted R² of 46.3%, rising to 50.1% with country fixed effects
- Callable bonds have significantly higher spreads; larger firms have lower spreads
- Results hold across the robustness checks

## Files

- `Analysis.do`: Stata do-file with all the code
- `Sorting.smcl`: Stata log with all the output
- `Drivers_of_Corporate_Bond_Credit_Spreads_Presentation.pdf`: project presentation
- `1-CS-data-CSV.csv`: dataset (semicolon-separated)
