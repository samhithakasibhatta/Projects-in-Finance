# CAPM vs Fama-French Models: Bias, Variance and Irreducible Noise

A simulation-based study of model error in asset pricing.

## Overview

This project investigates whether prediction error in CAPM, Fama-French 3-factor, and Fama-French 5-factor models can be understood through the bias-variance-noise framework.

A controlled simulated data-generating process is used so that the true systematic return function is known. The models are then repeatedly estimated on different training samples.

The project separates:

- **Squared bias** from model misspecification
- **Prediction variance** from training-sample instability
- **Irreducible noise** from random return shocks

## Research Question

How do model misspecification and estimation uncertainty contribute to prediction error in commonly used asset-pricing models?

## Methodology

The simulated true process contains:

- Market risk
- Size
- Value
- Profitability
- Investment
- An omitted momentum factor
- A nonlinear market effect
- A market-size interaction

CAPM, FF3, and FF5 are repeatedly fitted to simulated samples and evaluated on a common test set.

## Important Caveat

The simulated DGP is not claimed to be the true model of financial returns. Simulation is used as a controlled laboratory for understanding statistical mechanisms that cannot be directly observed in real markets.

## Repository Structure

```text
CAPM-FF-Bias-Variance/
├── README.md
├── notebooks/
│   └── CAPM_FF_Bias_Variance.ipynb
├── results/
│   └── CAPM_FF_Bias_Variance_Results.csv
└── figures/
```

## Tools

Python, NumPy, Pandas, Matplotlib, Scikit-learn, Jupyter.

## Extensions

- Correctly specified FF5 DGP
- Sample-size experiments
- Time-varying beta
- Rolling regressions
- State-space models
- Kalman filters
- Application to real factor-return data
