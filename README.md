# Mini Data Science Project - Customer Churn Analysis

Proyek data science end-to-end yang menganalisis data pelanggan telekomunikasi untuk memahami faktor-faktor yang mempengaruhi churn dan membangun model prediksi menggunakan Random Forest.

---

## Tujuan

1. Melakukan Exploratory Data Analysis (EDA) untuk memahami pola churn pelanggan
2. Mengidentifikasi faktor-faktor utama yang mempengaruhi churn
3. Membangun model klasifikasi untuk memprediksi pelanggan yang berisiko churn
4. Memberikan rekomendasi bisnis berdasarkan temuan analisis

---

## Dataset

**Telco Customer Churn** dari Kaggle, berisi data 7.043 pelanggan perusahaan telekomunikasi dengan 21 kolom meliputi: informasi demografis, layanan yang digunakan, informasi kontrak, dan status churn.

---

## Alur Analisis

### 1. Memuat dan Memahami Data
Membaca dataset, mengecek dimensi, tipe data, missing values, dan distribusi target variable (churn).

### 2. Exploratory Data Analysis (EDA)
Visualisasi untuk memahami pola data:
- Churn berdasarkan tipe kontrak (Month-to-month vs One year vs Two year)
- Churn berdasarkan jenis internet service (DSL vs Fiber optic)
- Distribusi tenure dan monthly charges berdasarkan status churn

### 3. Insight dari EDA
- Kontrak bulanan memiliki tingkat churn paling tinggi
- Pelanggan dengan tenure rendah (baru berlangganan) lebih cenderung churn
- Monthly charges tinggi berkorelasi dengan tingkat churn yang lebih tinggi
- Fiber optic memiliki tingkat churn lebih tinggi dibanding DSL

### 4. Persiapan Data untuk Model
- Konversi tipe data (TotalCharges ke numerik)
- Handling missing values dengan median
- Encoding variabel kategorikal (Contract, InternetService)
- Pemilihan fitur: tenure, MonthlyCharges, TotalCharges, Contract, InternetService

### 5. Membangun Model Prediksi
- Split data: 80% training, 20% testing
- Algoritma: Random Forest Classifier (100 trees)
- Evaluasi: accuracy, precision, recall, F1-score, confusion matrix

### 6. Kesimpulan dan Rekomendasi Bisnis
Rekomendasi berbasis data untuk mengurangi churn rate.

---

## Hasil Model

| Metrik | Nilai |
|--------|-------|
| Akurasi | ~79% |
| Feature terpenting | tenure, MonthlyCharges, TotalCharges |

---

## Visualisasi yang Dihasilkan

| File | Deskripsi |
|------|-----------|
| `eda_churn_overview.png` | Churn berdasarkan kontrak, internet service, dan distribusi keseluruhan |
| `eda_tenure_charges.png` | Distribusi tenure dan monthly charges berdasarkan churn |
| `model_results.png` | Confusion matrix dan feature importance |

---

## Rekomendasi Bisnis

1. Buat program loyalitas untuk pelanggan baru (0-12 bulan pertama)
2. Tawarkan insentif migrasi dari kontrak bulanan ke kontrak tahunan
3. Review pricing strategy untuk pelanggan dengan monthly charges tinggi
4. Fokuskan retensi pada segment fiber optic yang memiliki churn rate tinggi

---

## Struktur File

```
mini-data-science-project/
├── customer_churn_analysis.ipynb   # Jupyter Notebook (analisis lengkap)
├── telco_churn.csv                 # Dataset
├── eda_churn_overview.png          # Output visualisasi EDA
├── eda_tenure_charges.png          # Output visualisasi EDA
├── model_results.png               # Output hasil model
└── README.md
```

---

## Teknologi yang Digunakan

| Teknologi | Fungsi |
|-----------|--------|
| Python 3 | Bahasa pemrograman utama |
| pandas | Manipulasi dan analisis data |
| matplotlib | Pembuatan visualisasi |
| seaborn | Visualisasi statistik (heatmap, distribusi) |
| scikit-learn | Machine learning (Random Forest, train/test split, evaluasi) |
| Jupyter Notebook | Environment interaktif untuk analisis data |

---

## Tentang

Proyek ini dibuat sebagai bagian dari proses belajar data science, mulai dari eksplorasi data hingga pembuatan model machine learning sederhana. Fokus utama adalah pada proses analisis dan penyajian insight yang dapat diterjemahkan menjadi rekomendasi bisnis.
