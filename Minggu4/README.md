# 📚 Minggu 4 — Feature Extraction & Document Similarity

Eksperimen minggu ini membahas dua konsep penting dalam **Information Retrieval (IR)** dan **Natural Language Processing (NLP)**, yaitu:
1.  **Feature Extraction** menggunakan *Bag-of-Words (BoW)* dan *TF-IDF* untuk mengubah teks menjadi data numerik.
2.  **Document Similarity** menggunakan *Cosine Similarity* untuk mengukur kemiripan antar dokumen/fitur yang telah diekstrak.

---

## 🧠 Eksperimen 1 — Bag of Words (BoW) & TF-IDF

### 🎯 Tujuan
Mengubah kumpulan teks menjadi representasi numerik (**vektor fitur**) yang dapat digunakan dalam perhitungan kemiripan dan analisis teks lebih lanjut.

### 🔍 Konsep Kunci
| Konsep | Deskripsi |
| :--- | :--- |
| **Bag-of-Words (BoW)** | Model sederhana yang merepresentasikan teks sebagai kantong kata. Nilai sel adalah **frekuensi absolut** (Count) kemunculan kata dalam dokumen. |
| **TF-IDF** | Teknik pembobotan yang menyeimbangkan antara **Term Frequency (TF)** dan **Inverse Document Frequency (IDF)**. Memberikan bobot tinggi pada kata yang sering muncul di satu dokumen tetapi jarang di seluruh korpus (kata kunci penting). |

### 🛠️ Langkah-Langkah Teknis
1.  **Import Dataset**: Menggunakan dataset hasil *preprocessing* (`clean\_dataset\_stem.csv` atau data teks Anda).
2.  **Vectorization (BoW)**: Menggunakan `CountVectorizer()` dari *scikit-learn*.
3.  **Vectorization (TF-IDF)**: Menggunakan `TfidfVectorizer()`.
4.  **Export Matriks**: Matriks hasil TF-IDF diekspor ke file **`tfidf_matrix.csv`** untuk digunakan pada eksperimen berikutnya.

### 💾 Output
* **Matriks fitur hasil *CountVectorizer* (BoW)**: Matriks frekuensi kata.
* **Matriks fitur hasil *TfidfVectorizer* (TF-IDF)**: Matriks bobot kata terpenting.

**Contoh Output (TF-IDF Matriks):**
| | data | informasi | retrieval |
| :---: | :---: | :---: | :---: |
| Dokumen 1 | 0.707 | 0.5 | 0.5 |
| Dokumen 2 | 0.0 | 0.707 | 0.707 |

---

## 🤖 Eksperimen 2 — Document Similarity (Cosine Similarity)

### 🎯 Tujuan
Mengukur kemiripan antara dokumen teks secara kuantitatif menggunakan representasi vektor TF-IDF, yang merupakan langkah fundamental dalam **Information Retrieval (IR)** dan pengelompokan dokumen.

### 🔍 Konsep Kunci
| Konsep | Deskripsi |
| :--- | :--- |
| **Cosine Similarity** ($\cos(\theta)$) | Metrik yang mengukur kesamaan antara dua vektor dalam ruang multidimensi. Nilai berkisar antara **0** (tidak mirip, ortogonal) hingga **1** (identik). |
| **Input Matriks** | Proses ini menggunakan **`tfidf_matrix.csv`** sebagai input, di mana setiap baris dianggap sebagai vektor dokumen. |

### 🛠️ Langkah-Langkah Teknis
1.  **Import Matriks TF-IDF**: Memuat file **`tfidf_matrix.csv`** yang dihasilkan dari Eksperimen 1.
2.  **Compute Similarity**: Menggunakan fungsi `cosine\_similarity()` dari *sklearn.metrics.pairwise* dan menerapkannya pada matriks TF-IDF. Fungsi ini akan membandingkan setiap pasangan baris (dokumen) di dalam matriks.
3.  **Visualisasi Hasil**: Matriks hasil kemiripan disajikan dalam bentuk DataFrame agar mudah diinterpretasikan, dengan label baris dan kolom yang menunjukkan dokumen yang dibandingkan (misalnya, Doc1, Doc2, dst.).

### 💾 Output
* **Matriks Cosine Similarity** antar dokumen.

**Contoh Output Matriks Cosine Similarity:**
| | Doc1 | Doc2 | Doc3 | Doc4 |
| :---: | :---: | :---: | :---: | :---: |
| **Doc1** | 1.000 | 0.320 | 0.275 | 0.271 |
| **Doc2** | 0.320 | 1.000 | 0.000 | 0.247 |
| **Doc3** | 0.275 | 0.000 | 1.000 | 0.106 |
| **Doc4** | 0.271 | 0.247 | 0.106 | 1.000 |

*Interpretasi:* Nilai **0.000** antara Doc2 dan Doc3 menunjukkan kedua dokumen tersebut memiliki kemiripan paling rendah berdasarkan bobot kata kunci TF-IDF mereka.
