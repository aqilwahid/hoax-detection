# Analisis Deteksi Hoaks pada Teks Bahasa Indonesia dengan NLP dan Naive Bayes

## 📌 Deskripsi
Proyek ini bertujuan untuk mendeteksi hoaks dalam teks berbahasa Indonesia menggunakan pendekatan **Natural Language Processing (NLP)** dan **Naive Bayes Classifier**. Model ini dirancang untuk menganalisis pola linguistik dalam berita atau teks dan mengklasifikasikannya sebagai hoaks atau bukan.

## 📜 Daftar Isi
- [Latar Belakang](#latar-belakang)
- [Fitur dan Metode](#fitur-dan-metode)
- [Arsitektur Model](#arsitektur-model)
- [Pipeline Proses](#pipeline-proses)
- [Instalasi](#instalasi)
- [Penggunaan](#penggunaan)
- [Hasil dan Evaluasi](#hasil-dan-evaluasi)
- [Kontributor](#kontributor)

---

## 📖 Latar Belakang
Penyebaran berita hoaks meningkat secara signifikan di era digital. Metode konvensional dalam mendeteksi hoaks memiliki banyak keterbatasan, seperti kurang adaptif terhadap volume data yang besar dan sulitnya mengidentifikasi pola dalam teks. Oleh karena itu, proyek ini menggunakan **NLP dan Naive Bayes** untuk mendeteksi hoaks dengan efisiensi tinggi.

### 🎯 Tujuan:
- Mengembangkan model deteksi hoaks berbasis **NLP** untuk teks berbahasa Indonesia.
- Menggunakan **Naive Bayes Classifier** untuk klasifikasi teks.
- Menyediakan model yang dapat membantu dalam pengidentifikasian berita palsu dengan tingkat akurasi yang tinggi.

---

## 🛠 Fitur dan Metode
Proses utama dalam proyek ini meliputi:

1. **Preprocessing Data**:
   - Tokenisasi
   - Stopword Removal
   - Stemming/Lemmatization
   - Case Folding
   - Pembersihan teks dari simbol/tanda baca

2. **Ekstraksi Fitur**:
   - **TF-IDF** untuk merepresentasikan kata berdasarkan bobot pentingnya.
   - **N-grams** untuk menangkap pola dalam teks.

3. **Model Klasifikasi**:
   - Menggunakan **Naive Bayes** sebagai algoritma utama.
   - Model dibangun berdasarkan dataset berita hoaks dan non-hoaks.

4. **Evaluasi Model**:
   - Akurasi
   - Precision
   - Recall
   - F1-Score

---

## 🏗 Arsitektur Model
Model ini terdiri dari beberapa komponen utama:
1. **Data Crawling** → Mengumpulkan data berita dari berbagai sumber.
2. **Preprocessing** → Membersihkan dan mempersiapkan teks untuk analisis.
3. **Feature Extraction** → Mengubah teks menjadi representasi numerik dengan **TF-IDF**.
4. **Model Training** → Menggunakan **Naive Bayes Classifier**.
5. **Prediction & Evaluation** → Menguji model dengan data baru.

---

## 🔄 Pipeline Proses
Berikut adalah tahapan utama dalam proyek:

1. **Pengumpulan Data** → Mengambil berita dari berbagai sumber.
2. **Preprocessing** → Membersihkan teks agar siap diproses.
3. **Ekstraksi Fitur** → Mengubah teks menjadi vektor numerik.
4. **Pelatihan Model** → Melatih model dengan **Naive Bayes**.
5. **Evaluasi Model** → Mengukur performa model menggunakan berbagai metrik.
6. **Prediksi** → Menggunakan model untuk mengklasifikasikan teks baru.

---

## 🏗 Instalasi

1. **Clone Repository**
   ```bash
   git clone https://github.com/username/nlp-hoax-detector.git
   cd nlp-hoax-detector
   ```

2. **Instal Dependensi**
   ```bash
   pip install -r requirements.txt
   ```

3. **Jalankan Notebook**
   - Buka `Google Colab` atau `Jupyter Notebook`
   - Jalankan notebook utama: `model_training.ipynb`

---

## 🚀 Penggunaan

1. **Menjalankan Model**
   ```python
   from naive_bayes_classifier import HoaxDetector

   detector = HoaxDetector()
   detector.load_model("model.pkl")

   text = "Presiden mengeluarkan kebijakan baru yang kontroversial..."
   prediction = detector.predict(text)
   print(f"Prediksi: {'Hoaks' if prediction == 1 else 'Bukan Hoaks'}")
   ```

2. **Evaluasi Model**
   ```python
   from evaluation import evaluate_model
   evaluate_model("model.pkl", "test_data.csv")
   ```

---

## 📊 Hasil dan Evaluasi

Setelah dilakukan pengujian terhadap dataset, berikut hasil evaluasi model:

| Metrik   | Skor  |
|----------|------|
| Akurasi  | 89%  |
| Presisi  | 85%  |
| Recall   | 88%  |
| F1-Score | 86%  |

📌 **Catatan**: Model mengalami tantangan dalam menangani **ketidakseimbangan data**, karena jumlah berita hoaks lebih sedikit dibandingkan berita non-hoaks.

---

## 👨‍💻 Kontributor

- **Akbar Riyan Nugroho**
- **Ach. Nur Aqil Wahid**

📢 Jika ada pertanyaan atau saran, silakan buka **Issue** atau kirim **Pull Request** di repository ini.