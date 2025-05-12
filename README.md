# Submission-02_Klasifikasi_Image_CatsAndDogs
Submission-02 pada course Belajar Pengembangan Machine Learning - Dicoding

# Klasifikasi Image Cats vs Dogs 

## Deskripsi Project
Proyek ini mengembangkan model **Convolutional Neural Network (CNN)** untuk mengklasifikasikan gambar kucing (Cat) dan anjing (Dog) menggunakan dataset **Microsoft Cats vs Dogs** dari Kaggle. Model dilatih dengan TensorFlow dan mencapai akurasi validasi **89.65%** serta akurasi test **80%**. Model kemudian dikonversi ke format **TensorFlow Lite (TFLite)** dan **TensorFlow.js (TFJS)** untuk deployment di perangkat ringan dan aplikasi web.

## Fitur
- Preprocessing dataset dengan `ImageDataGenerator` dan augmentasi data.
- Arsitektur CNN sederhana dengan 3 lapisan konvolusi dan dropout.
- Callback seperti `EarlyStopping`, `ModelCheckpoint`, dan `ReduceLROnPlateau` untuk pelatihan optimal.
- Evaluasi model dengan confusion matrix dan classification report.
- Prediksi pada gambar baru yang diunggah pengguna.
- Konversi model ke TFLite dan TFJS.
- Dokumentasi library dalam `requirements.txt`.

## Prasyarat
- Python 3.8+
- Google Colab dengan GPU (untuk pelatihan)
- Akun Kaggle untuk mengunduh dataset
- Git untuk mengunggah ke GitHub

## Instalasi
1. **Clone repository**:
   ```bash
   git clone https://github.com/[username]/[repository].git
   cd [repository]
   ```
2. **Buat virtual environment** (opsional, direkomendasikan):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```
3. **Install dependensi**:
   ```bash
   pip install -r requirements.txt
   ```
4. **Unduh dataset**:
   - Dapatkan file `kaggle.json` dari Kaggle (Settings > API > Create New API Token).
   - Unggah `kaggle.json` saat diminta oleh kode.

## Struktur Direktori
```
cats-vs-dogs/
│
├── requirements.txt           # Daftar dependensi
├── savedModel.keras           # Model Keras yang dilatih
├── model.tflite               # Model TFLite
├── tfjs_model/                # Direktori model TFJS
├── tfjs_model.zip             # Arsip TFJS
└── README.md                  # Dokumentasi proyek
```

## Cara Menjalankan
1. **Buka Google Colab** dan buat notebook baru.
2. **Unggah semua file `.py`** dari repository ke Colab.
3. **Jalankan tahap demi tahap** 
4. **Uji model pada gambar baru**:
   - Jalankan `test_model.py`.
   - Unggah gambar kucing atau anjing saat diminta.
5. **Hasil**:
   - Akurasi validasi: **89.65%**.
   - Akurasi test: **80%**.
   - Model disimpan sebagai `savedModel.keras`, `model.tflite`, dan `tfjs_model.zip`.

## Deployment
- **TFLite**: Gunakan `model.tflite` untuk deployment di perangkat mobile/edge (contoh: Android dengan TensorFlow Lite Interpreter).
- **TFJS**: Gunakan folder `tfjs_model` (atau ekstrak `tfjs_model.zip`) untuk aplikasi web (contoh: dengan TensorFlow.js di browser).

## Catatan
- Dataset mungkin berisi file corrupt. Kode sudah menangani ini dengan validasi file.
- Akurasi test (80%) dapat ditingkatkan dengan menambah lapisan CNN atau epoch pelatihan.
- Untuk lingkungan tanpa GUI, gunakan `opencv-python-headless` alih-alih `opencv-python`.

## Kredit
- **Nama**: Faizal Riza
- **Akun Dicoding**: akuisal@gmail.com
- Dataset: [Microsoft Cats vs Dogs](https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset)



