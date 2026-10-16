<!-- order: 1 -->
# About

This site shows results of a **statistically downscaled CMIP6 dataset of daily maximum near-surface air
temperature (Tmax) for Virginia** at about 4 km (the PRISM 1/24-degree grid), 2015-2100, under three scenarios:
SSP2-4.5, SSP3-7.0 and SSP5-8.5, from 16 global climate models (19 for SSP5-8.5).

## How the data were made
1. **Bias correction** of each model's daily Tmax on its own grid against PRISM observations 1981-2014
   (empirical quantile mapping per calendar month; for the future, quantile delta mapping in 30-year windows).
2. **Downscaling** to 4 km with a residual analog method: a historical PRISM day with a similar coarse pattern
   provides the fine-scale detail, and the bias-corrected model value is kept exactly at the coarse grid points.
3. **Checks**: every model and scenario passed quality control; the method was validated against PRISM 2015-2024.

## How to read the results
- Changes are relative to each model's own bias-corrected **1995-2014** climate; periods follow IPCC AR6
  (2021-2040, 2041-2060, 2081-2100).
- Ensemble values are medians of equally weighted models; ranges say which percentiles they are, and **n**
  (the number of models) is printed on every figure.
- Scenario colours follow the IPCC AR6 style: SSP2-4.5 orange, SSP3-7.0 red, SSP5-8.5 dark red.

## Limitations
The CMIP6 models are warmer than observed in the recent summer upper tail (about 90 % of that is inherited from
the models, not from the downscaling), so counts of very hot days lean high; the ensemble is unconstrained and
equally weighted; each model contributes one run. Details are on each result page.

Shammunul Islam, Climate Dynamics, George Mason University (advisor: Dr. Luis Ortiz).
