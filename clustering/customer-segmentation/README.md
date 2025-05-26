# Customer Segmentation using K-Means Clustering

## Overview
Proyek ini bertujuan untuk menganalisis perilaku pelanggan dengan menggunakan teknik machine learning, khususnya K-Means Clustering. Segmentasi dilakukan berdasarkan kebiasaan belanja dan karakteristik demografis pelanggan untuk membantu bisnis dalam menyusun strategi pemasaran yang lebih efektif.

## Dataset
Dataset berasal dari kampanye pemasaran dan mencakup informasi seperti:

- **Demografi**: Tahun lahir, pendidikan, status pernikahan, pendapatan.
- **Pengeluaran**: Belanja untuk wine, buah, daging, ikan, permen, emas.
- **Perilaku Pembelian**: Jumlah pembelian via web, katalog, toko, dan diskon.
- **Respon Promosi**: Penerimaan terhadap beberapa kampanye pemasaran.

## Struktur Proyek

### 1. Data Preprocessing
- Menangani data hilang (imputasi nilai pendapatan).
- Menghapus outlier (misalnya usia > 90, pendapatan > 600.000).
- Feature engineering (usia, total belanja, ukuran keluarga).
- Encoding variabel kategorikal.

### 2. Exploratory Data Analysis (EDA)
- Visualisasi distribusi variabel.
- Analisis korelasi antar fitur.

### 3. Dimensionality Reduction
- Menggunakan **Principal Component Analysis (PCA)** untuk mereduksi data ke **2 dimensi**.
- Mempermudah visualisasi dan clustering.

### 4. Clustering
- Penerapan **K-Means Clustering** untuk segmentasi pelanggan.
- Penentuan jumlah klaster optimal menggunakan:
  - **Elbow Method**
  - **Silhouette Score**

### 5. Analisis Klaster
- Profiling tiap klaster berdasarkan pengeluaran, pendapatan, ukuran keluarga, dan respon promosi.
- Visualisasi hasil klaster dalam **2D scatter plot** dan **radar chart**.

## Hasil
Terdapat 4 klaster pelanggan yang diidentifikasi:
- **Cluster 0**: Pengeluaran moderat, responsif terhadap promosi ke-4.
- **Cluster 1**: Pelanggan hemat, suka diskon, merespon promosi ke-3.
- **Cluster 2**: Pendapatan dan pengeluaran tinggi, suka belanja di toko dan katalog.
- **Cluster 3**: Pendapatan rendah, merespon minim promosi (terutama ke-3).

## Implikasi Bisnis
- **Pemasaran Terarah**: Tawarkan diskon ke Cluster 1, produk premium ke Cluster 2.
- **Alokasi Sumber Daya**: Fokus pada Cluster bernilai tinggi (Cluster 2).
- **Rekomendasi Produk**: Sesuaikan dengan pola belanja tiap klaster.

## Dependencies
- Python 3.x
- Library:
  - `numpy`, `pandas`
  - `matplotlib`, `seaborn`
  - `scikit-learn`
  - `yellowbrick`

## Cara Menjalankan Proyek
1. Clone repositori:
    ```bash
    git clone [repository_url]
    cd customer-segmentation-kmeans
    ```

2. Install dependensi:
    ```bash
    pip install -r requirements.txt
    ```

3. Jalankan notebook:
    ```bash
    jupyter notebook customer_segmentation.ipynb
    ```

## File
- `marketing_campaign.csv` : Dataset utama.
- `customer_segmentation.ipynb` : Notebook dengan seluruh analisis.
- `README.md` : Deskripsi proyek.

## Pengembangan Selanjutnya
- Uji algoritma clustering lain seperti DBSCAN atau Hierarchical Clustering.
- Tambahkan fitur baru seperti feedback pelanggan atau data sosial media.
- Deploy sebagai aplikasi web untuk segmentasi real-time.

## Kontributor
- Dwiki Febrian
