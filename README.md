# QSAR Tutorial for Beginners

This repository contains a beginner-friendly tutorial for learning **Quantitative Structure–Activity Relationship (QSAR)** modeling. It is designed for undergraduate summer research students or new researchers who have little or no background in QSAR, cheminformatics, or machine learning.

The tutorial includes a written PDF/manual and a set of Jupyter notebooks. The PDF/manual explains the concepts, while the notebooks provide hands-on Python examples that students can run and modify.

## How to Use This Tutorial

For the best learning experience, students should follow this workflow:

1. **Read the corresponding chapter in the PDF/manual first.**  
   The manual explains the background, terminology, and purpose of each step.

2. **Open the matching chapter folder.**  
   Each folder contains a Jupyter notebook related to that chapter.

3. **Run the notebook step by step.**  
   Try to understand what each code cell is doing before moving to the next one.

4. **Modify the examples.**  
   Change SMILES strings, descriptor lists, models, or plotting options to see how the results change.

5. **Use the notebooks as practice material.**  
   The goal is not only to run the code, but to understand how each part of a QSAR workflow works.

## What Students Will Learn

By completing this tutorial, students should be able to:

- understand the basic idea of QSAR modeling,
- work with molecular structures using SMILES strings,
- use RDKit to visualize molecules and calculate descriptors,
- understand molecular descriptors and fingerprints,
- clean QSAR datasets before modeling,
- split data into training and test sets,
- train simple regression and classification models,
- evaluate models using common statistical metrics,
- understand internal and external validation,
- define and interpret applicability domain,
- explain QSAR models using feature importance, SHAP, and ALE-style interpretation.

## Recommended Setup

Create a new Python environment before running the notebooks.

```bash
conda create -n qsar_tutorial python=3.10
conda activate qsar_tutorial
conda install -c conda-forge rdkit pandas numpy matplotlib scikit-learn jupyterlab shap umap-learn ipywidgets ipympl
```

Then start JupyterLab:

```bash
jupyter lab
```

If you are using Google Colab, most notebooks should run after installing the required packages. However, some interactive plotting examples may behave differently in Colab than in local JupyterLab.

## Folder Structure

- `data/`: shared example QSAR dataset
- `00_how_to_use/`: environment and data check
- `01_what_is_qsar/`: introduction to QSAR and dataset exploration
- `02_statistics_metrics/`: mean, variance, standard deviation, MAE, RMSE, and R²
- `03_basic_chemistry_for_qsar/`: SMILES notation and RDKit visualization
- `04_molecular_descriptors_and_fingerprints/`: RDKit descriptors and Morgan fingerprints
- `05_data_cleaning_and_preprocessing/`: invalid SMILES removal, descriptor filtering, and train/test splitting
- `06_machine_learning_basics_for_qsar/`: regression, classification, overfitting, and feature selection
- `07_internal_and_external_validation/`: k-fold cross-validation, leave-one-out cross-validation, and external validation
- `08_applicability_domain/`: Williams plot and similarity-based applicability domain
- `09_interpreting_and_explaining_a_qsar_model/`: feature importance, SHAP, and ALE-style interpretation
- `10_example_dataset_template/`: example dataset format
- `11_suggested_student_report_template/`: student report template
- `12_useful_resources/`: package checks and useful links

## Suggested Learning Path

Students should go through the material in order:

1. Read the PDF/manual chapter.
2. Run the corresponding notebook.
3. Complete the exercises or modify the code.
4. Move to the next chapter.

This order is recommended because later chapters build on concepts from earlier chapters. For example, model validation and interpretation are easier to understand after learning about descriptors, preprocessing, and basic machine learning.

## Notes for Instructors

This tutorial can be used as a self-paced training resource or as part of a summer research onboarding plan. Instructors can assign one or two chapters per week depending on the student’s programming background.

A suggested six-week structure is:

| Week | Topics |
|---|---|
| Week 1 | QSAR overview, SMILES, RDKit, and basic statistics |
| Week 2 | Molecular descriptors and fingerprints |
| Week 3 | Data cleaning, preprocessing, and train/test splitting |
| Week 4 | Machine learning models and validation |
| Week 5 | Applicability domain and model interpretation |
| Week 6 | Final mini-project and student presentation |

## Final Goal

At the end of the tutorial, students should be able to complete a small QSAR project, including:

- loading and cleaning a molecular dataset,
- calculating descriptors or fingerprints,
- training a machine-learning model,
- evaluating model performance,
- checking applicability domain,
- interpreting important descriptors,
- presenting the results clearly.
