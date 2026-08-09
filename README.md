# 🚗 Car Price Prediction Project

Prediksi harga mobil menggunakan **Regresi Linear** yang diimplementasikan dari awal (*from scratch*) dengan NumPy.

## 🎯 Tujuan

Project ini bertujuan untuk membangun model prediksi harga mobil menggunakan algoritma regresi linear. Model ini membantu konsumen dan penjual dalam menentukan harga jual yang wajar berdasarkan berbagai faktor seperti merek, tahun, jarak tempuh, dan spesifikasi mobil lainnya.

## 📊 Dataset

Dataset yang digunakan adalah **[Car Features and MSRP](https://www.kaggle.com/datasets/CooperUnion/cardataset)** dari Kaggle, berisi sekitar **11.914 data mobil**. Fitur yang digunakan meliputi merek, model, tahun pembuatan, tenaga mesin (`engine_hp`), jumlah silinder, konsumsi bahan bakar (highway/city mpg), jenis transmisi, dan lain-lain, untuk memprediksi harga (**MSRP** — *Manufacturer Suggested Retail Price*).

## 🧠 Metode

Project ini mengimplementasikan **Regresi Linear** secara manual menggunakan operasi matriks NumPy (tanpa library machine learning siap pakai untuk model utamanya).

> Regresi linear adalah metode statistik yang digunakan untuk memodelkan hubungan antara satu atau lebih variabel independen (prediktor) dengan satu variabel dependen (respons) — mencari garis lurus terbaik yang menggambarkan hubungan antar variabel tersebut.

Regresi linear dipilih karena kesederhanaannya dan kemampuannya menemukan hubungan linear antara fitur mobil dan harga mobil, menghasilkan persamaan linear yang dapat digunakan untuk memprediksi harga berdasarkan fitur-fitur tersebut.

## 🔁 Alur Pengerjaan

1. **Persiapan Data** — memuat data, membersihkan penamaan kolom dan nilai kategori yang tidak konsisten.
2. **EDA (Exploratory Data Analysis)** — melihat distribusi harga, menangani nilai yang hilang, dan membagi data menjadi train/validation/test (60/20/20).
3. **Implementasi Regresi Linear** — membangun fungsi regresi linear dari fungsi dasar (dot product) hingga bentuk vektor/matriks.
4. **Memahami Internal Regresi Linear** — melatih model dengan *normal equation* (`XᵀX`⁻¹`Xᵀy`).
5. **Evaluasi Model** — mengukur performa menggunakan **RMSE (Root Mean Squared Error)**.
6. **Rekayasa Fitur (Feature Engineering)** — menambahkan fitur baru seperti usia mobil (`age`) dan variabel kategorikal (jumlah pintu, merek, dll.) melalui *one-hot encoding* manual.
7. **Regularisasi** — menerapkan regularisasi (`ridge regression` sederhana) untuk mengatasi *multicollinearity* dan menstabilkan model.
8. **Menggunakan Model** — melatih model final pada seluruh data train+validation, lalu mengujinya pada data test dan memprediksi harga mobil baru.

## 🛠️ Teknologi yang Digunakan

- **Python**
- **Pandas** & **NumPy** — manipulasi data dan operasi matriks/perhitungan model
- **Matplotlib** & **Seaborn** — visualisasi data
- **Google Colab** — lingkungan pelatihan dan evaluasi model

## 📂 Struktur Project

```
Car-Price-Prediction-Project/
├── Car_Price_Prediction_Project.ipynb   # Notebook utama berisi seluruh alur project
└── README.md
```

## ▶️ Cara Menjalankan

1. **Clone repository**
   ```sh
   git clone https://github.com/alfdmsr/Car-Price-Prediction-Project.git
   cd Car-Price-Prediction-Project
   ```

2. **Unduh dataset** *Car Features and MSRP* dari Kaggle, lalu simpan sebagai `data.csv` pada direktori yang sama dengan notebook.

3. **Buka notebook**, bisa langsung melalui tombol *Open in Colab* di bagian atas notebook, atau secara lokal dengan Jupyter:
   ```sh
   pip install pandas numpy matplotlib seaborn jupyter
   jupyter notebook Car_Price_Prediction_Project.ipynb
   ```

4. Jalankan seluruh cell secara berurutan dari atas ke bawah.

## 📌 Catatan

Project ini dibuat untuk tujuan pembelajaran — implementasi regresi linear dilakukan secara manual (from scratch) agar lebih memahami mekanisme internal model, bukan hanya menggunakan fungsi `fit()` dari library seperti scikit-learn.
