# Sistem Temu Kembali Informasi (STKI)
Repositori ini berisi kumpulan hasil **eksperimen mingguan mata kuliah STKI (Sistem Temu Kembali Informasi)**.  
Seluruh eksperimen dijalankan menggunakan **Google Colab** dan disimpan di repositori ini sebagai dokumentasi pembelajaran.

---

## Daftar Eksperimen

### 📂 Minggu 2 — *Text Preprocessing dengan NLTK*
**Tujuan:**  
Melakukan tahapan awal pengolahan teks menggunakan Natural Language Toolkit (NLTK) untuk membersihkan dan menyiapkan data teks sebelum digunakan dalam model Information Retrieval.

**Tahapan Eksperimen:**
1. Membaca teks berita dari file .json
2. Melakukan case folding (mengubah seluruh huruf menjadi huruf kecil)
3. Membersihkan teks dari angka, tanda baca, dan karakter non-alfabet
4. Melakukan tokenisasi menggunakan nltk.word_tokenize()
5. Menghapus stopwords menggunakan daftar kata umum dari nltk.corpus.stopwords
6. Melakukan stemming untuk mengembalikan kata ke bentuk dasar (misalnya: “berlari” → “lari”)

**Hasil:**
Dataset yang sudah dibersihkan dan siap digunakan untuk proses selanjutnya seperti indexing dan retrieval.

**Tools & Library:**
nltk, re, string, pandas, matplotlib, (opsional: Sastrawi, wordcloud)

📁 [Minggu 2 — Text Preprocessing dengan NLTK](Minggu2/)
📄 Notebook: TextPreprocessing_NLTK.ipynb

---

### 📂 Minggu 3 — *Boolean Model Implementation*

**Tujuan:**  
Membangun sistem pencarian informasi sederhana menggunakan Boolean Retrieval Model,
yang bekerja berdasarkan operasi logika (AND, OR, NOT) untuk menemukan dokumen yang relevan terhadap query pengguna.

**Tahapan Eksperimen:**
1. Membaca dokumen teks (.txt) dari folder data/
2. Melakukan text preprocessing (case folding, tokenisasi, stopword removal)
3. Membentuk Inverted Index untuk mencatat kemunculan setiap term dalam dokumen
4. Menyusun Incidence Matrix yang merepresentasikan relasi term ↔ dokumen
5. Mengimplementasikan fungsi pencarian Boolean menggunakan operator:
   - AND → semua kata harus muncul
   - OR → salah satu kata muncul
   - NOT → mengecualikan kata tertentu
6. Menguji hasil query dan menganalisis kombinasi logika pencarian

**Hasil:**
Sistem pencarian berbasis Boolean sederhana yang dapat memproses query dan menampilkan daftar dokumen relevan.

**Tools & Library:**
nltk, re, glob, pandas, numpy

📁 [Minggu 3 — Boolean Model Implementation](Minggu3/)
📄 Notebook: boolean_model.ipynb

---

### 📂 Minggu 4 — *Vector Space Model (Bag of Words & TF-IDF)*

**Tujuan:**
Menerapkan representasi teks menggunakan Vector Space Model (VSM) dengan pendekatan Bag of Words (BoW) dan TF-IDF weighting untuk mengukur kesamaan antar dokumen.

**Tahapan Eksperimen 1 — Bag of Words & TF-IDF:**
1. Membaca dataset .csv
2. Melakukan preprocessing ringan terhadap teks (case folding, tokenisasi)
3. Mengubah teks menjadi representasi numerik dengan:
   - CountVectorizer → Bag of Words
   - TfidfVectorizer → TF-IDF
4. Membandingkan hasil dua model dalam bentuk matrix term-document
5. Menyimpan hasil TF-IDF dalam file .csv

📓 Notebook: bag_of_words&TF_IDF.ipynb

**Tahapan Eksperimen 2 — Document Similarity:**
1. Membaca hasil TF-IDF matrix
2. Menghitung cosine similarity antar dokumen
3. Menampilkan hasil dalam bentuk similarity matrix
4. Menginterpretasikan nilai kesamaan antar dokumen

📓 Notebook: document_similarity.ipynb

**Hasil:**
Model VSM yang mampu merepresentasikan teks dalam ruang vektor
dan menghitung kemiripan antar dokumen dengan metode cosine similarity.

**Tools & Library:**
scikit-learn, pandas, seaborn, matplotlib, wordcloud

**Notebook utama:**  
📂 [Minggu 4 — TF-IDF & Cosine Similarity](Minggu4/)

---

## Catatan Tambahan
- Semua eksperimen menggunakan pustaka:
  - `nltk`
  - `scikit-learn`
  - `pandas`
  - `numpy`
- Setiap folder berisi:
  - `data/` → kumpulan dokumen teks  
  - `notebooks/` → notebook eksperimen utama  
  - `results/` → hasil olahan model  
- Struktur folder mengikuti format mingguan agar mudah ditelusuri

| Kategori               | Teknologi                      |
| :--------------------- | :----------------------------- |
| **Bahasa Pemrograman** | Python 3.10                    |
| **Platform**           | Google Colab                   |
| **Visualisasi**        | Matplotlib, Seaborn, WordCloud |
| **NLP Tools**          | NLTK, scikit-learn             |
| **Version Control**    | Git + GitHub                   |
