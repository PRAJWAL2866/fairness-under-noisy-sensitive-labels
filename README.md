# Fairness Under Noisy Sensitive Labels

**Project 22 | Group 2 | Team Rookies**

**Research Title:**  
Fairness under Noisy Sensitive Labels: Asymmetric Corruption of Recorded Sensitive Attributes and a Noise-Aware Model-Selection Safeguard

**GitHub Repository:**  
https://github.com/PRAJWAL2866/fairness-under-noisy-sensitive-labels

**Zenodo Archive:**  
https://doi.org/10.5281/zenodo.24090705

**Target Journal:** Data Mining and Knowledge Discovery (Springer Nature)

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

**RQ1:** How does asymmetric sensitive-attribute corruption affect the fairness–utility trade-off across fairness strategies?

**RQ2:** How does asymmetric corruption of validation sensitive labels influence fairness-based model selection and false-reassurance outcomes?

**RQ3:** Can a noise-aware model-selection safeguard reduce selection errors and improve the reliability of fairness-aware model selection?

**RQ4:** How do target-class imbalance and sensitive-attribute corruption interact when evaluating fairness and model-selection reliability?

**RQ5:** How well do the observed effects and the proposed safeguard generalize across different datasets?

## 4. Target Journal

- **Journal:** Data Mining and Knowledge Discovery
- **Publisher:** Springer Nature
- **Journal website:** https://link.springer.com/journal/10618

The research is being developed with this journal as its intended publication target. The experimental methodology, reproducibility, statistical evaluation and presentation of findings will be assessed against the expectations of the selected journal.

## 5. Anchor Research Paper

**Small et al. (2025)**

DOI: https://doi.org/10.1007/s10618-025-01112-8

This paper serves as the anchor reference for the research direction and motivates the investigation of fairness and robustness under sensitive-attribute label noise.

## 6. Datasets

Two benchmark datasets are used in this study.

### 6.1 Default of Credit Card Clients

- **Source:** UCI Machine Learning Repository
- **Dataset:** Default of Credit Card Clients
- **URL:** https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients
- **Sensitive attribute:** Sex
- **Purpose:** Investigate the effects of sensitive-attribute corruption on fairness evaluation and model selection.

### 6.2 Adult Dataset through Folktables

- **Source:** Folktables GitHub Repository
- **Repository:** https://github.com/socialfoundations/folktables
- **Description:** Standardized datasets and prediction tasks based on the American Community Survey (ACS).
- **Sensitive attribute:** Gender
- **Purpose:** Evaluate whether experimental findings generalize across datasets.

Dataset versions, access procedures, preprocessing and applicable usage or licensing conditions should be documented as part of the final experimental setup.

## 7. Research Methodology

The experimental methodology consists of the following stages.

### Step 1: Dataset Loading and Exploration

- Load the selected datasets.
- Inspect dataset structure, variables and data types.
- Identify missing values and inconsistent records.
- Examine target and sensitive-attribute distributions.

### Step 2: Data Preprocessing

- Handle missing values.
- Encode categorical variables.
- Prepare feature variables, target labels and sensitive attributes.
- Establish training, validation and test splits.

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

Different corruption rates are evaluated to understand their effects on fairness measurements and model selection.

### Step 6: Noise-Aware Model Selection

Evaluate how corrupted validation sensitive labels influence fairness-based model selection.

The proposed safeguard is investigated to reduce unreliable selection decisions and false-reassurance outcomes.

### Step 7: Evaluation and Robustness Analysis

- Compare predictive performance and fairness metrics.
- Measure model-selection reliability.
- Perform sensitivity and robustness analyses.
- Compare results across different datasets.
- Repeat experiments using multiple random seeds.

**Experimental protocol:** Training and validation sensitive labels are corrupted independently. Test sensitive labels remain clean to provide a reference for evaluating the effects of corruption.

The research design distinguishes pilot experimentation from the planned final experimental study. The number of seeds, dataset sizes and experimental conditions used in each reported run are documented with the corresponding results.

## 8. Evaluation Metrics

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

## 9. Expected Research Contributions

The study is designed to produce research figures and tables addressing all five research questions.

The planned analyses include:

- Comparisons of fairness measurements under different sensitive-label corruption mechanisms.
- Analysis of asymmetric corruption and fairness–utility trade-offs.
- Evaluation of false-reassurance rates and model-selection errors.
- Comparison of model-selection strategies with and without the proposed safeguard.
- Analysis of interactions between target-class imbalance and sensitive-label corruption.
- Cross-dataset comparisons of fairness and predictive performance.

The expected contribution is an empirical investigation of how unreliable sensitive-attribute labels affect fairness-aware model selection, together with an evaluation of a noise-aware safeguard.

**Note:** Expected or illustrative values are not experimental findings. Final conclusions must be based on actual executed experiments and appropriate statistical analysis.

## 10. Repository Structure

```text
fairness-under-noisy-sensitive-labels/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── final-notebook 22.ipynb
│
├── results/
│   ├── Project22_results_pilot.zip
│   ├── figures/
│   └── tables/
│
├── proposal/
│   └── Project22_Final_Proposal.pdf
│
├── documentation/
│   └── target_journal.txt
│
├── .gitignore
└── README.md
```

*The structure above describes the intended submission layout. Ensure the corresponding files are uploaded before treating the repository as complete.*

## 11. Installation and Requirements

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

The dependency file should include the packages required by the final notebook implementation, including relevant versions of:

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

## 12. Running the Notebook

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
8. Open `final-notebook 22.ipynb`.
9. Execute the notebook cells sequentially.
10. Review the generated figures, tables, fairness metrics and experimental comparisons.

Use the experimental configuration documented with each run when reproducing the results. Pilot configurations and final-study configurations must not be treated as interchangeable.

## 13. Reproducibility

The following practices support reproducibility:

- Fixed random seeds for controlled experiments.
- Documented corruption mechanisms and corruption rates.
- Independent corruption of training and validation sensitive labels.
- Clean test sensitive labels for reference evaluation.
- Consistent evaluation metrics across comparable experiments.
- Recorded package versions and experimental configurations.
- Explicit documentation of dataset sizes, experimental conditions and completed runs.
- Exported experimental tables and figures.

The final research report should identify the exact configuration used to generate every reported result.

## 14. Project Deliverables and Publication Links

### GitHub Repository

Complete research repository and source documentation:

https://github.com/PRAJWAL2866/fairness-under-noisy-sensitive-labels

### Zenodo Archive

**Published release:** Project 22 – Research Submission  
**Version:** v1.0.0  
**Publication date:** November 9, 2026

**Permanent DOI:** 10.5281/zenodo.24090705

**DOI link:** https://doi.org/10.5281/zenodo.24090705

The Zenodo record provides a persistent reference to the archived GitHub release.

### Research Notebook

The executed notebook containing the research implementation, experimental workflow, analyses and outputs.

### Experimental Results

The ZIP archive containing exported experimental results, including result tables and figures.

### Research Proposal

The finalized research proposal defining the research problem, objectives, research questions and methodology.

### Target Journal Text File

`target_journal.txt`

Content:

Data Mining and Knowledge Discovery

## 15. Project Team

**Team Name:** Rookies

**Group Number:** 2

**Team Members:**

1. Prajwal Dattatray Phalke
2. Naveenkumar Pugazhendi

## 16. Research Discussion and Documentation

The research planning, methodology discussion and project development conversation can be accessed through the following shared ChatGPT link:

**[Open Project 22 – Research Discussion](https://chatgpt.com/share/6ae8e543-eccc-83ed-8c5f-23699041ea15)**

## 17. Project Status

This repository is dedicated to Project 22: Fairness under Noisy Sensitive Labels.

The GitHub repository has been created and a release has been archived on Zenodo under DOI `10.5281/zenodo.24090705`.

The executed notebook and exported results provide the basis for reviewing the experimental implementation. Before the work is described as publication-ready, the final experimental configuration, metadata, statistical analyses, methodological limitations and clean-kernel reproducibility must be verified.

The research findings and conclusions will be finalised based on the validated experimental results.

---

**Project 22 | Group 2 | Team Rookies**

*Fairness under Noisy Sensitive Labels*
