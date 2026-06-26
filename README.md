# Klasifikasi Gambar Pemandangan Alam — Intel Image Classification

## Deskripsi Proyek
Proyek ini membangun model CNN (Convolutional Neural Network) untuk mengklasifikasikan gambar pemandangan alam ke dalam 6 kategori menggunakan dataset Intel Image Classification dari Kaggle.

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