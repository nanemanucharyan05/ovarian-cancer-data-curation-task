# Linkage Report

**Date:** 2026-03-01  
**Prepared by:** Nane Manucharyan 

---

## 1. Overview

This report summarizes the integration of the **HGSOC TCGA GDC Clinical dataset** with the **TCGA-OV Imaging metadata** to create a universal patient-level dataset (`ovarian_universal.csv`).  

**Objective:** Enrich clinical data with imaging metadata for patients with both records.

---

## 2. Join Logic

- **Canonical key:** `patient_id_canonical` (standardized patient ID).  
- **Join type:** Inner join on `patient_id_canonical`.  
- **Shared fields:** Patient identifiers; other fields preserved from original datasets.  
- **Duplicates:** Removed before joining.  

---

## 3. Match Rate

- Clinical patients: 588  
- Imaging patients: 143  
- Matched patients: 138  
- Match rate: 96.5%
- Unmatched patients:  
  - 5 imaging patients had no clinical record  
  - 450 clinical patients had no imaging record  

---

## 4. Notes

- Only patients with both clinical and imaging records are included.  
- The resulting dataset contains **one row per patient**, enriched with imaging metadata where available.  
- Some imaging metadata fields may be incomplete or inconsistent.
