# State of the Art (SOTA) - Analisis Sentimen Keamanan Data

**1. Judul**
ANALISIS SENTIMEN TERKAIT PERSEPSI KEAMANAN DATA INFORMASI DAN PRIVASI DI INDONESIA MENGGUNAKAN PENDEKATAN MACHINE LEARNING

**2. Nama dan Tahun**
*   **Penulis:** Alvali Zaqi Taufan, Wahyu Wibowo
*   **Tahun:** 2024
*   **Publikasi:** Jurnal Informatika Teknologi dan Sains (JINTEKS), Vol. 6, No. 3, Agustus 2024

**3. Latar Belakang Masalah dan Data yang Digunakan**
*   **Latar Belakang:** Peningkatan penetrasi internet di Indonesia (mencapai 213 juta pengguna pada 2023) memunculkan masalah baru terkait keamanan data, informasi, dan privasi. Pengesahan UU PDP (Pelindungan Data Pribadi) pada September 2022 belum menunjukkan dampak signifikan dalam penanganan kasus kebocoran data. Penelitian ini bertujuan mengetahui sentimen masyarakat untuk memberikan rekomendasi kepada organisasi terkait (seperti BSSN dan Kominfo) dalam penyusunan aturan turunan UU PDP.
*   **Data:** Data yang digunakan adalah cuitan (tweets) dari masyarakat Indonesia di platform Twitter (X.com).
    *   **Jumlah Data:** 10.151 cuitan.
    *   **Periode Pengambilan:** 1 Februari 2024 – 7 April 2024.
    *   **Kata Kunci:** Terkait data, informasi, privasi, serta organisasi seperti Kominfo dan BSSN.

**4. Metode / Algoritma**
Pendekatan *Machine Learning* dengan metode klasifikasi, membandingkan performa antara:
*   Random Forest (dengan variasi *Count Vectorizer* dan *TF-IDF Vectorizer*)
*   Support Vector Machine (Linear SVM)
*   (Naïve Bayes juga disebutkan dalam metodologi sebagai pembanding awal/metode yang umum, namun fokus utama hasil adalah perbandingan RF dan SVM).

**5. Bagaimana Metode / Algoritma Digunakan**
*   **Pengumpulan Data:** *Web scraping* menggunakan API Twitter.
*   **Preprocessing Text:** Meliputi *Data Cleansing* (menghapus *noise*, data kosong, duplikat), *Case Folding*, *Tokenizing*, *Stemming*, dan *Filtering*.
*   **Feature Extraction:** Menggunakan TF-IDF (*Term Frequency-Inverse Document Frequency*) dan pembobotan kata.
*   **Pelabelan:** Menggunakan *Lexicon Based* untuk menentukan sentimen Positif, Negatif, atau Netral.
*   **Klasifikasi & Evaluasi:** Data dibagi menjadi *training* dan *testing*. Model dilatih dan dievaluasi menggunakan *Confusion Matrix* untuk mengukur Akurasi, Presisi, *Recall*, F1-Score, dan AUC (*Area Under Curve*).

**6. Hasil Akhir**
*   **Sentimen Masyarakat:** Mayoritas sentimen adalah **Negatif (59.9%)**, diikuti Positif (30.4%) dan Netral (9.7%).
*   **Performa Model:**
    *   **Linear Support Vector Machine (SVM)** menjadi model terbaik.
    *   **Akurasi SVM:** 92.6%
    *   **AUC SVM:** 97%
    *   Sebagai perbandingan, *Random Forest Count Vectorizer* memiliki akurasi 92% dan *Random Forest TF-IDF* 91%.
*   **Temuan Kualitatif:** Kata kunci negatif sering muncul terkait "bocor", "lindung", "pidana", "sanksi", yang menunjukkan kekhawatiran masyarakat terhadap kebocoran data dan penegakan hukum.

**7. Gap / Kekurangan / Pengembangan yang Dapat Dilakukan**
*   **Rekomendasi/Pengembangan yang Disarankan Penulis:**
    *   Perlu adanya penguatan sumber daya manusia untuk pelindungan data.
    *   Penyusunan konten strategis yang menarik dan edukatif untuk meningkatkan kesadaran (*security awareness*) masyarakat.
    *   Optimasi layanan admin media sosial instansi terkait (respons 24 jam atau *automatic scheduled post*).
    *   Penerapan model ML untuk otomatisasi respon sentimen negatif.
*   **Gap (Tersirat):**
    *   Penelitian hanya terbatas pada satu platform media sosial (Twitter/X).
    *   Periode pengambilan data relatif singkat (Februari - April 2024), meskipun membahas konteks UU PDP tahun 2022.
    *   Fokus pada analisis teks, belum menggabungkan data non-teks atau platform lain.
