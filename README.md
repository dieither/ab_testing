# A/B Testing Analysis

This repository contains an A/B testing analysis performed in the notebook [`AB_testing.ipynb`](./AB_testing.ipynb). The main goal is to evaluate whether changes between control and test groups lead to statistically significant improvements in conversion metrics.

## Project Overview

A/B testing is a standard method used to compare two versions of a feature or product to determine which performs better. In this notebook, we:

* Load and clean the data for A/B test results
* Calculate key metrics like conversion rates
* Conduct statistical hypothesis testing (z-test)
* Identify significant changes in user behavior
* Provide summary insights on test results

## Methodology

* **Conversion metrics analyzed:** add\_to\_cart, begin\_checkout, add\_payment\_info, etc.
* **Statistical test used:** Z-test for proportions
* **Significance level:** 0.05
* **Output:** metric-level change percentage, p-values, z-statistics, and significance flags

## Files

* `AB_testing.ipynb` – Main analysis notebook
* (Optional: `data/` folder if you want to add raw data)

## How to Use

To run the analysis:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
open AB_testing.ipynb in Jupyter or VSCode
```

> Requirements: `pandas`, `numpy`, `scipy`, `matplotlib` (install via `pip install -r requirements.txt` if needed)

## Example Output

| Metric              | Group A CR | Group B CR | Δ (%)  | p-value | Significant |
| ------------------- | ---------- | ---------- | ------ | ------- | ----------- |
| add\_payment\_info  | 3.55%      | 3.42%      | -3.66% | 0.116   | ❌ No        |
| add\_shipping\_info | 4.88%      | 5.28%      | +8.20% | 0.008   | ✅ Yes       |

## Conclusion

This notebook helps identify which experiments yield statistically significant changes in user behavior, supporting data-driven product decisions.
