# XAI_Enhanced_Ensemble_Model_for_Infectious_Disease_Prediction_and_Visualization.ipynb
BERT/XLNet/RoBERTa models with majority-vote + weighted-avg ensembling, plus explainability (SHAP/LIME) and visual analytics for genomic-derived protein classification. Based on our IEEE BIBE 2023 paper


---

```
# XAI-Enhanced Ensemble Model for Infectious Disease Prediction

This repository contains the implementation of an **Explainable AI (XAI)–enhanced ensemble Transformer framework** for predicting infectious diseases from **translated protein sequences** derived from genomic data.

The project combines multiple Transformer models (BERT, XLNet, and RoBERTa) with ensemble learning and explainability techniques to improve prediction accuracy while maintaining interpretability.

This work is based on our IEEE BIBE 2023 publication.

---

## Project Overview

- **Task:** Infectious disease classification from genomic data  
- **Input:** DNA/RNA sequences → translated to protein sequences  
- **Models:** BERT, XLNet, RoBERTa  
- **Ensemble Methods:**  
  - Majority Voting  
  - Weighted Averaging  
- **Explainability:** SHAP / LIME-style interpretation  
- **Evaluation:** Accuracy, precision, recall, F1-score, confusion matrix  

The ensemble approach improves robustness and generalization compared to individual Transformer models.

---

## Repository Contents

- `XAI_Enhanced_Ensemble_Model_for_Infectious_Disease_Prediction_and_Visualization.ipynb`  
  End-to-end notebook including:
  - Data loading and preprocessing
  - Sequence translation (genomic → protein)
  - Model training and evaluation
  - Ensemble prediction
  - Explainability and visualization

- `Exhibit 3.2.pdf`  
  Supporting documentation / paper excerpt.

---

## Dataset Structure

The notebook expects genomic sequence files organized by class:

```

Genomic Sequences/
├── Ebola/
├── Influenza_A/
├── Influenza_B/
├── SARCoV2/
├── Tuberculosis/
├── Zika/
└── Normal_Genome/

````

Each subfolder represents a **class label**, and contains sequence files (`.fasta`, `.fna`, `.txt`, etc.).

---

## Methodology

### 1. Preprocessing
- Load genomic sequences
- Remove ambiguous bases
- Transcribe DNA → RNA
- Translate RNA → protein sequences

### 2. Modeling
- Fine-tune pretrained Transformer models:
  - BERT
  - XLNet
  - RoBERTa
- Train models independently on protein sequence representations

### 3. Ensemble Learning
- Combine predictions using:
  - **Majority voting**
  - **Weighted averaging** based on model performance

### 4. Explainability & Visualization
- Model interpretability using SHAP/LIME-inspired methods
- Performance visualization (confusion matrices, metrics plots)

---

## Installation

Create a virtual environment and install dependencies:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
pip install torch transformers
pip install biopython
pip install shap lime
````

> GPU-enabled PyTorch is recommended for faster training.

---

## Running the Code

1. Place your dataset in the expected folder structure.
2. Open the notebook:

```bash
jupyter notebook
```

3. Run all cells sequentially.

---

## Results Summary

* Individual Transformer models achieve strong classification performance.
* Ensemble methods further improve accuracy and stability.
* Explainability tools provide insight into sequence features influencing predictions.

---

## Citation

If you use this work, please cite:

**Ensemble and Transformer Models for Infectious Disease Prediction**
IEEE International Conference on Bioinformatics and Bioengineering (BIBE), 2023
DOI: 10.1109/BIBE60311.2023.00068

---

## License

This project is intended for **research and educational purposes**.

---

## Author

Blessing Adeika

```

```
