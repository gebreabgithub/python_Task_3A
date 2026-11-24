# Assignment 3A — Explore and Plan

[Open the notebook in Google Colab](https://colab.research.google.com/github/gebreabgithub/python_Task_3A/blob/main/Assignment_3A_Alzheimers_Explore_and_Plan.ipynb)

The notebook covers all Part A requirements: a plan, an audit of all 35 variables, a data dictionary, five exploratory figures, three distinct research questions with analysis plans and preliminary answers, and data-quality limitations. Saved outputs are included.

## Run

1. Open the Colab link.
2. Select **Runtime → Run all**.
3. Upload the supplied `alzheimers_disease_data.csv` when prompted.

For local Jupyter use, place the CSV beside the notebook and install `pandas`, `numpy`, and `matplotlib`. No GPU is needed. The raw CSV is not bundled in this repository.

## Findings

- The file contains 2,149 patient records and 35 fields, with no missing cells or exact duplicate rows.
- Recorded diagnosis is associated with a 4.27-point lower mean MMSE, with overlapping distributions.
- Physical activity and ADL show almost no monotonic association (Spearman rho −0.014).
- Education-related MMSE differences are small and inconsistent across age bands.
- Cross-field checks flag 186 blood-pressure ordering conflicts and 114 LDL/total cholesterol conflicts. No values are silently corrected.

These are descriptive findings from the supplied file, not causal or clinical conclusions. Provenance, diagnosis criteria, sampling and score construction require clarification.

## Sources and scope

The supplied assignment paper and Alzheimer's data dictionary define the requirements and coding. The linked Google Sheet was inspected and is a class submission register; it was not modified. The optional `data.h5` contains a separate three-row `Name`, `Age`, `Score` table and is unnecessary for this analysis.

All notebook code cells were executed locally without errors, and all five figures were visually checked. Colab upload code is included; execution was validated in a local Python/Jupyter environment. Review the notebook and add group details or AI-use disclosure as required by the course before submitting it.
