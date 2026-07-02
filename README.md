# ENIAC A/B Testing & Hypothesis Testing

Coursework covering hypothesis testing fundamentals and a full A/B test case study on Eniac's "SHOP NOW" button redesign.

## Background

Eniac's Marketing team wants to increase the click-through rate (CTR) of the **"SHOP NOW"** button. Design produced three alternative versions to test against the original:

| Version | Change |
|---|---|
| **A** | Original site (control) |
| **B** | Button color changed to red |
| **C** | Button text changed to "SEE DEALS" |
| **D** | Both the B and C changes applied |

Each version's `.csv` file contains element-level click data scraped from the corresponding page snapshot (element ID, tag, name, click count, visibility, and snapshot metadata).

## Repo structure

```
eniac-ab-testing/
├── data/
│   ├── eniac_a.csv     # Control
│   ├── eniac_b.csv     # Red button
│   ├── eniac_c.csv     # "SEE DEALS" text
│   └── eniac_d.csv     # Red + "SEE DEALS"
└── notebooks/
    ├── 4_one_sample_t_test_solutions.ipynb
    ├── 5_two_sample_t_test_solutions.ipynb
    ├── 6_chi_square_test_solutions.ipynb
    └── 7_eniac_case_solutions.ipynb   # Full A/B test analysis
```

## Notebooks

1. **One-sample t-test** – testing a sample mean against a known/hypothesized population value.
2. **Two-sample t-test** – comparing means between two independent groups.
3. **Chi-square test** – testing independence/association between categorical variables.
4. **Eniac case study** – applies these tests to the A/B experiment above, comparing conversion rates across versions A–D to determine whether the button redesign meaningfully improves CTR, and by how much.

## Key questions explored

- How many versions should be tested, and what should change between them?
- Which metric best captures success — CTR, revenue per visitor, something else?
- How do we know a version's higher click count isn't just due to chance?
- How long should an experiment run to reach a reliable conclusion?

## Tools

Python (pandas, numpy, scipy.stats), Jupyter Notebook.
