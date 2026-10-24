# Pan-Cancer Tumour-Type Classifier from Tissue Genomics

This notebook predicts tumour site (24 classes) from somatic mutation and copy-number alteration (CNA) profiles.

## What's in the notebook

- **Data preparation:** complete-case selection across modalities, a 1% gene-frequency filter, and transformations.
- **Fusion strategies compared:** early-fusion MLP, modular (intermediate-fusion) MLP, and dimensionality reduction followed by an MLP. The reduction methods are PCA, factor analysis, an autoencoder, a VAE and MOFA+. Models are built in PyTorch.
- **Evaluation:** balanced accuracy, per-class precision, recall, F1 and AUROC, and normalised confusion matrices.
- **Interpretability:** Integrated Gradients, SHAP and LIME, with a cascade-randomisation sanity check (Adebayo et al., 2018).
- **Calibration:** per-class reliability diagrams and post-hoc temperature scaling.

Outputs are kept in the notebook so results can be read without re-running.

## Data

China Pan-Cancer (OrigiMed, 2020), publicly available from [cBioPortal](https://www.cbioportal.org/). Download the study files and set `DATA_DIR` in the setup cell.

## Tools

Python: PyTorch, scikit-learn, pandas, SHAP, LIME, matplotlib, seaborn.

## Context

Developed during my MPhil in Population Health Sciences (Health Data Science) at the University of Cambridge, 2025–26.

**Author:** Samuel Tekle Mengistu · [GitHub](https://github.com/teklesam) · [ORCID](https://orcid.org/0000-0002-2817-1421)
