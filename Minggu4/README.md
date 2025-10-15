# 📚 Minggu 4 – Feature Extraction & Document Similarity

Minggu ini berfokus pada dua eksperimen penting dalam Information Retrieval:

1. **Feature Extraction (Bag of Words & TF-IDF)**
2. **Document Similarity menggunakan Cosine Similarity**


## 🧩 Struktur Folder

Minggu4/
│
├── 1-BOW-TFIDF/
│ ├── BOW-Praktek1.ipynb
│ ├── BOW-Praktek2-tfidf.ipynb
│ ├── FeatureExtractionBOW.ipynb
│ ├── clean_dataset_stem.csv
│ └── gb1.png
│
└── 2-DocumentSimilarity/
├── Document Similarity.ipynb
└── tmdb_5000_movies.csv.gz


---

## 🧠 Eksperimen 1: Bag of Words (BoW) & TF-IDF

**Tujuan:**  
Mengubah teks menjadi representasi numerik.

**Langkah Utama:**
1. Import data (`clean_dataset_stem.csv`)
2. Gunakan `CountVectorizer()` → representasi **BoW**
3. Gunakan `TfidfVectorizer()` → representasi **TF-IDF**
4. Bandingkan hasil keduanya

**Output:**  
Matriks fitur (BoW dan TF-IDF) untuk setiap dokumen.

---

## 🧮 Eksperimen 2: Document Similarity

**Tujuan:**  
Mengukur kemiripan antar dokumen teks menggunakan **Cosine Similarity**.

**Langkah Utama:**
1. Import dataset film `tmdb_5000_movies.csv.gz`
2. Vectorisasi teks overview dengan `TfidfVectorizer`
3. Hitung kemiripan antar dokumen dengan `cosine_similarity`
4. Buat fungsi rekomendasi film mirip berdasarkan judul

**Output:**  
Daftar film yang memiliki kemiripan isi dengan film input.

---

## ⚙️ Teknologi yang Digunakan
- Python 3.x  
- Scikit-learn  
- Pandas  
- Numpy  
- Google Colab / Jupyter Notebook  

---

## 🧾 Referensi
- Scikit-learn documentation: [https://scikit-learn.org/stable/modules/feature_extraction.html](https://scikit-learn.org/stable/modules/feature_extraction.html)  
- TMDB 5000 Movie Dataset – Kaggle
