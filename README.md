# Car Fuel Analysis & Predictive Modeling

Repositori ini berisi proyek analisis data dan pemodelan Machine Learning yang berfokus pada karakteristik konsumsi bahan bakar kendaraan, evaluasi metrik performa model, serta perbandingan algoritma regresi dan klasifikasi terkini.

---

## 1. Evaluasi Performa Model (Metrik Regresi & Klasifikasi)

Dalam pengembangan model prediktif terkait performa kendaraan, pemahaman metrik evaluasi sangat krusial:
* **Koefisien Determinasi ($R^2$):** Nilai $R^2$ harus $\le 1$ dan idealnya mendekati angka **1** (misal 0.85 - 0.95). Nilai ini tidak pernah lebih dari 1, dan bisa bernilai negatif jika performa model sangat buruk.
* **MAE & MSE (Error Metrics):** Tidak harus di bawah angka 1, karena skalanya mengikuti data asli (misalnya liter/kilometer). Prinsip utamanya adalah **mendekati angka 0** untuk meminimalisir kesalahan prediksi.

---

## 2. Faktor Utama Pemilihan Model
Pemilihan algoritma disesuaikan dengan 3 aspek utama data:
1. **Jenis Data (*Data Type*):** Menangani variabel numerik kontinu, biner, maupun kategori fitur kendaraan.
2. **Ukuran Dataset (*Dataset Size*):** Optimalisasi algoritma untuk skala data kecil hingga menengah.
3. **Linearitas (*Linearity*):** Memetakan hubungan linear vs non-linear antara spesifikasi mesin mobil dan tingkat konsumsi bahan bakar.

---

## 3. Taksonomi Algoritma Terkait Proyek

| Algoritma | Karakteristik & Kegunaan | Skala Dataset | Peruntukan Utama |
| :--- | :--- | :--- | :--- |
| **Linear Regression** | Hubungan data berbentuk garis lurus. Sangat cepat dan mudah diinterpretasikan. | Kecil – Menengah | Baseline model untuk estimasi nilai kontinu dasar. |
| **Ridge & Lasso Regression** | Regresi linear dengan penalti regularisasi untuk mengatasi multikolinearitas fitur mesin. | Kecil – Menengah | Mencegah *overfitting* saat fitur prediktor sangat banyak. |
| **Random Forest / Ensemble** | Berbasis *decision tree* ganda. Handal menangani hubungan non-linear yang kompleks. | Menengah – Besar | Analisis data tabular otomotif yang tahan terhadap *outlier*. |
| **Gradient Boosting (XGBoost/CatBoost)** | Algoritma *boosting* sekuensial dengan akurasi tinggi. | Menengah – Besar | Kompetisi / pemodelan performa tingkat lanjut. |

---

## Referensi Literatur

1. **Rastogi, A. & Kumar, P. (2026).** *10 Regression & Classification Algorithms in Machine Learning: Which to Use*. ML Research Series.
2. **Ali, A., et al. (2025).** *Comparative Analysis of Machine Learning Algorithms in Vehicle Performance Datasets*. Journal of Intelligent Computing.
3. **Ginting, A. H., et al. (2025).** *Performance Evaluation of Linear Models vs. Tree-Based Ensembles*. Atlantis Press.
4. **Joseph, K. (2024).** *Mastering Regression and Classification Workflows: A Practical Guide*. Medium Data Science.

---


# Car-Fuel-Classification
Analisis dan Klasifikasi Jenis Bahan Bakar Mobil Berdasarkan Performa Mesin Tahun 2025 menggunakan Algoritma Random Forest.
# Analisis dan Klasifikasi Jenis Bahan Bakar Mobil Berdasarkan Performa Mesin Tahun 2025

Proyek ini bertujuan untuk menganalisis dan mengklasifikasikan jenis bahan bakar kendaraan (*Fuel Types*) berdasarkan spesifikasi teknis dan performa mesin menggunakan dataset **Cars Datasets 2025**.

---

## Deskripsi Proyek
Dengan perkembangan teknologi otomotif di tahun 2025, beragam jenis bahan bakar dan sistem penggerak (seperti Petrol, Diesel, Hybrid, Electric, dan Plug-in Hybrid) hadir dengan karakteristik mesin yang berbeda-beda. Proyek *Machine Learning* ini menggunakan algoritma **Random Forest Classifier** untuk memprediksi kategori bahan bakar mobil berdasarkan atribut teknikal seperti kapasitas mesin, tenaga kuda (*HorsePower*), kecepatan maksimum (*Top Speed*), akselerasi, torsi, dan jumlah kursi.

---

## Alur Kerja (Workflow)
1. **Data Cleaning & Preprocessing:**
   - Menghapus data duplikat dan merapikan spasi pada kolom teks.
   - Mengimputasi *missing values* pada data numerik dengan nilai *median*.
   - Menyederhanakan kategori *Fuel Types* menjadi kelompok utama yang homogen (`Fuel_Clean`).
2. **Feature Engineering:**
   - Ekstraksi data angka dari kolom spesifikasi bernilai teks (CC, HP, Top Speed, Akselerasi, dan Torsi).
3. **Pemodelan & Pipeline:**
   - Penskalaan fitur numerik menggunakan `StandardScaler`.
   - *Encoding* fitur kategorikal menggunakan `OneHotEncoder`.
   - Pelatihan model dengan algoritma `RandomForestClassifier`.
4. **Evaluasi Model:**
   - Pengukuran akurasi dan analisis performa menggunakan *Classification Report* serta *Confusion Matrix*.

---

## Pustaka & Teknologi yang Digunakan
- **Bahasa:** Python
- **Pustaka Analisis Data:** `pandas`, `numpy`
- **Pustaka Visualisasi:** `matplotlib`, `seaborn`
- **Pustaka Machine Learning:** `scikit-learn` (`RandomForestClassifier`, `Pipeline`, `ColumnTransformer`, `StandardScaler`, `OneHotEncoder`)

---

## Cara Menjalankan Proyek
1. *Clone* repositori ini atau unduh file notebook `.ipynb`.
2. Jalankan di lingkungan **Google Colab** atau **Jupyter Notebook**.
3. Pastikan file dataset `Cars Datasets 2025.csv` telah diunggah ke direktori kerja Anda.
