# Bioactivity Prediction on ABL1 Receptor Using BioT5 Model

## Project Overview

This project aims to predict the bioactivity of compounds against the ABL1 receptor (Tyrosine-protein kinase ABL1), a target associated with mutations linked to cancers, especially leukemia. Using molecular descriptors and SMILES (Simplified Molecular Input Line Entry System) representations, we fine-tune a pre-trained `BioT5` model for bioactivity classification.

## Dataset

The dataset, sourced from ChEMBL, includes the following features:

- **SMILES**: String notation for molecular structure.
- **Molecular Weight (MW)**: Weight of the molecule.
- **LogP**: Partition coefficient, indicating lipophilicity.
- **Number of Hydrogen Donors** and **Acceptors**: Counts of hydrogen donors and acceptors in the molecule.
- **Bioactivity Class**: Label indicating if the compound is active or inactive against the ABL1 receptor.

These molecules are processed for model input to predict their binding capability with the ABL1 receptor.

## Code Workflow

1. **Preprocessing**: Scaling molecular descriptors and encoding labels for classification.
2. **Handling Class Imbalance**: Using SMOTENC to oversample the minority class.
3. **Model Fine-tuning**: Training the `BioT5` model on processed data, using descriptors and SMILES for input.
4. **Evaluation**: Classifying compounds as active or inactive and evaluating the model’s performance.

## Installation

Install the required packages with:

```bash
pip install -r requirements.txt
