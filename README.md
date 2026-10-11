# Car-Fuel-Classification
Analisis dan Klasifikasi Jenis Bahan Bakar Mobil Berdasarkan Performa Mesin Tahun 2025 menggunakan Algoritma Random Forest.
# 🚗 Analisis dan Klasifikasi Jenis Bahan Bakar Mobil Berdasarkan Performa Mesin Tahun 2025

Proyek ini bertujuan untuk menganalisis dan mengklasifikasikan jenis bahan bakar kendaraan (*Fuel Types*) berdasarkan spesifikasi teknis dan performa mesin menggunakan dataset **Cars Datasets 2025**.

---

## 📌 Deskripsi Proyek
Dengan perkembangan teknologi otomotif di tahun 2025, beragam jenis bahan bakar dan sistem penggerak (seperti Petrol, Diesel, Hybrid, Electric, dan Plug-in Hybrid) hadir dengan karakteristik mesin yang berbeda-beda. Proyek *Machine Learning* ini menggunakan algoritma **Random Forest Classifier** untuk memprediksi kategori bahan bakar mobil berdasarkan atribut teknikal seperti kapasitas mesin, tenaga kuda (*HorsePower*), kecepatan maksimum (*Top Speed*), akselerasi, torsi, dan jumlah kursi.

---

## 🛠️ Alur Kerja (Workflow)
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

## 🧰 Pustaka & Teknologi yang Digunakan
- **Bahasa:** Python
- **Pustaka Analisis Data:** `pandas`, `numpy`
- **Pustaka Visualisasi:** `matplotlib`, `seaborn`
- **Pustaka Machine Learning:** `scikit-learn` (`RandomForestClassifier`, `Pipeline`, `ColumnTransformer`, `StandardScaler`, `OneHotEncoder`)

---

## 🚀 Cara Menjalankan Proyek
1. *Clone* repositori ini atau unduh file notebook `.ipynb`.
2. Jalankan di lingkungan **Google Colab** atau **Jupyter Notebook**.
3. Pastikan file dataset `Cars Datasets 2025.csv` telah diunggah ke direktori kerja Anda.
