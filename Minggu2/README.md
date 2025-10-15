# 🧠 Minggu 2 — Text Preprocessing dengan NLTK

Eksperimen ini bertujuan untuk memahami dan mengimplementasikan tahap **text preprocessing** menggunakan library **NLTK (Natural Language Toolkit)** sebagai bagian dari mata kuliah *Sistem Temu Kembali Informasi (STKI)*.

## 🎯 Tujuan
Melakukan pembersihan dan normalisasi teks agar siap digunakan untuk proses analisis lebih lanjut seperti perhitungan frekuensi kata atau pembentukan *index term*.

## 🔍 Langkah Eksperimen
1. **Import Library**
   - Menggunakan `nltk`, `string`, dan `pandas`.
   - Melakukan *download* resource NLTK seperti `stopwords`.
2. **Input Data**
   - Menggunakan teks contoh yang berisi kalimat dalam Bahasa Indonesia.
3. **Case Folding**
   - Mengubah semua huruf menjadi huruf kecil (*lowercase*).
4. **Tokenization**
   - Memecah teks menjadi potongan kata (*tokens*).
5. **Cleaning**
   - Menghapus tanda baca, simbol, dan karakter non-alfabet.
6. **Stopword Removal**
   - Menghapus kata-kata umum yang tidak memiliki makna penting (seperti “dan”, “yang”, “atau”).
7. **Stemming**
   - Mengubah kata menjadi bentuk dasarnya menggunakan `PorterStemmer` atau stemmer Bahasa Indonesia.
8. **Output**
   - Menampilkan hasil tokenisasi, stopword removal, dan stemming.
   - (Opsional) Menyimpan hasil dalam file `.csv` untuk analisis lanjutan.

## 💾 Hasil
Hasil preprocessing menunjukkan perubahan signifikan pada teks:
- Teks menjadi bersih, terstandardisasi, dan siap untuk proses analisis lanjutan.
- Token yang tersisa merepresentasikan kata-kata penting (*keywords*) dari dokumen.

Contoh hasil:
Input: "Andi dan Icha kerap melakukan transaksi rutin secara daring atau online."
Output: ['andi', 'icha', 'kerap', 'laku', 'transaksi', 'rutin', 'daring', 'online']


## 📦 Dependensi
- Python ≥ 3.10
- NLTK
- Pandas
