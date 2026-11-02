# Fairness Under Noisy Sensitive Labels

**Project 22 | Group 2 | Team Rookies**

**Research Title:** Fairness under Noisy Sensitive Labels: Asymmetric Corruption of Recorded Sensitive Attributes and a Noise-Aware Model-Selection Safeguard

**Repository:** [PRAJWAL2866/fairness-under-noisy-sensitive-labels](https://github.com/PRAJWAL2866/fairness-under-noisy-sensitive-labels)

---

## 1. Project Overview

This research investigates how inaccuracies in recorded sensitive attributes affect fairness evaluation and machine learning model selection.

In real-world machine learning applications, sensitive attributes such as gender and demographic group membership may contain incorrect or inconsistent labels. These inaccuracies can distort fairness measurements and lead to misleading conclusions about whether a model treats different demographic groups fairly.

The project focuses on asymmetric and group-dependent sensitive-attribute label corruption. It examines how different corruption mechanisms affect fairness measurements, predictive performance, and fairness-aware model selection.

The study also investigates a noise-aware model-selection safeguard designed to reduce the risk of selecting models that appear fair under corrupted validation labels but perform poorly when evaluated using clean reference labels.

## 2. Research Objectives

The main objectives are:

- Investigate how sensitive-attribute label noise affects machine learning fairness.
- Evaluate the impact of different noise rates and corruption patterns.
- Examine fairness and predictive utility trade-offs.
- Identify misleading fairness assessments caused by corrupted sensitive labels.
- Investigate noise-aware model-selection strategies.
- Compare experimental findings across multiple datasets.

## 3. Research Questions

The study focuses on five research questions:

**RQ1:** How does asymmetric sensitive-attribute corruption affect the fairness–utility trade-off across fairness strategies?

**RQ2:** How does asymmetric corruption of validation sensitive labels influence fairness-based model selection and false-reassurance outcomes?

**RQ3:** Can a noise-aware model-selection safeguard reduce selection errors and improve the reliability of fairness-aware model selection?

**RQ4:** How do target-class imbalance and sensitive-attribute corruption interact when evaluating fairness and model-selection reliability?

**RQ5:** How well do the observed effects and the proposed safeguard generalize across different datasets?

## 4. Datasets

Two benchmark datasets are used in this study.

### 4.1 Default of Credit Card Clients

- **Source:** UCI Machine Learning Repository
- **Dataset:** Default of Credit Card Clients
- **URL:** https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients
- **Description:** Contains information about credit card clients, including demographic characteristics, credit history, payment information, and default payment status.
- **Purpose:** Used to investigate the effects of sensitive-attribute corruption on fairness evaluation and model selection.

### 4.2 Adult Dataset through Folktables

- **Source:** Folktables GitHub Repository
- **Repository:** https://github.com/socialfoundations/folktables
- **Description:** Provides standardized datasets and prediction tasks based on the American Community Survey (ACS).
- **Purpose:** Used to evaluate whether the experimental findings generalize across datasets.

**Dataset preparation:** The datasets will be inspected, cleaned, preprocessed, and transformed into suitable feature, target, and sensitive-attribute representations. Dataset versions, access procedures, and applicable usage or licensing conditions should be documented as part of the final experimental setup.

## 5. Research Methodology

The experimental methodology consists of the following stages:

### Step 1: Dataset Loading and Exploration

- Load the selected datasets.
- Inspect dataset structure, variables, and data types.
- Identify missing values and inconsistent records.
- Examine target and sensitive-attribute distributions.

### Step 2: Data Preprocessing

- Handle missing values.
- Encode categorical variables.
- Prepare feature variables, target labels, and sensitive attributes.
- Establish training, validation, and test splits.

### Step 3: Baseline Model Training

Train baseline machine learning models, including Logistic Regression, to establish reference predictive performance.

### Step 4: Fairness-Aware Strategies

Compare different fairness approaches:

- Baseline classification.
- Reweighting.
- Fairlearn Exponentiated Gradient with Demographic Parity constraints.
- Fairlearn Exponentiated Gradient with Equalized Odds constraints.
- Threshold-based post-processing.

### Step 5: Sensitive-Attribute Corruption

Introduce controlled corruption into recorded sensitive attributes.

The study considers four corruption mechanisms:

1. **Symmetric corruption:** Both sensitive groups have equal corruption probabilities.
2. **Minority-to-majority corruption:** Sensitive labels from the minority group are changed to the majority group.
3. **Majority-to-minority corruption:** Sensitive labels from the majority group are changed to the minority group.
4. **Class-dependent corruption:** Corruption probabilities depend on the target class.

Different corruption rates will be evaluated to understand their effects on fairness measurements and model selection.

### Step 6: Noise-Aware Model Selection

Evaluate how corrupted validation sensitive labels influence fairness-based model selection.

The proposed safeguard will be investigated to reduce unreliable selection decisions and false-reassurance outcomes.

### Step 7: Evaluation and Robustness Analysis

- Compare predictive performance and fairness metrics.
- Measure model-selection reliability.
- Perform sensitivity and robustness analyses.
- Compare results across different datasets.
- Repeat experiments using multiple random seeds.

**Experimental protocol:** Training and validation sensitive labels are corrupted independently. Test sensitive labels remain clean to provide a reference for evaluating the effects of corruption.

The pilot experiments use three random seeds. The final experimental study is planned to use at least 20 random seeds.

## 6. Evaluation Metrics

The following metrics are used to evaluate predictive performance, fairness, and model-selection reliability.

### Predictive Performance

- Accuracy
- Balanced Accuracy

### Fairness Metrics

- Demographic Parity Difference
- Equal Opportunity Difference
- Equalized Odds Difference

### Model-Selection Reliability

- False-Reassurance Rate
- Oracle Disagreement
- Regret
- Robustness Ratio

These metrics help determine whether corrupted sensitive labels lead to misleading fairness assessments and whether the proposed safeguard improves model-selection reliability.

## 7. Expected Results and Research Contributions

The study is designed to produce publication-oriented figures and tables addressing all five research questions.

The planned analyses include:

- Comparisons of fairness measurements under different sensitive-label corruption mechanisms.
- Analysis of asymmetric corruption and fairness–utility trade-offs.
- Evaluation of false-reassurance rates and model-selection errors.
- Comparison of model-selection strategies with and without the proposed safeguard.
- Analysis of interactions between target-class imbalance and sensitive-label corruption.
- Cross-dataset comparisons of fairness and predictive performance.

The expected contribution is an empirical investigation of how unreliable sensitive-attribute labels affect fairness-aware model selection, together with an evaluation of a noise-aware safeguard.

**Note:** Expected or illustrative values are not experimental findings. Final conclusions will be based on actual executed experiments and statistical analysis.

## 8. Repository Structure

```text
fairness-under-noisy-sensitive-labels/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── Project22_Fairness_Noisy_Sensitive_Labels_Kaggle.ipynb
│
├── results/
│   ├── figures/
│   └── tables/
│
├── .gitignore
├── README.md
└── requirements.txt
```

### Directory Description

| Directory/File | Description |
|---|---|
| `data/raw/` | Original downloaded datasets |
| `data/processed/` | Cleaned and preprocessed datasets |
| `notebooks/` | Research implementation and experiments |
| `results/figures/` | Generated plots and visualizations |
| `results/tables/` | Experimental result tables |
| `.gitignore` | Files and directories excluded from Git |
| `requirements.txt` | Python dependencies |
| `README.md` | Project documentation |

The structure represents the intended organization of the research implementation. Directories can be added as the experiments progress.

## 9. Installation and Requirements

### Prerequisites

- Python 3.10 or later
- Jupyter Notebook or JupyterLab
- Git
- Internet connection for dataset retrieval

### Clone the Repository

```bash
git clone https://github.com/PRAJWAL2866/fairness-under-noisy-sensitive-labels.git

cd fairness-under-noisy-sensitive-labels
```

### Create a Virtual Environment

**Windows PowerShell:**

```powershell
python -m venv .venv

.venv\Scripts\Activate.ps1
```

**Linux/macOS:**

```bash
python -m venv .venv

source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

The dependency file should include the packages required by the final notebook implementation, including the relevant versions of:

- NumPy
- Pandas
- Scikit-learn
- Fairlearn
- SciPy
- Matplotlib
- Seaborn
- Jupyter
- Folktables, if used for dataset retrieval

The final `requirements.txt` should be checked against the notebook imports before running the experiments.

## 10. Running the Notebook

Follow these steps to execute the experiments:

1. Clone the GitHub repository.
2. Create and activate a Python virtual environment.
3. Install the required dependencies.
4. Download or retrieve the datasets from their official sources.
5. Configure the dataset paths in the notebook.
6. Start Jupyter Notebook:

```bash
jupyter notebook
```

7. Open the `notebooks/` directory.
8. Open `Project22_Fairness_Noisy_Sensitive_Labels_Kaggle.ipynb`.
9. Execute the notebook cells sequentially.
10. Review the generated figures, tables, fairness metrics, and experimental comparisons.

For the final study, use at least 20 random seeds. The three-seed configuration is intended for pilot experimentation only.

## 11. Reproducibility

The following practices will be used to support reproducibility:

- Fixed random seeds for controlled experiments.
- Documented corruption mechanisms and corruption rates.
- Independent corruption of training and validation sensitive labels.
- Clean test sensitive labels for reference evaluation.
- Consistent evaluation metrics across comparable experiments.
- Recorded package versions and experimental configurations.
- At least 20 random seeds for the final experimental study.

## 12. Project Team

**Team Name:** Rookies

**Group Number:** 2

**Team Members:**

1. Prajwal Dattatray Phalke
2. Naveenkumar Pugazhendhi

## 13. Research Discussion and Documentation

The research planning, methodology discussion, and project development conversation can be accessed through the following shared ChatGPT link:

**[Open Project 22 – Research Discussion](https://chatgpt.com/share/6ae8e543-eccc-83ed-8c5f-23699041ea15)**

## 14. Project Status

This repository is dedicated to Project 22: Fairness under Noisy Sensitive Labels.

It contains the research documentation and implementation framework for investigating fairness evaluation under asymmetric and group-dependent sensitive-attribute corruption.

The final results, figures, tables, and conclusions will be updated as the experiments are implemented and completed.

---

**Project 22 | Group 2 | Team Rookies**

*Fairness under Noisy Sensitive Labels*
