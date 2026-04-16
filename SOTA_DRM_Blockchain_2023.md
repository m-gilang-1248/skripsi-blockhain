# State of the Art (SOTA) - DRM Blockchain 2023

**1. Judul**
THE ROLE OF BLOCKCHAIN TO SOLVE PROBLEMS OF DIGITAL RIGHT MANAGEMENT (DRM) / PERANAN BLOCKCHAIN UNTUK MENGATASI KEKURANGAN TEKNOLOGI PENGELOLA HAK CIPTA DIGITAL (DRM)

**2. Nama dan Tahun**
*   **Penulis:** Jehan Afwazi Ahmad, Teduh Dirgahayu
*   **Tahun:** 2023
*   **Publikasi:** Jurnal Teknik Informatika (JUTIF), Vol. 4, No. 1, Februari 2023

**3. Latar Belakang Masalah dan Data yang Digunakan**
*   **Latar Belakang:** Peningkatan penggunaan konten digital memicu maraknya pelanggaran hak cipta. Teknologi *Digital Right Management* (DRM) konvensional memiliki kelemahan kritis: ketidakmampuan melacak kebocoran data, sulitnya autentikasi jika sumber informasi rusak/dimanipulasi, ketiadaan fitur pemindahan hak kepemilikan, dan model sentralisasi yang memicu masalah kepercayaan (*trust issue*).
*   **Data:** Penelitian ini menggunakan metode *Narrative Literature Review* dengan mengumpulkan dan menganalisis sumber berupa makalah, artikel, dan berita terkait DRM dan blockchain dalam kurun waktu lima tahun terakhir (2017–2022).

**4. Metode / Algoritma**
*   **Arsitektur Teknologi:**
    *   *Blockchain:* Sebagai buku besar terdesentralisasi yang bersifat *immutable* dan *tamper-proof*.
    *   *Smart Contract:* Untuk otomatisasi perjanjian antara pihak-pihak terlibat (pengaturan kontrak otomatis).
    *   *IPFS (InterPlanetary File System):* Digunakan sebagai media penyimpanan konten digital yang terdesentralisasi untuk mengatasi keterbatasan kapasitas blok pada blockchain.
    *   *Kriptografi Kunci Publik:* Penggunaan *Public Key* (PK) dan *Private Key* (SK) untuk enkripsi dan autentikasi.
    *   *Watermarking:* Teknik penyisipan identitas pada konten digital untuk pembuktian kepemilikan.

**5. Bagaimana Metode / Algoritma Digunakan**
*   **Alur Publikasi:** Penulis mengunggah konten ke IPFS, lalu nilai *hash* dari IPFS disimpan ke dalam *smart contract* di jaringan blockchain.
*   **Alur Permintaan Salinan:** Konsumen mengirimkan permintaan salinan melalui *smart contract* dengan menyertakan identitas dan *Public Key*.
*   **Mekanisme Transaksi:** Penulis memberikan *watermark* pada konten, mengenkripsi *hash* file menggunakan *Public Key* konsumen, dan menandatanganinya secara digital. Data tersebut kemudian dikirim ke *smart contract* untuk disimpan.
*   **Akses Konten:** Konsumen mengunduh konten dari IPFS menggunakan *hash* yang telah didekripsi dengan *Private Key* miliknya, memastikan hanya pihak sah yang dapat mengakses file tersebut.

**6. Hasil Akhir**
*   **Solusi Keamanan:** Blockchain berhasil mengatasi 6 masalah utama DRM: menjamin keamanan distribusi, memastikan originalitas, menyediakan transaksi *non-repudiation*, mendukung identifikasi pencipta, melacak kebocoran data, serta memungkinkan pembatasan unduh dan pemindahan hak kepemilikan.
*   **Integritas Data:** Penggunaan *hash* yang saling terhubung antar blok memastikan data tidak dapat dimanipulasi tanpa merusak rantai blockchain, sehingga keaslian dokumen digital terjamin.
*   **Desentralisasi:** Menghilangkan ketergantungan pada pihak ketiga (perantara), sehingga meningkatkan transparansi pembagian royalti antara penulis, penerbit, dan konsumen.

**7. Gap / Kekurangan / Pengembangan yang Dapat Dilakukan**
*   **Gap/Kekurangan:**
    *   Penggunaan konsensus *Proof of Work* (PoW) pada beberapa implementasi blockchain masih memakan konsumsi energi yang sangat besar (disarankan beralih ke *Proof of Stake*).
    *   Beberapa penelitian terdahulu yang diulas masih terbatas pada sistem satu pengguna (*single user*) atau masih melakukan proses perjanjian di luar kontrak (*off-chain*).
*   **Pengembangan:**
    *   Penerapan konsensus *Proof of Stake* (PoS) untuk efisiensi energi.
    *   Pengembangan sistem yang mampu mengakomodasi pembagian royalti secara otomatis dan adil antara *author* dan *publisher* langsung di dalam *smart contract*.
    *   Implementasi fitur pembatasan akses yang lebih dinamis untuk skema peminjaman konten digital.
