# Precision Feeding and Growth Variability

This repository contains data and reproducible R analyses associated with the
manuscript:

> **Increasing the threonine-to-lysine ratio improves the growth performance
> of slow-growing pigs within group precision feeding**

Pedro Righetti Arnaut, Candido Pomar, Luciano Hauschild, and Aline Remus.  
Submitted to the *Journal of Animal Science* (2026).

## About the study

The manuscript examines growth variability and the response of slow-growing
pigs to increasing dietary threonine-to-lysine ratios under group precision
feeding. The accompanying analyses evaluate whether growth-rate categories are
associated with birth weight, quantify within-animal changes in average daily
gain, and project the observed growth responses to a 120 kg market weight.

The feeding treatments represented in the data are conventional phase feeding
at 100% of an ideal threonine-to-lysine ratio of 0.65 (`CPF100`) and group
precision feeding at 80%, 100%, 120%, and 140% of that ratio (`GPF80`,
`GPF100`, `GPF120`, and `GPF140`). Animals are classified into Fast, Medium,
and Slow growth-rate categories.

## Analyses included

The R Markdown document covers:

- growth-rate categories and birth weight;
- the timing of body-weight differences among slow-growing pigs;
- within-animal changes in average daily gain;
- projection of observed growth responses to a 120 kg body weight;
- bootstrap uncertainty intervals for projected differences;
- projected growth trajectories; and
- feed-cost comparisons during the 21-day experimental period, including a
  transparent table of ingredient reference costs and source notes.

Projections to 120 kg are extrapolations from the measured average daily gain;
body weight at 120 kg was not directly observed. Feed-cost calculations use
2025 reference ingredient prices and should be interpreted as comparisons among
treatments rather than current absolute costs.

## Repository files

- `pedro_thr_analyses.Rmd` — reproducible analysis and figures;
- `growth_rates_all_phases.csv` — growth records by pig and phase;
- `feed_cost_by_pig.csv` — feed-cost records for the experimental period;
- `CITATION.cff` — machine-readable citation metadata;
- `PAPER_DESCRIPTION.md` — concise description of the associated manuscript;
- `LICENSE` — MIT License.

## Reproducing the analyses

Keep the R Markdown file and both CSV files in the same folder. The analyses use
base R. The `rmarkdown` and `knitr` packages are required only to generate the
HTML document.

```r
rmarkdown::render("pedro_thr_analyses.Rmd")
```

The bootstrap analysis uses a fixed random seed (`20260827`) for
reproducibility.

## Citation

When using the code for **growth categories and birth weight**,
**within-animal growth response**, or **projection to market weight**, please
cite:

Pedro Righetti Arnaut, Candido Pomar, Luciano Hauschild, and Aline Remus (2026).
*Increasing the threonine-to-lysine ratio improves the growth performance of
slow-growing pigs within group precision feeding*. Manuscript submitted to the
*Journal of Animal Science*.

The manuscript is submitted, not in press. Please update the publication status
and bibliographic information after acceptance or publication.

## Contact

**Corresponding author:** Aline Remus  
[aline.remus@agr.gc.ca](mailto:aline.remus@agr.gc.ca)  
Additional email: [alnremus@gmail.com](mailto:alnremus@gmail.com)

## License

The software is distributed under the [MIT License](LICENSE). The license
governs reuse of the software; the citation information above explains how to
acknowledge the associated scientific work.
