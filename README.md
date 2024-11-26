# Dokumentasi Proyek Analisis Sentimen

## 1. Judul Project
Analisis Sentimen pada Ulasan Lazada (Lazada Indonesian Reviews)

## 2. Deskripsi
Proyek ini dirancang untuk melakukan analisis sentimen pada ulasan produk Lazada dalam bahasa Indonesia. Melalui preprocessing teks, model machine learning atau deep learning digunakan untuk mengklasifikasikan sentimen ulasan sebagai positif atau negatif. Proyek ini bertujuan membantu bisnis memahami opini pelanggan secara lebih efektif.

## 3. Fitur Utama
- Preprocessing Teks: Pembersihan data (Casefolding, Punctuation, Slangword, Repetition Character, Stemming, and Stopword), tokenisasi, dan representasi teks dengan teknik seperti TF-IDF.
- Klasifikasi Sentimen: Model yang digunakan adalah Naive Bayes.
- Evaluasi Model: Hasil analisis dilengkapi dengan metrik evaluasi seperti akurasi, precision, recall, F1-score.
- Visualisasi Data: Confusion matrix.

## 4. Persyaratan
- Python >= 3.8
- Library yang diperlukan
numpy, pandas, scikit-learn, nltk, matplotlib, seaborn, time, pickle, string, re, and sastrawi.
- Dataset Lazada Indonesian Reviews dari Kaggle.

## 5. Hasil Preprocessing
Proses preprocessing adalah langkah awal untuk mempersiapkan data teks agar dapat digunakan dalam analisis sentimen. Dataset Lazada Indonesian Reviews terdiri dari ulasan pelanggan dalam bahasa Indonesia. Langkah-langkah yang dilakukan selama preprocessing mencakup:
- Pembersihan Data Teks
  - a. Semua teks diubah menjadi huruf kecil untuk memastikan konsistensi.
  - b. Tanda baca, angka, dan karakter khusus dihapus agar teks lebih bersih.
  - c. Stopwords (kata-kata umum seperti "yang", "dan", "di") dihapus
    menggunakan daftar stopwords Bahasa Indonesia.
- Tokenisasi dan Stemming
  - a. Teks dipecah menjadi kata-kata (tokenisasi) agar lebih mudah diproses.
  - b. Kata-kata diubah menjadi bentuk dasarnya (stemming) menggunakan
    library NLP seperti Sastrawi.
- Representasi Data
Setelah preprocessing, teks direpresentasikan dalam bentuk fitur numerik. Teknik yang digunakan: TF-IDF (Term Frequency-Inverse Document Frequency) untuk menghitung bobot pentingnya setiap kata dalam ulasan.

## 6. Hasil Klasifikasi 
- Penggunaan model Naive Bayes untuk klasifikasi sentimen menunjukkan kinerja yang sangat baik. Model dilatih dalam waktu yang sangat singkat, yaitu hanya 0,1018 detik, menunjukkan efisiensi tinggi untuk dataset besar berbasis teks. Berdasarkan laporan evaluasi, model berhasil mencapai akurasi sebesar 90%, yang berarti sekitar 90% data uji diklasifikasikan dengan benar. Untuk label 'negatif', precision sebesar 89% menunjukkan bahwa prediksi negatif cukup akurat, sementara recall sebesar 91% mengindikasikan bahwa sebagian besar data negatif berhasil dikenali dengan baik. F1-score sebesar 90% menunjukkan keseimbangan yang optimal antara precision dan recall. Hal serupa juga terlihat pada label 'positif', di mana precision mencapai 91%, recall sebesar 89%, dan F1-score sebesar 90%.
- Kinerja model secara keseluruhan dinilai konsisten dengan rata-rata precision, recall, dan F1-score sebesar 90%, baik berdasarkan rata-rata makro (tanpa mempertimbangkan distribusi kelas) maupun rata-rata tertimbang (dengan mempertimbangkan distribusi data). Melalui hasil ini menunjukkan bahwa model tidak bias terhadap salah satu kelas dan bekerja dengan baik pada dataset ini.  Selain dengan performa yang cepat dan akurat, Naive Bayes menjadi pilihan yang sangat cocok untuk tugas klasifikasi sentimen tetapi untuk peningkatan lebih lanjut perlu melakukan perbandingan dengan algoritma lain.
- Hasil evaluasi menggunakan confusion matrix divisualisasikan dalam bentuk heatmap, yang menunjukkan distribusi prediksi dibandingkan dengan label aktual. Terdapat 161 false positif (kelas negatif salah diprediksi sebagai positif) dan 198 false negatif (kelas positif salah diprediksi sebagai negatif). Kesalahan berupa false positif dan false negatif menunjukkan bahwa model masih memiliki ruang untuk ditingkatkan, melalui algoritma yang lebih kompleks.


