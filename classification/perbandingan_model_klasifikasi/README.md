# Perbandingan Model Klasifikasi

## Overview
Proyek ini bertujuan untuk mengklasifikasikan apakah air layak minum menggunakan beberapa model machine learning. Dataset berisi data kualitas air dan label potabilitas (layak atau tidak).

## Dataset
- Total data: 3,276 sampel
- Fitur (9): ph, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic_carbon, Trihalomethanes, Turbidity
- Target: Potability (0 = Tidak Layak, 1 = Layak)

Beberapa fitur memiliki nilai hilang, misalnya ph (491 missing), Sulfate (781 missing), Trihalomethanes (162 missing).

## Data Preprocessing
Nilai yang hilang diisi menggunakan KNN Imputer dengan 3 tetangga.

## Model yang Digunakan
1. **Logistic Regression**  
   Jaccard Score: 0.314

2. **Decision Tree**  
   - Criterion: Entropy  
   - Max depth: 4  
   - Accuracy: 0.632  
   - Jaccard Score: 0.341  
   - Visualisasi decision tree dibuat

3. **Support Vector Machine (SVM)**  
   - Kernel: RBF  
   - Jaccard Score: 0.311  
   - Visualisasi confusion matrix dibuat

4. **K-Nearest Neighbors (KNN)**  
   - K optimal: 2  
   - Accuracy: 0.588  
   - Jaccard Score: 0.332  
   - Grafik akurasi vs k dibuat

## Perbandingan Model (Jaccard Score)
| Model              | Skor   |
|--------------------|--------|
| Logistic Regression | 0.314  |
| Decision Tree      | 0.341  |
| SVM                | 0.311  |
| KNN                | 0.332  |

Model Decision Tree memberikan performa terbaik.

## Requirements
- Python 3.10+
- Libraries: numpy, pandas, matplotlib, seaborn, scikit-learn

## Cara Menjalankan
1. Install library yang dibutuhkan  
2. Download dataset dari Kaggle (Water Potability Dataset)  
3. Update path dataset pada kode  
4. Jalankan notebook atau script Python

## Output
- Dataset setelah imputasi  
- Evaluasi model  
- Visualisasi decision tree  
- Confusion matrix SVM  
- Grafik akurasi KNN

## Kesimpulan
Decision Tree merupakan model terbaik untuk klasifikasi potabilitas air pada proyek ini.  
Pengembangan selanjutnya bisa meliputi feature engineering, tuning hyperparameter, dan eksplorasi model yang lebih kompleks.

## Author
[Dwiki Febrian]
