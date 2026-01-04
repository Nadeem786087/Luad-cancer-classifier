
# Machine Learning-Based Lung Cancer Classification Web Tool

**Team**:  
- Muhammad Anas (Developer - Frontend/Backend)  
- Muhammad Nadeem (ML & Bioinformatics)  
- Muhammad Hussnain (Documentation & Reporting)  

**Department**: Bioinformatics & Biotechnology, GCUF  
**Semester**: 7th | Session: 2022–2026

### Project Overview
A web-based tool for classifying lung adenocarcinoma (LUAD) samples as **Tumor** or **Normal** using TCGA-LUAD gene expression data and machine learning.

- **ML Model**: Random Forest (trained on top 2000 most variable genes)
- **Performance**: **100% accuracy** on held-out test set (576 samples: 515 tumor, 59 normal)
- **Features**: Upload CSV → prediction + confidence score + visualizations

### Files in Repo
- `/ml_artifacts/` folder:
  - `best_luad_model.pkl` → Trained model
  - `scaler.pkl` → Data scaler
  - `selected_genes.pkl` → List of 2000 genes (input must align)
  - `demo_tumor.csv` → Test sample (should predict Tumor)
  - `demo_normal.csv` → Test sample (should predict Normal)
- `notebook.ipynb` → Full ML workflow (data loading → training → results)

### How to Run (For Developer)
1. **Backend (FastAPI)**:
   - Place .pkl files in backend folder
   - Run `uvicorn main:app --reload`
   - Test `/predict` with demo CSVs

2. **Frontend (React)**:
   - Connect to backend
   - Add file upload + demo buttons

### Results Summary
- PCA: Complete separation of tumor vs normal
- Heatmap: Clear clustering
- Test Accuracy: 100%
- Confusion Matrix: No errors

**Status**: ML complete  | Web app in progress 
