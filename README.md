# Beyond Detection: Bridging the Gap Between Nodule Detection and Lung Cancer Diagnosis in Virtual Imaging Trials (VITs)

[![DOI](https://img.shields.io/badge/DOI-10.13140/RG.2.2.26638.78402-blue)](https://doi.org/10.13140/RG.2.2.26638.78402)

**Author(s):** Fakrul Islam Tushar, Liesbeth Vancoillie, Dhrubajyoti Ghosh, Kyle J. Lafata, Joseph Y. Lo  
**Institution:** Center for Virtual Imaging Trials, Duke University  
**Contact:** tushar.ece@duke.edu  

---

## 📖 Overview

This project advances virtual imaging trials (VITs) by moving beyond nodule detection to address **lung cancer diagnosis** within simulated screening studies. Using data from multiple clinical and simulated datasets (DLCSD, NLST, LIDC-IDRI, VLST), we introduce a novel **statistical labeling** approach that generates probabilistic diagnostic labels (benign/malignant) for simulated nodules, bridging the gap between detection metrics and diagnostic endpoints.

---

## 🏆 Recognition

This study was presented at the  
[Virtual Imaging Trials Meeting 2024 (VITM24)](https://vitm.io/)  
and received the **Best Presentation Award**.

We are grateful for this recognition, which highlights the project’s innovative approach to connecting detection and diagnostic endpoints in virtual trials.



## 🚀 Key Features

✅ Virtual Lung Screening Trial (VLST)  
✅ Simulated CT nodules with diagnostic labels  
✅ Statistical labeling model based on nodule size  
✅ Evaluation on real-world clinical datasets  
✅ ROC analysis for patient-level detection and diagnosis  
✅ Framework for integrating additional imaging features (planned)

---

## 📂 Project Structure

## 📈 Results

We evaluated the performance of our statistical labeling framework across simulated and real-world datasets.

| **Dataset** | **Detection AUC (Nodule-Level)** | **Diagnosis AUC (Patient-Level)** |
|-------------|----------------------------------|-----------------------------------|
| VLST        | 0.89                             | 0.72                              |
| NLST        | 0.91                             | 0.75                              |
| DLCSD       | 0.88                             | 0.74                              |

**Key Findings:**
- The **detection system** (virtual reader) shows strong performance across datasets, achieving AUCs around 0.88–0.91.
- The **diagnosis performance**, based on statistical malignancy labeling, consistently lags behind detection, with AUCs in the 0.72–0.75 range.
- This performance gap mirrors trends in real-world clinical settings, where detection alone is insufficient for confident cancer diagnosis.
- Our statistical labeling approach, despite using only nodule size, aligns closely with reported clinical metrics, confirming its value as a baseline.

---

## ⚠️ Limitations

While promising, the current system has several known limitations:

- **Single-feature model:**  
  Diagnosis predictions are based solely on nodule size, ignoring key imaging features like:
  - sphericity
  - margin sharpness
  - lobulation
  - spiculation
  - internal texture

- **No demographic integration:**  
  Patient-level risk factors (age, smoking history, family history) are not yet incorporated, which limits the generalizability of predictions.

- **Simulated data constraints:**  
  While virtual trials offer control and reproducibility, they may not fully capture the biological variability and complexity seen in real patients.

- **No temporal modeling:**  
  Longitudinal (follow-up) scans are not yet used to assess progression, an important clinical factor for risk stratification.

---

## 🌟 Planned Improvements

We aim to address these limitations in future work by:
- Expanding the feature set beyond size to include advanced image-derived biomarkers.
- Fusing demographic and clinical data with imaging outputs for richer predictions.
- Integrating longitudinal datasets to simulate disease progression over time.
- Applying and testing the framework across additional cancer types and screening contexts.

