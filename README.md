# Sistem Case-Based Reasoning (CBR) untuk Analisis Putusan Pengadilan Indonesia

## Deskripsi Proyek

Proyek ini merupakan implementasi metode **Case-Based Reasoning (CBR)** untuk melakukan analisis putusan pengadilan Indonesia. Sistem dibangun dengan memanfaatkan dokumen putusan sebagai basis kasus (case base), kemudian melakukan pencarian kasus serupa dan memberikan rekomendasi berdasarkan kasus-kasus yang pernah terjadi sebelumnya.

Proyek ini dikembangkan sebagai tugas mata kuliah **Penalaran Komputer** Program Studi Informatika Universitas Muhammadiyah Malang.

## Tujuan

Tujuan dari proyek ini adalah:

1. Membangun basis kasus dari dokumen putusan pengadilan.
2. Melakukan representasi kasus menggunakan metadata dan fitur teks.
3. Mengimplementasikan mekanisme pencarian kasus serupa (case retrieval).
4. Mengimplementasikan mekanisme pemanfaatan solusi dari kasus sebelumnya (case reuse).
5. Melakukan evaluasi performa model menggunakan berbagai metrik pengukuran.

## Tahapan Case-Based Reasoning

Sistem dikembangkan berdasarkan siklus Case-Based Reasoning yang terdiri dari:

### 1. Case Base Construction

* Pengumpulan dokumen putusan pengadilan.
* Ekstraksi teks dari dokumen.
* Pembersihan dan normalisasi data.

### 2. Case Representation

* Ekstraksi metadata perkara.
* Representasi dokumen dalam bentuk fitur teks.
* Penyimpanan data dalam format terstruktur.

### 3. Case Retrieval

Metode yang digunakan:

* TF-IDF + Support Vector Machine (SVM)
* TF-IDF + Naive Bayes
* BERT Retrieval

### 4. Case Solution Reuse

* Mengambil kasus dengan tingkat kemiripan tertinggi.
* Menghasilkan rekomendasi berdasarkan kasus terdahulu.

### 5. Evaluation

Evaluasi dilakukan menggunakan:

* Accuracy
* Precision
* Recall
* F1-Score

## Struktur Repository

```text
Penalaran-Komputer-CBR
│
├── data
│   ├── raw
│   │   └── .gitkeep
│   │
│   └── processed
│       ├── cases.csv
│       ├── cases.json
│       ├── queries.json
│       ├── predictions.csv
│       ├── retrieval_metrics.csv
│       └── prediction_metrics.csv
│
├── notebooks
│   └── Penalaran_Komputer_CBR_215_209.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

## Kebutuhan Sistem

* Python 3.10 atau lebih baru
* Jupyter Notebook

## Instalasi

Clone repository:

```bash
git clone https://github.com/TegarReskiPratama/Penalaran-Komputer-CBR.git
cd Penalaran-Komputer-CBR
```

Install seluruh dependency:

```bash
pip install -r requirements.txt
```

## Cara Menjalankan Program

Jalankan Jupyter Notebook:

```bash
jupyter notebook
```

Kemudian buka file:

```text
notebooks/Penalaran_Komputer_CBR_215_209.ipynb
```

Jalankan seluruh cell secara berurutan dari atas ke bawah hingga proses selesai.

## Dataset

Dataset yang digunakan berasal dari dokumen putusan pengadilan yang diperoleh dari Direktori Putusan Mahkamah Agung Republik Indonesia.

## Hasil yang Dihasilkan

Program menghasilkan beberapa file keluaran sebagai berikut:

| File                   | Keterangan                   |
| ---------------------- | ---------------------------- |
| cases.csv              | Data kasus dalam format CSV  |
| cases.json             | Data kasus dalam format JSON |
| queries.json           | Data query dan ground truth  |
| predictions.csv        | Hasil prediksi kasus         |
| retrieval_metrics.csv  | Hasil evaluasi retrieval     |
| prediction_metrics.csv | Hasil evaluasi klasifikasi   |

## Hasil Evaluasi

| Model                | Accuracy | Precision | Recall   | F1-Score |
| -------------------- | -------- | --------- | -------- | -------- |
| TF-IDF + SVM         | 0.857143 | 0.734694  | 0.857143 | 0.791209 |
| TF-IDF + Naive Bayes | 0.857143 | 0.734694  | 0.857143 | 0.791209 |
| BERT Retrieval       | 0.857143 | 0.734694  | 0.857143 | 0.791209 |

Berdasarkan hasil evaluasi, seluruh model menghasilkan performa yang sama pada dataset yang digunakan. Hal ini menunjukkan bahwa ukuran dataset yang relatif terbatas belum mampu menunjukkan perbedaan performa yang signifikan antara metode machine learning tradisional dan pendekatan berbasis transformer.

## Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dilakukan pada penelitian berikutnya antara lain:

* Menambah jumlah dokumen putusan.
* Melakukan fine-tuning model BERT khusus domain hukum.
* Menggabungkan fitur metadata dengan embedding semantik.
* Mengembangkan metode hybrid retrieval untuk meningkatkan akurasi pencarian kasus.

## Penulis

Nama : Tegar Reski Pratama

Program Studi : Informatika

Universitas : Universitas Muhammadiyah Malang

Mata Kuliah : Penalaran Komputer

Tahun Akademik : 2025/2026

## Lisensi

Repository ini dibuat untuk keperluan akademik dan pembelajaran.
