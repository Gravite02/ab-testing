# HEXAL A/B Testing & Hypothesis Testing

Coursework covering hypothesis testing fundamentals and a full A/B test case study on Hexal's "SHOP NOW" button redesign.

## Background

Hexal's Marketing team wants to increase the click-through rate (CTR) of the **"SHOP NOW"** button. Design produced three alternative versions to test against the original:

| Version | Change |
|---|---|
| **A** | Original site (control) |
| **B** | Button color changed to red |
| **C** | Button text changed to "SEE DEALS" |
| **D** | Both the B and C changes applied |

Each version's `.csv` file contains element-level click data scraped from the corresponding page snapshot (element ID, tag, name, click count, visibility, and snapshot metadata).

## Repo structure

```
ab-testing/
├── data/
│   ├── hexal_a.csv     # Control
│   ├── hexal_b.csv     # Red button
│   ├── hexal_c.csv     # "SEE DEALS" text
│   └── hexal_d.csv     # Red + "SEE DEALS"
└── notebooks/
    └── hexal_case_solutions.ipynb   # Full A/B test analysis
```

> **Note:** the `data/` CSVs are not yet committed — see `data/README.md`.

## Notebooks

1. **Hexal case study** – applies these tests to the A/B experiment above, comparing conversion rates across versions A–D to determine whether the button redesign meaningfully improves CTR, and by how much.

## Key questions explored

- How many versions should be tested, and what should change between them?
- Which metric best captures success — CTR, revenue per visitor, something else?
- How do we know a version's higher click count isn't just due to chance?
- How long should an experiment run to reach a reliable conclusion?

## Tools

Python (pandas, numpy, scipy.stats), Jupyter Notebook.
