# Medical Text Classification Using LLMs (TCGA Pathology Reports)

A systematic evaluation of classical ML, supervised transformer, zero-shot, 
and few-shot approaches for 32-class cancer type classification from TCGA 
pathology reports.

## Overview

This project evaluates multiple model families on a long-document clinical 
text classification task, with a focus on feasibility-aware evaluation and 
leakage-safe experimental design.

## Results

### Full Test Set (N=1,905)
| Model | Accuracy | Macro-F1 | Weighted-F1 | Per Report (sec) |
|---|---|---|---|---|
| TF-IDF + LinearSVC | 96.6% | 95.0% | 96.5% | ~0.0003 |
| TF-IDF + LogReg | 95.4% | 94.0% | 95.4% | ~0.0007 |
| DistilBERT (fine-tuned) | 92.3% | 89.6% | 92.4% | ~0.4 |

### Subset Evaluation (N=300)
| Model | Accuracy | Macro-F1 | Weighted-F1 | Per Report (sec) |
|---|---|---|---|---|
| TF-IDF + LinearSVC | 95.3% | 93.6% | 95.0% | ~0.0003 |
| TF-IDF + LogReg | 95.0% | 94.2% | 95.1% | ~0.0007 |
| DistilBERT (fine-tuned) | 90.3% | 87.7% | 90.2% | ~0.4 |
| Hybrid Top-K + Chunked NLI | 81.7% | 77.0% | 81.0% | 2.38 |
| Full-Label Chunked NLI | 75.3% | 70.9% | 75.2% | 15.27 |
| Zero-Shot BART-MNLI (naive) | 67.7% | 61.0% | 68.1% | 5.49 |
| Few-Shot FLAN-T5 (3-shot) | 46.3% | 37.0% | 45.4% | 0.108 |

## Key Contributions

- Leakage-safe patient-disjoint train/test splitting with group-aware CV
- Hybrid Top-K candidate narrowing + chunked NLI reranking framework
- Feasibility analysis of LLM-based methods on long clinical documents
- Ablation study isolating Top-K narrowing contribution (+6.3% accuracy, 6.4x faster vs full-label chunked)
- Performance-efficiency tradeoff analysis across model families

## Setup

**Runtime:** Google Colab, Python 3.12, T4 GPU

**Install dependencies:**
```bash
pip install transformers datasets evaluate accelerate sentencepiece scikit-learn
```

## How to Run

1. Upload data files to Google Drive under a folder named 
   `Medical-Text-Classification-LLMs`
2. Open the notebook in Google Colab
3. Mount Drive and run all sections in order

## Data

| File | Description |
|---|---|
| TCGA_Reports.csv | 9,523 pathology reports |
| tcga_patient_to_cancer_type.csv | 32 cancer type labels |

Data sourced from The Cancer Genome Atlas (TCGA) via NIH GDC Portal.

## Files

```plaintext
Medical-Text-Classification-LLMs/
├── Medical-Text-Classification.ipynb
├── data/
└── results/
```
