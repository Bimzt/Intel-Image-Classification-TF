# Klasifikasi Gambar Pemandangan Alam Intel Image Classification

## Deskripsi Proyek
Proyek ini membangun model CNN (Convolutional Neural Network) untuk mengklasifikasikan gambar pemandangan alam ke dalam 6 kategori menggunakan dataset Intel Image Classification dari Kaggle.

## Dampak Proyek Terhadap bisnis
Proyek ini tidak hanya dirancang sebagai eksperimen *Computer Vision* semata, tetapi juga membawa dampak bisnis yang nyata dengan membuka peluang otomatisasi di berbagai sektor industri. Dalam manajemen aset digital, model ini dapat digunakan oleh platform stok foto atau aplikasi pariwisata untuk menyortir ribuan gambar lanskap secara otomatis, sehingga sangat mempercepat alur kerja dan mengurangi kebutuhan intervensi manual. Lebih jauh lagi, inisiatif ini berpotensi menjadi fondasi bagi sistem pemantauan iklim dan perencanaan tata kota, yang memungkinkan deteksi cepat terhadap elemen geografis seperti bangunan, area hutan, atau perubahan gletser melalui analisis citra drone maupun satelit. Dari perspektif rekayasa perangkat lunak dan arsitektur sistem, ketersediaan model dalam format TensorFlow Lite dan TensorFlow.js sangat mendukung penerapan *Edge AI*. Hal ini mendobrak ketergantungan pada server dengan memungkinkan proses inferensi dilakukan secara efisien dan langsung di perangkat *mobile* atau peramban (*browser*) pengguna, yang secara signifikan menekan biaya operasional *cloud* sekaligus menjaga privasi data karena gambar tidak perlu diunggah ke *server* luar.

## Dataset
- **Sumber:** [Intel Image Classification — Kaggle](https://www.kaggle.com/datasets/puneet6060/intel-image-classification)
- **Jumlah gambar:** ~25.000 gambar (150×150 piksel)
- **Kelas:** `buildings`, `forest`, `glacier`, `mountain`, `sea`, `street`
- **Split:**
  - `seg_train/` -> Training set
  - `seg_test/` -> Test set
  - `seg_pred/` -> Validation/Prediction set

## Struktur Direktori
```
submission/
├── tfjs_model/
│   ├── group1-shard1of1.bin
│   └── model.json
├── tflite/
│   ├── model.tflite
│   └── label.txt
├── saved_model/
│   ├── saved_model.pb
│   └── variables/
├── notebook.ipynb
├── README.md
└── requirements.txt
```

## Cara Menjalankan
1. Upload folder `data_deep_learning/` ke Google Drive
2. Buka `notebook.ipynb` di Google Colab
3. Mount Google Drive dan sesuaikan path dataset jika perlu
4. Jalankan semua sel secara berurutan

## Instalasi Dependensi
```bash
pip install -r requirements.txt
```

## Hasil Model
- Akurasi Training: > 85%
- Akurasi Testing: > 85%
- Format model yang disimpan: SavedModel, TF-Lite, TensorFlow.js

## Teknologi
- Python 3.10+
- TensorFlow / Keras 2.15
- TensorFlow.js
- Matplotlib
- Scikit-learn
