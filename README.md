# Human-Caused Global Warming — A Data-Driven Case

> Reproducible analysis linking rising **CO₂** to **global temperature anomalies**, while testing and ruling out **solar irradiance** and **volcanic aerosols** as the main drivers.

![Key result](docs/fig_observed_vs_predicted.png)

---

## TL;DR (key findings)

- **CO₂ ↔ Temperature:** Strong, stable relationship.  
  Slope ≈ **0.010–0.012 °C per ppm**; **R² ≈ 0.92–0.93** (annual data, 1959–present).
- **Model comparison:** Adding solar (TSI) + volcanic (AOD/VEI) improves fit **modestly**; **CO₂ remains dominant**.
- **CO₂ doubling sensitivity:** ~**2.7 °C** per doubling (log₂ model), consistent with mainstream ranges.
- **Diagnostics:** HAC/Newey–West SEs; DW ≈ **1.85**; BP p ≈ **0.81**; max Cook’s D ≈ **0.31**; VIFs ≈ **1.0**.

The full write-up lives in **`reports/final_project.pdf`**.

---

## Project structure

```
├── data/
│   ├── raw/            # original datasets (gitignored)
│   └── processed/      # tidy annual series built by the notebook/scripts
├── docs/               # figures exported by the analysis
├── notebooks/
│   └── final_project.ipynb   # main analysis (run-all → regenerates figures/results)
├── reports/
│   └── final_project.pdf     # compiled report
├── src/
│   ├── io.py           # loaders/cleaners for each dataset
│   ├── features.py     # merge to global series, build driver panel
│   ├── models.py       # regressions + diagnostics
│   └── plots.py        # figure generation
├── requirements.txt
└── README.md
```
