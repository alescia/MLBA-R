# MLBA-R

This repository presents an extension of the multiattribute linear ballistic accumulator model to allow for choice revisions. 

We provide RStan code for the model, and commands for the simulations, estimations and post-estimation on two experiments.

## Dependencies

To run the simulations and model estimation you need R and the following packages (available on CRAN):

- `rstan` and `cmdstanr` -- for Bayesian modeling and inference.
- `posterior` and `bayesplot` -- for posterior analysis and plotting results

- other necessary libraries are loaded in the file MLBAR_LOADING_LIBRARIES.Rmd

## How to run the analysis

- Download or clone this repository.
- Open the .Rproj file.
- Open and run the following files:
  - MLBAR_LOADING_LIBRARIES.Rmd : loads necessary packages and functions to do graphs and tables
  - MLBAR_SIMULATIONS.Rmd : to perform simulations of choices for the attraction, similarity and compromise effects
  - MLBAR_ESTIMATION.Rmd : to perform estimates of the parameters of the MLBAR model and outputs resulting estimates
  - MLBAR_POST_ESTIMATION.Rmd : to obtain post-estimation based on estimated parameters and simulate resulting choices

## Models

- stan models are provided for three types of regressions:
  - a model with no revisions in choice and no mixed effects: mlba_single_v8_Frechet_generalized.stan
  - a model with revisions in choice and no mixed effects: mlba_revision_v9_Frechet_generalized.stan
  - a model with revisions in choice and mixed effects: mlba_revision_v9_Frechet_generalized_mixed.stan

### Data
Data is saved to the `data/` folder. 

### Results
Estimation results are saved to the `results/` folder. We only loaded the results of the first chain (sample of 2000) on GitHub.

This leads to slight differences in the figures and tables compared to the paper which reports results for 16 chains.

### Figures
Figures are saved to the `graphs/` folder.

### Tables
Tables are saved to the `tables/` folder. They contain the exact same information as in the paper.

## License

Creative Commons Attribution-NonCommercial-ShareAlike -- CC BY-NC-SA
