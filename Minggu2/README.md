### 📂 Minggu 2 — *Text Preprocessing dengan NLTK*
**Tujuan:**  
Melakukan tahap awal pengolahan teks menggunakan pustaka NLTK untuk mempersiapkan data sebelum digunakan dalam model pencarian informasi.

**Tahapan Eksperimen:**
1. Import dan Pembacaan Data
   - Membaca dataset teks dari file .txt atau input langsung.
   - Menampilkan contoh isi dokumen.
2. Case Folding
   - Mengubah seluruh huruf menjadi huruf kecil agar konsisten
3. Tokenisasi
   - Memecah teks menjadi satuan kata menggunakan nltk.word_tokenize().
4. Pembersihan Teks (Cleaning)
   - Menghapus tanda baca (string.punctuation), angka, serta karakter non-alfabet dengan modul re (regular expression).
5. Stopword Removal
   - Menghapus kata-kata umum yang tidak memiliki makna penting (seperti “yang”, “dan”, “di”) menggunakan daftar stopword bahasa Indonesia dari nltk.corpus.stopwords.
6. Stemming (opsional, jika digunakan)
   - Mengubah kata ke bentuk dasarnya dengan StemmerFactory dari Sastrawi jika diaktifkan pada bagian eksperimen.
7. Perhitungan Frekuensi Kata (Word Frequency)
   - Menghitung jumlah kemunculan setiap kata dalam dokumen menggunakan nltk.FreqDist().
   - Menyimpan hasil dalam bentuk DataFrame agar mudah divisualisasikan.
8. Visualisasi
   - Membuat bar chart frekuensi kata paling sering muncul menggunakan matplotlib.
   - Menampilkan WordCloud (jika digunakan) untuk ilustrasi distribusi kata.

Tools yang Digunakan:
nltk, re, string, pandas, matplotlib, (opsional: Sastrawi, wordcloud)
