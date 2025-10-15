# 🧠 Minggu 3 — Boolean Model untuk Pencarian Dokumen

Eksperimen ini bertujuan memahami cara kerja **Boolean Retrieval Model** dalam Sistem Temu Kembali Informasi (STKI).  
Model ini memungkinkan pencarian dokumen berdasarkan ekspresi logika menggunakan operator **AND**, **OR**, dan **NOT**.

## 🎯 Tujuan
- Memahami prinsip kerja model boolean dalam pencarian teks.  
- Mengimplementasikan proses *indexing* dan *retrieval* sederhana menggunakan Python.  
- Menghubungkan hasil preprocessing teks dengan model pencarian dokumen.

## 🔍 Langkah Eksperimen
1. **Import Library**
   - Menggunakan `NLTK`, `Sastrawi`, dan `pandas` untuk pemrosesan teks.
2. **Text Preprocessing**
   - *Case Folding*: Mengubah huruf menjadi huruf kecil.
   - *Tokenization*: Memecah dokumen menjadi token.
   - *Stopword Removal*: Menghapus kata umum yang tidak informatif.
   - *Stemming*: Mengubah kata ke bentuk dasarnya dengan stemmer Bahasa Indonesia (Sastrawi).
3. **Membangun Inverted Index**
   - Menyusun struktur data yang mencatat setiap term dan daftar dokumen tempat term tersebut muncul.
   - Contoh:
     ```
     {
       "data": [1, 3],
       "informasi": [2, 3],
       "retrieval": [1]
     }
     ```
4. **Pencarian dengan Boolean Query**
   - Pengguna dapat memasukkan query seperti:
     - `data AND informasi`
     - `data OR retrieval`
     - `informasi AND NOT retrieval`
   - Sistem akan mengembalikan daftar dokumen yang memenuhi ekspresi logika tersebut.
5. **Evaluasi Hasil**
   - Menampilkan daftar dokumen yang relevan sesuai query.

## 💾 Contoh Output
Query: data AND informasi
Hasil: Dokumen [1, 3]

## 📦 Dependensi
- Python ≥ 3.10  
- NLTK  
- Sastrawi  
- Pandas  

## 💡 Kesimpulan
Eksperimen ini menunjukkan bagaimana **Boolean Model** bekerja dengan menghubungkan preprocessing teks dan pencarian berbasis logika.  
Model ini merupakan dasar dari sistem pencarian klasik sebelum berkembang ke model vektor dan probabilistik.
