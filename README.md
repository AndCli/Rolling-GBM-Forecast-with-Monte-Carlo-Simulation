# Rolling GBM Forecast with Monte Carlo Simulation

## Overview
This project implements a rolling-window forecasting framework for financial time series
based on the Geometric Brownian Motion (GBM) model.

At each time step, GBM parameters are estimated using a fixed-length rolling window of
log-returns. One-step-ahead price forecasts are then generated via Monte Carlo simulation,
together with 95% confidence intervals.

## Methodology
- Daily log-returns are computed from historical prices
- GBM drift and volatility are estimated on a rolling window
- One-step-ahead price distributions are simulated using Monte Carlo methods
- Forecast accuracy is evaluated through confidence interval coverage

## Project Structure
gbm-rolling-montecarlo-forecast/
├── R/ # Core functions
├── data/ # Data instructions (raw data excluded)
├── output/ # Generated outputs
└── run_analysis.R # Main execution script


## Data
Raw data are not included in this repository.

The analysis requires a dataset containing:
- Date
- Closing price

Comparable data can be obtained from public sources such as Yahoo Finance or Nasdaq.

## How to Run
1. Place the price dataset in the `data/` folder
2. Run `run\_analysis.R`
3. The coverage rate is saved in `output/coverage\_summary.txt`

## Tools
- R
- tidyverse
- readxl
- lubridate
