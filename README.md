# Sistem Temu Kembali Informasi (STKI)
Repositori ini berisi kumpulan hasil **eksperimen mingguan mata kuliah STKI (Sistem Temu Kembali Informasi)**.  
Seluruh eksperimen dijalankan menggunakan **Google Colab** dan disimpan di repositori ini sebagai dokumentasi pembelajaran.

---

## Daftar Eksperimen

### 📂 Minggu 2 — *Document Preprocessing & Word Frequency*
**Tujuan:**  
Melakukan proses awal pengolahan teks seperti:
- *Case folding* (mengubah semua huruf menjadi huruf kecil)
- *Tokenisasi* (memecah teks menjadi kata-kata)
- *Stopword removal* (menghapus kata-kata umum seperti "dan", "yang", dll)
- Analisis frekuensi kata  

**Output:**  
Dataset teks yang sudah dibersihkan dan file CSV berisi daftar kata serta jumlah kemunculannya.

**Notebook utama:**  
📂 [Minggu 2 — Text Preprocessing & Word Frequency](Minggu2/)

---

### 📂 Minggu 3 — *Boolean Retrieval Model*

**Tujuan:**  
Membangun model pencarian sederhana berdasarkan **Boolean Model** menggunakan operator logika seperti:
- `AND`
- `OR`
- `NOT`

**Langkah utama:**
1. Melakukan preprocessing teks (tokenisasi dan stopword removal)
2. Membuat *inverted index* dari kumpulan dokumen
3. Menerapkan pencarian berdasarkan query Boolean seperti `modi AND india`

**Output:**  
Hasil pencarian berupa daftar dokumen yang relevan terhadap query Boolean.
 
**Notebook utama:**  
📂 [Minggu 3 — Boolean Model](Minggu3/)

---

### 📂 Minggu 4 — *Feature Extraction & Document Similarity*

**Eksperimen 1 — TF-IDF Vectorization**  
Melakukan *feature extraction* menggunakan metode:
- **Bag of Words (BoW)**
- **TF-IDF (Term Frequency – Inverse Document Frequency)**  
Tujuannya untuk merepresentasikan dokumen dalam bentuk numerik (vektor).

**Eksperimen 2 — Document Similarity**  
Menghitung tingkat kesamaan antar dokumen menggunakan **Cosine Similarity** berdasarkan hasil TF-IDF.

**Output:**  
- File `tfidf_matrix.csv` yang berisi bobot kata untuk tiap dokumen  
- Matriks kesamaan antar dokumen (`similarity_matrix`)

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
