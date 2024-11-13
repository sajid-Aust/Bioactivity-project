# Bioactivity Prediction on ABL1 Receptor Using BioT5 Model

## Project Overview

This project aims to predict the bioactivity of compounds against the ABL1 receptor (Tyrosine-protein kinase ABL1), a target associated with mutations linked to cancers, especially leukemia. Using molecular descriptors extracted from SMILES (Simplified Molecular Input Line Entry System) representations, we fine-tune a pre-trained `BioT5` model for bioactivity classification.

## Dataset

The dataset, sourced from ChEMBL, includes:

- **SMILES**: String notation for molecular structure.
- **Bioactivity Class**: Label indicating if the compound is active or inactive against the ABL1 receptor.

To enhance the dataset, **PaDEL** software was used to extract additional molecular descriptors from the SMILES representations. These descriptors include:

- **Molecular Weight (MW)**: Weight of the molecule.
- **LogP**: Partition coefficient, indicating lipophilicity.
- **Number of Hydrogen Donors** and **Acceptors**: Counts of hydrogen donors and acceptors in the molecule.

These descriptors are used as input features for the model, along with SMILES data, to improve bioactivity prediction accuracy.

## Code Workflow

1. **Preprocessing**: Scaling molecular descriptors and encoding labels for classification.
2. **Handling Class Imbalance**: Using SMOTENC to oversample the minority class.
3. **Model Fine-tuning**: Training the `BioT5` model on processed data, using descriptors and SMILES for input.
4. **Evaluation**: Classifying compounds as active or inactive and evaluating the model’s performance.
