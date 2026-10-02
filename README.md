# Healthcare Admissions and Billing Analysis
### Descriptive analysis and classification limits

A Python capstone exploring 55,500 records and 15 variables from Prasad Patil’s public healthcare practice dataset, covering admissions, length of stay, billing, and test-result labels.

**Tools:** Python · pandas · NumPy · Jupyter  
**Analyst:** Chukwuemeka Ogo

**[View dashboards](docs/dashboard-gallery.md)** · [Read analytical notes](docs/analytical-notes.md)

## Business question

How do admissions, length of stay, billing, and test-result labels vary across the supplied practice records?

## Dashboard preview

![Healthcare Admissions and Billing Analysis overview](images/healthcare-overview.png)

[Explore all dashboard views and version notes →](docs/dashboard-gallery.md)

## Key findings

| Notebook-reported observation | Result |
| --- | ---: |
| Records | 55,500 |
| Variables | 15 |
| Average length of stay | Approximately 15.5 days |
| Average billing | Approximately $25,500 |
| Random Forest accuracy | 41.69% |

The classification result requires comparison with a baseline, class distribution, and validation design before judging model usefulness.

## Decision use

1. Use admission and billing summaries to define questions for further investigation.
2. Assess classification performance against suitable baselines and validation checks.
3. Confirm dataset representativeness before applying findings to operational decisions.

These recommendations identify next steps; they do not represent measured business impact.

## Approach

Explore admission types and conditions, length of stay, billing by condition and insurer, and medication versus test-result labels. Treat the Random Forest exercise separately from descriptive findings and assess its validation design.

## Explore the project

| Resource | Purpose |
| --- | --- |
| [Python notebook](healthcare_analysis.ipynb) | Python notebook |
| [Practice dataset](healthcare_dataset.csv) | Practice dataset |
| [Dashboard gallery](docs/dashboard-gallery.md) | Full-size views and version context |
| [Analytical notes](docs/analytical-notes.md) | Methodology, metric definitions, and limitations |

## Scope and limitations

This is a public practice dataset, not verified hospital operational data. Category balance limits real-world interpretation. Associations do not establish treatment effects, and the classifier is not established as clinically useful.

---

[Portfolio](https://mikkymo.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/ogochukwuemeka/)
