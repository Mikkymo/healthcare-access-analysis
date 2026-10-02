# Analytical Notes

[Back to project overview](../README.md)

## Objective

How do admissions, length of stay, billing, and test-result labels vary across the supplied practice records?

## Data and method

Explore admission types and conditions, length of stay, billing by condition and insurer, and medication versus test-result labels. Treat the Random Forest exercise separately from descriptive findings and assess its validation design.

## Reported results and definitions

| Notebook-reported observation | Result |
| --- | ---: |
| Records | 55,500 |
| Variables | 15 |
| Average length of stay | Approximately 15.5 days |
| Average billing | Approximately $25,500 |
| Random Forest accuracy | 41.69% |

The classification result requires comparison with a baseline, class distribution, and validation design before judging model usefulness.

## Review the analysis

Open `healthcare_analysis.ipynb` in Jupyter or VS Code, with the CSV in the repository directory. Install the packages imported by the notebook. Package versions are not pinned; no runnable Dash app is included.

## Interpretation

- Use admission and billing summaries to define questions for further investigation.
- Assess classification performance against suitable baselines and validation checks.
- Confirm dataset representativeness before applying findings to operational decisions.

## Limitations

This is a public practice dataset, not verified hospital operational data. Category balance limits real-world interpretation. Associations do not establish treatment effects, and the classifier is not established as clinically useful.

## Historical material

Earlier reports and presentations remain in the archive as historical deliverables. They have not been rewritten or independently reconciled in this documentation cleanup. Use the current project overview for the stated findings and definitions.

## Dataset source

[Prasad Patil healthcare practice dataset on Kaggle](https://www.kaggle.com/datasets/prasad22/healthcare-dataset).
