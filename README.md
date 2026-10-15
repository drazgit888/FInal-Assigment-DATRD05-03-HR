# HR 1 — Employee Retention Support

## Project Overview

This project applies the CRISP-DM methodology to an HR business case involving employee retention.

The goal is to investigate whether employee data can support HR in identifying employees who may leave the company within the next six months. The intended use is to support voluntary, human-led retention reviews rather than make automatic personnel decisions.

The project connects data analysis and machine learning to a practical business decision. Model performance alone is not sufficient: the results must be interpreted in terms of their potential usefulness, limitations, and implications for HR.

## Business Context

- **Business problem:** Employee attrition within the next six months.
- **Main stakeholder:** HR team / HR managers.
- **Target variable:** `attrition_next_6m`.
- **Business key:** `employee_id`.
- **Prediction moment:** The employee survey date, while the employee is still working for the company.
- **Intended use:** Decision support for voluntary, human-led retention reviews.

Predictions must not automatically determine employment decisions. HR should review the available information, consider the individual context, and retain the ability to override model recommendations.

## Dataset

The project uses the allocated HR 1 dataset:

`group_08_hr_1.csv`

The dataset is loaded and analysed in the Jupyter Notebook. Its structure, target distribution, missing values, duplicates, variable distributions, and potential data-quality issues are examined during Data Understanding.

All numerical claims in the final analysis should be supported by visible notebook outputs. Dataset facts must be distinguished from business assumptions and analytical choices.

## CRISP-DM Structure

The notebook follows the six CRISP-DM phases:

1. **Business Understanding** — Define the business problem, stakeholder, decision, prediction moment, and measurable success criteria.
2. **Data Understanding** — Examine the observation unit, business key, target, data quality, distributions, patterns, and potential data leakage.
3. **Data Preparation** — Make and justify preparation decisions, including feature inclusion, exclusion, or engineering.
4. **Modelling** — Establish a baseline and develop at least one justified candidate model using an appropriate validation strategy.
5. **Evaluation** — Compare the candidate model with the baseline, interpret errors in business terms, inspect relevant subgroups, and make a defensible business recommendation.
6. **Deployment / Next Iteration** — Propose a workflow for human review, monitoring, feedback, and future improvement.

## Applying the Instructor's Feedback

The final analysis explicitly connects decisions across CRISP-DM phases.

For every important data-preparation decision, the notebook should show:

**We observed X → therefore we applied Y → after applying Y we found Z → this means…**

This structure ensures that preparation decisions are supported by evidence from Data Understanding and that their effects are verified rather than merely described.

The analysis should also explain how preparation choices affect the modelling process and the final business recommendation.

## Modelling and Evaluation Principles

The evaluation should not rely on accuracy alone, because a majority-class baseline may achieve high accuracy when attrition is relatively uncommon.

The notebook should compare the candidate model with the baseline and interpret appropriate metrics, including precision and recall. False positives and false negatives should be considered in relation to HR review capacity and the consequences of the two types of error.

Any assumptions about review capacity, acceptable performance, or business costs must be clearly labelled as assumptions unless supported by evidence.

A model should not be recommended for deployment solely because it produces a better technical score. The final recommendation must be justified by the available evidence.

## Responsible Use and Limitations

The proposed model is intended to support, not replace, human judgement.

The analysis should:

- Exclude information that would not be available at the prediction moment, particularly information recorded after an employee leaves.
- Consider potential differences in model performance across departments.
- Discuss limitations in the available data and business assumptions.
- Avoid treating associations as proof of causation.
- Include human review, privacy safeguards, monitoring, and a clear condition for pausing or stopping use of the model.

The final deployment recommendation may be to pilot, revise, collect additional data, return to an earlier CRISP-DM phase, or not deploy. The decision must follow from the evidence.

## Repository Structure

The repository contains:

- `README.md` — Project overview, methodology, and working principles.
- `group_08_hr_1.csv` — Source dataset.
- `HR_1_Final.ipynb` — Main notebook containing the CRISP-DM analysis.

## Reproducibility

Before submission:

1. Ensure the notebook can locate the source CSV.
2. Restart the kernel and run all cells from beginning to end.
3. Resolve execution errors.
4. Save the notebook with relevant outputs visible.
5. Check that numerical claims are supported by visible results.
6. Ensure the final notebook contains the complete analysis, interpretation, justification, and recommendation.

## Final Deliverable

The final deliverable is one completed Jupyter Notebook (`.ipynb`) containing the six CRISP-DM phases, supported by visible evidence and a defensible business recommendation.
