# Assignment 3A — Explore and Plan

[Open the notebook in Google Colab](https://colab.research.google.com/github/gebreabgithub/python_Task_3A/blob/main/Assignment_3A_Alzheimers_Explore_and_Plan.ipynb)

The revised notebook covers all Part A requirements: a plan, an audit of all 35 variables, a data dictionary, five exploratory figures, three replacement research questions with analysis plans and answers, and data-quality limitations. Saved outputs are included. It also reviews how the three accessible notebooks linked in the class register approach their questions, distinguishing completed EDA from proposed models. The fourth linked file requires access.

## Run

1. Open the Colab link.
2. Select **Runtime → Run all**.
3. Upload the supplied `alzheimers_disease_data.csv` when prompted.

For local Jupyter use, place the CSV beside the notebook and install `pandas`, `numpy`, and `matplotlib`. No GPU is needed. The raw CSV is not bundled in this repository.

## Findings

- The file contains 2,149 patient records and 35 fields, with no missing cells or exact duplicate rows.
- MemoryComplaints and Forgetfulness disagree in 831 records (38.7%); Cohen's kappa is −0.007. Mean MMSE for both indicators minus neither is +1.19 points, with a bootstrap interval spanning zero.
- ADL and FunctionalAssessment have a weak rank correlation (0.053). Their within-sample percentile ranks differ by more than 25 points in 54.4% of records and more than 50 points in 22.9%.
- Blood-pressure ordering flags affect 186 records; LDL + HDL exceeding total cholesterol flags 578. Their union contains 719 records. Excluding these leaves 1,430 and changes memory kappa by +0.013, functional rank correlation by −0.020, and the large-rank-gap proportion by +0.12 percentage points.
- The sensitivity changes are smaller than the notebook's prespecified descriptive tolerances. This does not establish equivalence or validate the remaining records. No values are silently corrected.

These are descriptive findings from the supplied file, not causal or clinical conclusions. Provenance, diagnosis criteria, sampling and score construction require clarification.

## Sources and scope

The supplied assignment paper and Alzheimer's data dictionary define the requirements and coding. The linked Google Sheet was inspected and is a class submission register; it was not modified. Three reference notebooks were reviewed without running or editing them; their approaches are paraphrased and linked in the notebook. All analysis code here is independently implemented. The questions differ from the stated questions in those accessible submissions, but scientific novelty across the literature is not established. The functional-measure question explicitly develops a weak-correlation observation already noted in their audits.

The optional `data.h5` contains a separate three-row `Name`, `Age`, `Score` table and is unnecessary for this analysis.

All notebook code cells were executed locally without errors, including 1,000-resample bootstrap intervals, and all five figures were visually checked. Colab upload code is included; execution was validated in a local Python/Jupyter environment. Review the notebook and add group details or AI-use disclosure as required by the course before submitting it.
