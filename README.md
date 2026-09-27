# ML-Based Protein-Ligand Interaction Analysis

A computational workflow for analyzing protein-ligand interactions using PDB structures, structural distance features, and machine learning.

## Project Overview

This project analyzes protein-ligand interactions from experimentally determined protein structures obtained from the Protein Data Bank (PDB).

The workflow identifies ligand-binding residues, calculates protein-ligand distances, generates structural interaction features, and applies a Random Forest classifier for close-contact classification.

## Workflow

PDB Structures → Ligand Identification → Nearby Residues → Distance Calculation → Feature Engineering → Random Forest → Feature Importance

## Key Features

- Download and parse PDB structures
- Identify protein-bound ligands
- Detect nearby interacting residues
- Calculate minimum protein-ligand distances
- Generate hydrophobic and charged residue features
- Simulate computational mutation-impact scores
- Train a Random Forest classifier
- Analyze feature importance
- Export interaction data to CSV

## PDB Structures

The analysis uses the following PDB structures:

- 1HSG
- 1M17
- 3ERT
- 1TQN

## Results

- Extracted 110 protein-ligand interaction records
- Identified 84 close contacts and 26 non-close contacts using a 4 Å distance threshold
- Distance was the dominant feature in the Random Forest feature-importance analysis

## Technologies

- Python
- Biopython
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Biotite

## Important Note

The close-contact classification target is defined using a 4 Å distance threshold, while distance is also included as an input feature. Therefore, the machine-learning result should be interpreted as a structural-contact classification demonstration rather than an independent prediction of binding affinity or experimental interaction strength.
