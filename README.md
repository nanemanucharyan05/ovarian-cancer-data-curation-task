Video Link: https://drive.google.com/file/d/1FO5HbVxH7HRohePjdVYe1vRV1uf9YSd7/view?usp=sharing
# Ovarian Cancer Data Curation Task

This repository contains a curated, integrated dataset combining clinical and imaging
metadata for high-grade serous ovarian cancer (HGSOC) patients.

The project demonstrates best practices in:
- data ingestion and cleaning
- exploratory analysis and visualization
- dataset integration and linkage
- schema and metadata documentation

---

## Datasets Used

1. **HGSOC TCGA GDC Clinical Dataset**
   - Source: cBioPortal / GDC
   - Modality: Clinical / Genomics
   - Patients: 588
   - Access: Open

2. **TCGA-OV Imaging Metadata**
   - Source: The Cancer Imaging Archive (TCIA)
   - Modality: CT/MRI imaging metadata
   - Patients: 143
   - License: CC BY 3.0

---

## Repository Structure

- `notebooks/` – step-by-step notebooks for loading, analysis, and integration
- `data/raw/` – raw data 
- `data/processed/` – final cleaned and integrated datasets
- `schema.json` – column-level schema and provenance
- `metadata.json` – dataset-level metadata and processing notes
- `reports/linkage_report.md` – patient linkage logic and match rate

---

## Workflow

1. Load and audit raw datasets
2. Perform exploratory analysis and visualization
3. Clean and standardize identifiers
4. Integrate datasets at the patient level
5. Export final dataset, schema, and metadata

---

## Output

- `data/processed/ovarian_universal.csv`  
  Unified patient-level dataset containing clinical and imaging metadata.

---

## Reproducibility

Install dependencies using:

```bash
pip install -r requirements.txt
