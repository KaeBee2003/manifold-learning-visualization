# DA5401 - Assignment 5: Manifold Visualization

This repository contains my submission for **DA5401 A5: Visualizing Data Veracity Challenges in Multi-Label Classification**.  
The objective of this assignment was to explore **t-SNE** and **Isomap** for visualizing high-dimensional **multi-label classification data** (Yeast dataset) and to inspect potential **data veracity issues** such as noisy labels, outliers, and hard-to-learn samples.

---

##  Contents
- `Ass5.ipynb` – Jupyter Notebook with full code, visualizations, and analysis  
- `yeast.arff` – The Original Dataset used for this assignment
- `README.md` – This file  

---

##  Dataset
- Dataset: **Yeast gene expression data** (multi-label, 14 categories)  
- Features: 103 columns
- Labels: Multi-label functional categories (14 total)

---

## ⚠️ Notes & Discrepancies
- The assignment instructions asked for:
  - Two most frequent *single-label* classes and one *multi-label* combination  

- However, the dataset used had:
  - Only **one frequent single-label class** (`Class1`)  

To adapt, I used:
- **Top single-label class**: `Class1`  
- **Top 2 multi-label combinations**:  
  1. (`Class3`, `Class4`, `Class12`, `Class13`)  
  2. (`Class4`, `Class5`, `Class12`, `Class13`)  
- All others were grouped as **"Other"**  

This resulted in **4 categories** instead of what is given in instructions.

---

##  Methods
- **Preprocessing**: Standardization of features  
- **t-SNE**:
  - Explored perplexity values from **1 to 100**  
  - Visualized in 2D with categorical color mapping  
- **Isomap**:
  - Neighborhood values from **10 to 80**  
  - Compared global vs local structure preservation  

---

##  Results
- **Clusters were poorly separated** due to dataset limitations and adapted labeling scheme  
- **Silhouette scores** were negative across runs  
- Both **t-SNE and Isomap** visualizations highlighted overlapping and noisy labels, reflecting the **data veracity challenges** in this dataset  

---
