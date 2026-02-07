# Regularized Raking for Better Survey Estimates

Slides from a talk on regularized raking, presented at the New York Open Statistical Programming meetup.

## Viewing the Slides

The rendered slides are available in [`nyosp_regrake.html`](nyosp_regrake.html) - you can download and open this file directly in your browser.

## Reproducing the Analysis

To rebuild the slides from source, you'll need:

### 1. R Packages

```r
install.packages(c("tidyverse", "survey", "ggrepel", "autumn"))

# Install regrake from GitHub
remotes::install_github("andytimm/regrake")
```

### 2. Data

The analysis uses polling data that must be obtained separately. Place the following files in a `data/` directory:

- `cces.rds` - 2016 Cooperative Congressional Election Study data
- `pew.rds` - 2016 Pew Research Center polling data
- `election.rds` - Election results data

These datasets can be obtained from the Code Ocean capsule for [Target Estimation and Adjustment Weighting for Survey Nonresponse and Sampling Bias](https://codeocean.com/capsule/4173151/tree/v1) (Caughey et al., 2020). The capsule contains the data files and preprocessing code needed.

### 3. Render

```bash
quarto render nyosp_regrake.qmd
```

## References

The talk draws heavily on:

- Barratt, S., Angeris, G., & Boyd, S. (2021). [Optimal Representative Sample Weighting](https://web.stanford.edu/~boyd/papers/optimal_representative_sampling.html)
- Caughey, D., et al. (2020). Target Estimation and Adjustment Weighting for Survey Nonresponse and Sampling Bias

## Related

- [`regrake`](https://github.com/andytimm/regrake) - R package implementing regularized raking
- [`Regularized-Raking`](https://github.com/andytimm/Regularized-Raking) - Earlier version of this talk with additional experiments
