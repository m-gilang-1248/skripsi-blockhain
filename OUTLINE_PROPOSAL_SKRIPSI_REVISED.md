# OUTLINE PROPOSAL SKRIPSI
## PROGRAM STUDI TEKNIK INFORMATIKA

| | |
| :--- | :--- |
| **Nama** | M. GILANG M.W. SABDOKAFI |
| **NIM** | 221240001248 |
| **Judul Penelitian** | **Analisis Komparasi Efisiensi Biaya Gas dan Latensi Transaksi Smart Contract pada Validasi Sertifikat Digital Organisasi Mahasiswa: Studi Kasus Ethereum Sepolia dan Polygon Amoy Menggunakan Metode Batch Minting (ERC-721A)** |
| **Latar Belakang** | Sertifikat kegiatan yang diterbitkan oleh organisasi kemahasiswaan, seperti Himpunan Mahasiswa Program Studi Teknik Informatika (HMPSIF), memiliki peran vital sebagai bukti kompetensi non-akademik. Namun, kredibilitas dokumen digital ini rentan terhadap manipulasi grafis. Perlindungan terhadap integritas data privasi menjadi urgensi sebagaimana ditekankan oleh **Alvali Zaqi Taufan & Wahyu Wibowo (2024)**. Oleh karena itu, diperlukan mekanisme validasi yang *tamper-proof* dan transparan menggunakan teknologi Blockchain.<br><br>Secara global, **Rahman Tasfia et al. (2023)** merancang *Verifi-Chain* menggunakan kombinasi Blockchain dan IPFS. Di Indonesia, implementasi serupa dieksplorasi oleh **Hariani (Kasim) et al. (2025)** menggunakan jaringan lokal Ganache, dan **Nur Hazbiy Shaffan et al. (2025)** menggunakan jaringan privat *Consensys GoQuorum*. Meskipun sistem tersebut aman secara fungsional, mayoritas penelitian terdahulu terbatas pada lingkungan "steril" (Localhost/Private Network) yang tidak memiliki fluktuasi biaya gas dan latensi jaringan yang dinamis.<br><br>Kesenjangan (*gap*) yang muncul adalah minimnya analisis pada **jaringan publik (Public Testnet)** yang memiliki karakteristik trafik riil. Bagi organisasi non-profit seperti HMPSIF, penggunaan Blockchain Layer-1 sering terhambat biaya transaksi yang mahal. Penelitian ini hadir untuk memberikan solusi melalui analisis komparasi performa antara **Ethereum Sepolia (Layer-1)** dan **Polygon Amoy (Layer-2)** menggunakan 280 data sertifikat riil. Kebaruan (*novelty*) penelitian ini terletak pada pengujian di jaringan publik dengan menerapkan standar **ERC-721A** untuk mengoptimalkan metode **Batch Minting**, guna mencapai efisiensi biaya dan kecepatan validasi yang maksimal. |
| **Rumusan Masalah** | 1. Bagaimana perbandingan biaya transaksi (*gas fee*) yang dibutuhkan untuk memvalidasi 280 sertifikat digital antara jaringan Ethereum Sepolia dan Polygon Amoy menggunakan metode *Batch Minting* (ERC-721A)?<br>2. Bagaimana perbandingan latensi waktu (*confirmation time*) transaksi antara metode *Single Minting* dan *Batch Minting* pada kondisi trafik jaringan publik tersebut?<br>3. Apakah penerapan metode *Batch Minting* (ERC-721A) pada jaringan Layer-2 dapat menjadi solusi efisiensi biaya yang signifikan bagi organisasi mahasiswa dibandingkan standar ERC-721 konvensional? |
| **Referensi Utama** | **Windra Swastika, Hermawan Wira Santoso, & Oesman Hendra Kelana. (2022).** *"Rancang Bangun Website Akademik Dengan Penyimpanan Sertifikat Digital Menggunakan Teknologi Blockchain"*. Jurnal Teknologi Informasi dan Ilmu Komputer (JTIIK).<br><br>Penelitian tersebut membuktikan secara kuantitatif bahwa blockchain mampu memproses transaksi skala institusi di jaringan lokal. Namun, penelitian Swastika et al. masih menggunakan standar pencetakan per unit di lingkungan Geth lokal. Penelitian saya akan memperluas temuan ini dengan menguji aspek biaya operasional riil di **jaringan publik** dan mengoptimalkan kontrak pintar menggunakan standar **ERC-721A** untuk menekan biaya gas secara drastis pada pengiriman massal. |

### Daftar Pustaka

1. **Rahman, T., et al. (2023).** *Verifi-chain: a credentials verifier using blockchain and IPFS*. International Conference on Information, Communication and Computing Technology.
2. **Hariani, Ibrahim, A. M., & Ahmad, Z. F. (2025).** *IMPLEMENTASI TEKNOLOGI BLOCKCHAIN PADA PENGELOLAAN DATA AKADEMIK*. Jurnal INSTEK (Informatika Sains dan Teknologi), 10(1).
3. **Swastika, W., et al. (2022).** *Rancang bangun website akademik dengan penyimpanan sertifikat digital menggunakan teknologi blockchain*. Jurnal Teknologi Informasi Dan Ilmu Komputer, 9(1).
4. **Nur Hazbiy Shaffan, et al. (2025).** *Implementasi Blockchain sebagai Sistem Validasi dan Arsip Berkas (Sertifikasi dan Ijazah)*. Jurnal Informatika Universitas Pamulang, 10(1).
5. **Taufan, A. Z., & Wibowo, W. (2024).** *Analisis Sentimen Terkait Persepsi Keamanan Data Informasi Dan Privasi di Indonesia*. Jurnal Informatika Teknologi dan Sains (Jinteks), 6(3).

***

**Jepara, 17 Januari 2026**
**Pengusul:**

**(M. GILANG M.W. SABDOKAFI)**
**NIM: 221240001248**
