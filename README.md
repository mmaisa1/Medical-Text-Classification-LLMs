# Medical Text Classification using Large Language Models

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 🎯 Project Overview

Advanced NLP research project implementing state-of-the-art Large Language Models for medical text classification. This graduate-level research explores the application of BERT, BioBERT, and GPT variants for classifying medical documents into cancer and non-cancer categories.

## 🔬 Research Objectives

- Develop comprehensive medical text classification pipeline
- Compare traditional ML approaches with modern LLM techniques
- Implement few-shot learning for medical domain adaptation
- Achieve high accuracy on large-scale medical datasets (19,000+ documents)

## 🏗️ System Architecture

Data Preprocessing → Feature Engineering → Model Training → Evaluation
↓ ↓ ↓ ↓
TCGA/IMR Data → TF-IDF/Embeddings → BERT/BioBERT → Performance Metrics


## 📊 Datasets

- **TCGA Pathology Reports**: 9,500+ medical pathology records
- **Independent Medical Reviews (IMR)**: 19,000+ medical review documents
- **Data Sources**: Kaggle, medical institutions (anonymized)

## 🛠️ Technologies Used

**Languages & Frameworks:**
- Python 3.8+, Jupyter Notebooks
- scikit-learn, pandas, numpy

**Machine Learning:**
- Traditional: TF-IDF + Logistic Regression
- Advanced: BERT, BioBERT, GPT variants
- Techniques: SMOTE, Few-shot Learning

**Evaluation:**
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrices, ROC-AUC
- Cross-validation, Statistical Analysis

## 🚀 Key Results

- **87.32% Baseline Accuracy** with TF-IDF + Logistic Regression
- **Successful LLM Integration** with BERT fine-tuning
- **Comprehensive Data Processing** of 19,000+ medical documents
- **Multi-class Classification** with class balancing techniques

## 📁 Repository Structure

├── README.md # Project overview (this file)
├── requirements.txt # Python dependencies
├── notebooks/ # Jupyter notebooks
│ ├── main_implementation.ipynb # Primary code implementation
│ ├── data_analysis.ipynb # Data exploration & visualization
│ ├── dataset_exploration.ipynb # Initial dataset analysis
│ └── project_progress.ipynb # Development progress tracking
├── docs/ # Project documentation
│ ├── Project_Design_Document.pdf # System architecture & methodology
│ ├── Final_Progress_Report.pdf # Results & analysis
│ └── Project_Proposal.pdf # Initial objectives & scope
├── src/ # Python modules (future development)
└── assets/ # Images, diagrams, visualizations


## 🔧 Getting Started

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook
- GPU recommended for LLM training (optional)

### Installation
Clone the repository
git clone https://github.com/mmaisa1/Medical-Text-Classification-LLMs.git
cd Medical-Text-Classification-LLMs

Install dependencies
pip install -r requirements.txt

Launch Jupyter
jupyter notebook


### Usage
1. Start with `notebooks/data_analysis.ipynb` for dataset exploration
2. Run `notebooks/main_implementation.ipynb` for full pipeline
3. Check `docs/` folder for detailed methodology and results

## 📈 Performance Metrics

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|---------|----------|
| TF-IDF + LR | 87.32% | 85.1% | 88.7% | 86.8% |
| BERT Fine-tuned | *In Progress* | - | - | - |
| BioBERT | *In Progress* | - | - | - |

## 📚 Research Documentation

- [📋 Project Design Document](docs/Project_Design_Document.pdf) - System architecture and technical methodology
- [📊 Final Progress Report](docs/Final_Progress_Report.pdf) - Comprehensive results and analysis  
- [🎯 Project Proposal](docs/Project_Proposal.pdf) - Initial objectives and research scope

## 🔍 Key Features

- **End-to-end ML Pipeline**: From raw text to model deployment
- **Advanced Preprocessing**: Text cleaning, normalization, feature engineering
- **Class Balancing**: SMOTE implementation for imbalanced datasets
- **Model Comparison**: Traditional ML vs. Modern LLM approaches
- **Comprehensive Evaluation**: Multiple metrics and visualization

## 🎓 Academic Context

This project was developed as part of graduate coursework (CSC 590) at California State University Dominguez Hills, focusing on advanced AI/ML applications in healthcare domains.

## 👤 Author

**Medha Maisa**  
MS Computer Science Student | California State University Dominguez Hills  
[LinkedIn](https://linkedin.com/in/maisa-medha-4959651a3) | [Email](mailto:your-email@domain.com)

## 🤝 Contributing

This project is part of ongoing academic research. For questions or collaboration opportunities, please reach out via LinkedIn or email.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*🔬 This repository demonstrates graduate-level AI/ML research capabilities with real-world applications in healthcare NLP.*
