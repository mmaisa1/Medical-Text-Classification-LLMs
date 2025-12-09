# Cancer Type Prediction from Pathology Reports

**This repository contains a clean pipeline for predicting 32 specific cancer types (BRCA, KIRC, LUAD, etc.) from TCGA pathology reports.**

## 🎯 Aim
Determine if pathology report text contains discriminative patterns to identify specific cancer types with high accuracy.

## 🛤️ Plan of Action
1. **Classical ML Baseline**: TF-IDF → Logistic Regression/Random Forest
2. **LLM Evaluation**: Zero-shot, few-shot, fine-tuned biomedical LLMs
3. **Comparison**: Establish performance hierarchy

## 📊 Current Results
- **Logistic Regression**: 94.2% accuracy (32 classes)
- **5-Fold CV**: 93.1% ± 0.6%
- **Random Forest**: 93.2% (comparison baseline)

## 📈 Expected Outcomes
1. ✅ **94%+ ML baseline** (ACHIEVED)
2. **LLM superiority** (96-98% expected)
3. **Few-shot efficiency** demonstration

## 🗂️ Files
```
data/
├── TCGAReports.csv              # 9,523 pathology reports
└── tcga_patient_to_cancer_type.csv  # 32 cancer labels

TCGA_cancer_classification.ipynb  # Complete 94.2% pipeline
project_documenation.doc          # Research journey
```
