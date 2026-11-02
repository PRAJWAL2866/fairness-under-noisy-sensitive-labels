# Fairness Under Noisy Sensitive Labels

Reproducible research on robust fair machine learning under asymmetric and group-dependent sensitive-attribute label noise.

## 1. Project Overview

This research investigates how inaccuracies in sensitive-attribute labels affect fairness evaluation and machine learning model selection.

In real-world machine learning applications, sensitive attributes such as gender may contain incorrect or inconsistent labels. Such inaccuracies can distort fairness measurements and lead to misleading conclusions about whether a model treats different demographic groups fairly.

The project aims to evaluate the impact of asymmetric and group-dependent sensitive-attribute label noise and investigate approaches for more reliable fairness-aware model selection.

## 2. Research Objectives

The main objectives are:

- Investigate how sensitive-attribute label noise affects machine learning fairness.
- Evaluate the impact of different noise rates and corruption patterns.
- Examine fairness and predictive utility trade-offs.
- Identify misleading fairness assessments caused by corrupted sensitive labels.
- Investigate noise-aware model selection strategies.
- Compare experimental findings across multiple datasets.

## 3. Research Questions

The study focuses on the following research questions:

1. How does asymmetric sensitive-attribute corruption affect the fairness–utility trade-off across fairness strategies?
2. Can corrupted validation sensitive labels cause model selection to prefer a model that appears fair but is unfair under clean reference labels?
3. Can a noise-aware selection safeguard improve worst-case clean-reference fairness subject to a utility threshold?
4. How do corruption direction and rate, group prevalence, and target imbalance interact with fairness outcomes?
5. Do the observed patterns generalize across the Adult Income and Default of Credit Card Clients datasets?

## 4. Datasets

The research uses two publicly available datasets.

### Adult Income Dataset

- Source: UCI Machine Learning Repository
- URL: https://archive.ics.uci.edu/dataset/2/adult
- Prediction task: Income classification
- Sensitive attribute: Sex

### Default of Credit Card Clients Dataset

- Source: UCI Machine Learning Repository
- URL: https://archive.ics.uci.edu/dataset/350/default+credit+card+clients
- Prediction task: Credit default prediction
- Sensitive attribute: Sex

Both datasets are used to evaluate the impact of sensitive-attribute label corruption across different prediction tasks.

## 5. Methodology

The planned methodology includes:

1. Dataset loading and exploratory inspection.
2. Data cleaning and preprocessing.
3. Definition of target and sensitive attributes.
4. Stratified training, validation, and test splitting.
5. Controlled asymmetric sensitive-label corruption.
6. Training baseline and fairness-aware machine learning models.
7. Evaluation under different corruption rates.
8. Comparison of fairness and predictive utility.
9. Investigation of model-selection disagreement.
10. Evaluation of a noise-aware model-selection safeguard.
11. Cross-dataset comparison and robustness analysis.

## 6. Experimental Setup

The initial experimental configuration includes:

| Parameter | Setting |
|---|---|
| Random state | 42 |
| Noise rates | 0%, 5%, 10%, 20%, 30% |
| Random seeds | 11, 23, 37 |
| Adult dataset sample limit | 18,000 |
| Credit dataset sample limit | 12,000 |
| Utility threshold | 0.55 |

These are preliminary experimental settings and may be adjusted during the research.

## 7. Machine Learning Models

The planned experiments include:

- Logistic Regression (baseline).
- Inverse-group-frequency reweighting.
- Exponentiated Gradient fairness constraints using Fairlearn, where supported.

## 8. Evaluation Metrics

### Predictive Performance

- Accuracy
- Balanced Accuracy

### Fairness Evaluation

- Demographic Parity Difference
- Equal Opportunity Difference
- Equalized Odds Difference

### Additional Analysis

- False-reassurance rate.
- Model-selection disagreement.
- Fairness degradation under different noise rates.
- Bootstrap confidence intervals.
- Cross-dataset robustness.

## 9. Expected Research Contributions

The research aims to:

- Demonstrate the effect of noisy sensitive attributes on fairness evaluation.
- Analyze the relationship between label corruption and fairness–utility trade-offs.
- Identify situations where corrupted validation labels produce misleading model-selection decisions.
- Investigate a noise-aware model-selection safeguard.
- Provide comparative evidence across two real-world datasets.

These are intended contributions and will be evaluated through experiments.

## 10. Dependencies

The project uses Python and the following libraries:

- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Fairlearn
- OpenPyXL
- xlrd
- Jupyter Notebook

Install dependencies using:

```bash
pip install -r requirements.txt
```

## 11. Dataset Access and Execution

1. Download the datasets from the official UCI Machine Learning Repository links.
2. Prepare the downloaded files according to the notebook's expected filenames.
3. Place the datasets in the existing raw-data location or configure the notebook paths accordingly.
4. Install the required dependencies.
5. Open the Jupyter Notebook.
6. Execute the notebook cells sequentially when conducting the actual experiments.

## 12. Reproducibility and Research Integrity

- Fixed random seeds are used for reproducibility.
- Original recorded sensitive attributes are preserved as experimental reference labels.
- Artificial corruption is introduced separately from the original labels.
- Final test evaluation uses clean reference labels.
- Experimental findings will only be reported after actual execution and validation.
- No fabricated results are included.
- Recorded sensitive attributes are treated as experimental reference labels rather than unquestionable ground truth.

## 13. Current Implementation Status

This repository contains the initial research implementation and supporting dataset resources.

The submitted initial implementation is intended to demonstrate the planned methodology and experimental feasibility.

The notebook is submitted without executed outputs, in accordance with the initial project proposal submission requirements.

## 14. Authors

**Project:** Fairness Under Noisy Sensitive Labels

**Team Members:**
- Prajwal Phalke
- [Second Team Member's Full Name]

**Module:** AI, Power & Responsibility: Governing Intelligence

**Institution:** University of Europe for Applied Sciences
