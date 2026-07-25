# Group09_FACED_ML

[![Course](https://img.shields.io/badge/Course-CSE521%2FAIML508-blue)](#)
[![Dataset](https://img.shields.io/badge/Dataset-FACED-orange)](https://doi.org/10.7303/syn50614194)
[![Track](https://img.shields.io/badge/Track-Graph%20Neural%20Network-green)](#)
[![Status](https://img.shields.io/badge/Status-Task%201%20Completed-brightgreen)](#)
[![License](https://img.shields.io/badge/License-GPL--3.0-lightgrey)](LICENSE)

## Project Overview

This repository contains the implementation, reports, related work, and model artifacts for the **Group 09 course project** in **CSE521/AIML508: Machine Learning, Summer 2026**.

The project uses the **Finer-grained Affective Computing EEG Dataset (FACED)** to investigate EEG-based emotion recognition using classical machine-learning baselines and graph neural networks.

The work is organized into four stages:

1. Dataset exploration, related-work analysis, and research-gap identification  
2. Baseline-model development, graph construction, and proposed GNN design  
3. Model improvement, ablation, cross-validation, statistical testing, and explainability  
4. Preparation of the final IEEE journal-format report  

---

## Project Information

| Item | Description |
|---|---|
| **Group** | Group 09 |
| **Dataset** | Finer-grained Affective Computing EEG Dataset |
| **Dataset Abbreviation** | FACED |
| **Application Area** | EEG-based emotion recognition |
| **Track** | Track 1 — Graph Neural Network on Table-Style EEG Data |
| **Problem Type** | Multiclass emotion classification |
| **Course** | CSE521/AIML508 — Machine Learning |
| **Semester** | Summer 2026 |
| **Institution** | East West University |
| **Repository** | [Group09_FACED_ML](https://github.com/NushratJabenAurnima/Group09_FACED_ML) |

---

## FACED Dataset

This project uses the **Finer-grained Affective Computing EEG Dataset (FACED)** for EEG-based emotion recognition.

FACED contains EEG recordings from **123 participants**, collected using **32 EEG channels** while participants watched **28 emotion-elicitation video clips** representing **nine emotion categories**.

The dataset provides raw EEG recordings, preprocessed EEG signals, self-reported emotional ratings, and extracted features such as Differential Entropy and Power Spectral Density.

### Dataset Summary

- **123 participants**
- **32 EEG channels**
- **28 emotion-elicitation video clips**
- **9 emotion categories**
- Raw EEG recordings
- Preprocessed EEG signals
- Differential Entropy features
- Power Spectral Density features
- Self-reported emotional ratings

### Emotion Categories

| Emotion Group | Categories |
|---|---|
| **Positive** | Amusement, Inspiration, Joy, Tenderness |
| **Negative** | Anger, Disgust, Fear, Sadness |
| **Neutral** | Neutral |

### Official Sources

- **Official Dataset Repository:** [FACED on Synapse](https://www.synapse.org/Synapse:syn50614194)
- **Dataset DOI:** [10.7303/syn50614194](https://doi.org/10.7303/syn50614194)
- **Original Dataset Paper:** [A Large Finer-grained Affective Computing EEG Dataset](https://www.nature.com/articles/s41597-023-02650-w)

> The FACED dataset is not redistributed through this repository. Users must obtain it from the official source and follow its access and usage conditions.

---

## Research Objective

The primary objective of this project is to develop a leakage-free and interpretable framework for EEG-based emotion recognition using the FACED dataset.

The project aims to:

1. Explore the structure, quality, and statistical properties of the FACED EEG features.
2. Establish classical machine-learning and neural-network baselines.
3. Construct a meaningful EEG graph using channels as nodes and justified relationships as edges.
4. Develop a graph neural network for multiclass emotion classification.
5. Evaluate whether graph-based modeling improves performance over non-graph baselines.
6. Measure model stability using subject-grouped cross-validation.
7. Interpret model decisions using explainable-AI techniques.
8. Compare the final model fairly with relevant published studies.

---

## Project Status

| Task | Description | Status |
|---|---|---|
| **Task 1** | Exploratory Data Analysis, Related Work, and Research-Gap Identification | ✅ Completed |
| **Task 2** | Baseline Models, Graph Construction, and Proposed GNN | ⏳ Not Started |
| **Task 3** | Model Improvement, Ablation, Cross-Validation, Significance Testing, and XAI | ⏳ Not Started |
| **Task 4** | Final IEEE Journal-Format Report | ⏳ Pending |

---

## Repository Structure

```text
Group09_FACED_ML/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── code/
│   ├── task1/
│   │   └── Group09_FACED_task1_eda.ipynb
│   ├── task2/
│   │   ├── Group09_FACED_task2_baselines.ipynb
│   │   └── Group09_FACED_task2_proposed_model.ipynb
│   └── task3/
│       ├── Group09_FACED_task3_improvement_ablation.ipynb
│       └── Group09_FACED_task3_explainability.ipynb
│
├── report/
│   ├── task1/
│   │   └── Group09_FACED_task1_report.pdf
│   ├── task2/
│   │   └── Group09_FACED_task2_report.pdf
│   ├── task3/
│   │   └── Group09_FACED_task3_report.pdf
│   └── task4/
│       └── Group09_FACED_final_report.pdf
│
├── related_work/
│   ├── README.md
│   ├── Group09_FACED_related_work_table.pdf
│   └── papers/
│
└── models/
    ├── Group09_FACED_best_model.*
    └── supporting_model_files/
```

> Files listed under Tasks 2–4 and the `models/` directory represent the planned final repository structure. They will be added after the corresponding work is completed.

---

## Task 1 — Dataset Understanding and Related Work

### Objectives

Task 1 focuses on understanding the FACED dataset, assessing its quality, and identifying a research gap that motivates the proposed graph-based approach.

### Completed Work

- Dataset-source and structure investigation
- Sample, subject, class, and feature analysis
- Descriptive statistical analysis
- Missing-value and duplicate analysis
- Class-distribution analysis
- Feature-distribution visualization
- Outlier and skewness investigation
- Correlation analysis
- Dimensionality-reduction visualization
- Review of relevant EEG emotion-recognition studies
- Identification of limitations and research gaps
- Motivation for graph-based EEG modeling

### Task 1 Files

| Deliverable | Location |
|---|---|
| **EDA Notebook** | `code/task1/Group09_FACED_task1_eda.ipynb` |
| **Task 1 Report** | `report/task1/Group09_FACED_task1_report.pdf` |
| **Related-Work Table** | `related_work/Group09_FACED_related_work_table.pdf` |
| **Reviewed Papers** | `related_work/papers/` |

---

## Task 2 — Baselines and Proposed GNN

### Planned Baseline Models

Representative baseline models may include:

- Logistic Regression
- Support Vector Machine
- k-Nearest Neighbors
- Decision Tree
- Random Forest
- Gradient Boosting or XGBoost
- Multilayer Perceptron
- One-dimensional Convolutional Neural Network

### Proposed Graph-Based Approach

The proposed graph neural network will define:

- **Nodes:** EEG channels or electrodes
- **Node features:** EEG-derived features such as Differential Entropy or Power Spectral Density
- **Edges:** Functional, statistical, spatial, or hybrid relationships between EEG channels
- **Edge weights:** Strength of the selected channel relationships
- **Readout:** Graph-level representation used for emotion classification

The graph-construction method will be justified experimentally rather than assumed to be beneficial.

---

## Task 3 — Improvement, Evaluation, and Explainability

Task 3 will focus on improving and validating the proposed model.

### Planned Work

- GNN architecture refinement
- Hyperparameter optimization
- Graph-construction comparison
- GCN, GAT, or GraphSAGE comparison
- Ablation study
- Subject-grouped five-fold cross-validation
- Mean and standard-deviation reporting
- Statistical significance testing
- Comparison with the strongest baseline
- Comparison with relevant published studies
- SHAP analysis
- LIME analysis
- Analysis of correctly and incorrectly classified samples

---

## Task 4 — Final Report

The final report will be written in **IEEE journal format** and will consolidate the findings from Tasks 1–3.

### Planned Sections

1. Abstract
2. Introduction
3. Related Work
4. Proposed Method
5. Experimental Setup
6. Results and Discussion
7. Conclusion
8. References

The final report will include:

- Dataset and preprocessing details
- Leakage-prevention safeguards
- Baseline-model results
- Proposed-model results
- Cross-validation mean and standard deviation
- Statistical significance test
- Ablation-study results
- Explainability findings
- Limitations and future work

---

## Contributors

### Nushrat Jaben Aurnima

- Project co-author
- GitHub: [@NushratJabenAurnima](https://github.com/NushratJabenAurnima)

### Shairin Akter Hashi

- Project co-author
- GitHub: [@Shairin207](https://github.com/Shairin207)

Both contributors participate in the research, implementation, analysis, documentation, and preparation of the final report.

---

## License

This repository is distributed under the terms of the [GNU General Public License v3.0](LICENSE).

The FACED dataset is governed by its own access and usage conditions and is not covered by this repository’s software license.

---

## Acknowledgement

We acknowledge the creators of the FACED dataset and the authors of the related studies used to support this project.
