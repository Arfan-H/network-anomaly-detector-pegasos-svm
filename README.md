# network-anomaly-detector-pegasos-svm

# 🔐 Anomaly Detection in Network Traffic using Pegasos SVM

Deteksi anomali dalam lalu lintas jaringan menggunakan metode **Support Vector Machine (SVM)** yang dilatih dengan algoritma **Pegasos (Primal Estimated sub-Gradient SOlver)** berbasis **Stochastic Gradient Descent (SGD)**. Sistem ini menangani kasus klasifikasi **multi-kelas** dengan pendekatan **One-vs-One (OvO)** dan menggunakan **kernel RBF** untuk memisahkan data non-linear secara efisien.

## 📌 Fitur Utama

* Preprocessing data NSL-KDD 1999 secara menyeluruh (EDA, encoding, normalisasi, handling imbalance).
* Penerapan Pegasos SVM dengan kernel RBF.
* Klasifikasi multi-kelas menggunakan pendekatan One-vs-One.
* Evaluasi model dengan akurasi, precision, recall, F1-score, dan confusion matrix.
* Deploy model dalam aplikasi Streamlit.

## 🚀 Akses Aplikasi

🌐 [Streamlit App](https://anomaly-detection-in-network-traffic.streamlit.app)

## 🧠 Model

Model dibangun menggunakan:

* `PegasosKernelSVM`: Implementasi manual algoritma Pegasos untuk klasifikasi biner dengan kernel support.
* `OneVsOneSVM`: Klasifikasi multi-kelas berbasis voting dari beberapa klasifikasi biner (OvO).

> Lihat implementasi detail di [`modelSV.py`](modelSV.py)

## 📊 Dataset

Dataset: [NSL-KDD 1999](https://www.kaggle.com/datasets/hassan06/nslkdd)

* Fitur: 41 + 1 label
* Ukuran: 125.973 entri
* Format: `.txt`
* Label dikategorikan ulang menjadi 5 kelas:

  * 0: Normal
  * 1: DoS
  * 2: Probe
  * 3: R2L
  * 4: U2R


## 📂 Struktur File

```
├── modelSV.py                  # Implementasi Pegasos Kernel SVM dan OvO
├── BuildModel.ipynb           # Notebook proses training & evaluasi
├── Lampiran (Manual Guide).pdf
├── Laporan PMD.pdf            # Laporan lengkap berisi latar belakang dan metode
├── app.py                     # Streamlit app untuk prediksi
└── README.md                  # Dokumentasi proyek
```

