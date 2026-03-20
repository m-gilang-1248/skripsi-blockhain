# State of the Art (SOTA) - Blockchain Validasi Ijazah

**1. Judul**
Implementasi Blockchain sebagai Sistem Validasi dan Arsip Berkas (Sertifikasi dan Ijazah)

**2. Nama dan Tahun**
*   **Penulis:** Nur Hazbiy Shaffan, Primantara Hari Trisnawan, Ananda Fitra Diraja, Muhammad Yusuf Affandy
*   **Tahun:** 2025
*   **Publikasi:** Jurnal Informatika Universitas Pamulang, Vol. 10, No. 1, Maret 2025

**3. Latar Belakang Masalah dan Data yang Digunakan**
*   **Latar Belakang:** Maraknya pemalsuan dokumen akademik (ijazah dan sertifikat) baik fisik maupun digital menurunkan kredibilitas institusi pendidikan. Sistem verifikasi konvensional yang terpusat rentan terhadap manipulasi data dan *single point of failure*. Penelitian ini bertujuan membangun sistem validasi dan pengarsipan yang terdesentralisasi, transparan, dan *immutable* (tidak dapat diubah).
*   **Data:** Objek data yang digunakan adalah dokumen akademik digital (format PDF) seperti ijazah dan sertifikat yang diunggah ke sistem untuk divalidasi dan diarsipkan.

**4. Metode / Algoritma**
*   **Konsep Utama:** Integrasi Blockchain dengan *InterPlanetary File System* (IPFS) dan *Non-Fungible Token* (NFT/ERC-721).
*   **Platform Blockchain:** Consensys GoQuorum (jaringan blockchain privat/konsorsium berbasis Ethereum).
*   **Bahasa Pemrograman:** Solidity (Smart Contract).
*   **Tools & Infrastruktur:**
    *   **Penyimpanan:** IPFS (untuk menyimpan file fisik dokumen secara terdesentralisasi).
    *   **Wallet:** MetaMask (untuk otentikasi dan manajemen kunci).
    *   **Monitoring:** Blockscout (Blockchain Explorer).
    *   **Otomasi:** Ansible & Docker.

**5. Bagaimana Metode / Algoritma Digunakan**
*   **Arsitektur:** Menggunakan topologi jaringan dengan 4 *validator node* dan 1 *member node*.
*   **Alur Penerbitan Dokumen:**
    1.  **Verifikasi Akun:** Pihak penerbit (kampus) login menggunakan MetaMask. Smart contract memvalidasi *role* (hak akses) akun tersebut.
    2.  **Upload ke IPFS:** Dokumen PDF diunggah ke IPFS, menghasilkan *Content Identifier* (CID) yang unik (hash).
    3.  **Minting NFT:** Smart contract menjalankan fungsi `safeMintDocument()`. CID dari IPFS disimpan sebagai *metadata* dalam token NFT yang diterbitkan di blockchain.
    4.  **Pencatatan:** Transaksi dicatat di ledger blockchain yang tidak bisa diubah.
*   **Verifikasi:** Pihak verifikator dapat mengakses metadata NFT melalui fungsi `tokenURI()` untuk melihat CID dan membandingkannya dengan dokumen asli di IPFS, memastikan keaslian tanpa perantara.

**6. Hasil Akhir**
*   **Fungsionalitas:** Sistem berhasil menerbitkan dokumen digital sebagai NFT dan menyimpannya secara aman.
*   **Keamanan:** Mekanisme *Access Control* pada smart contract berfungsi baik; sistem menolak percobaan penerbitan dokumen oleh akun yang tidak memiliki hak akses (*unauthorized*).
*   **Transparansi:** Seluruh riwayat penerbitan dan metadata dokumen dapat dipantau secara *real-time* dan transparan melalui BlockExplorer.
*   **Integritas:** Data yang tersimpan (Hash CID) di blockchain terbukti tidak dapat dimanipulasi. Jika file diubah, Hash akan berbeda dan tidak valid.

**7. Gap / Kekurangan / Pengembangan yang Dapat Dilakukan**
*   **Gap/Tantangan:**
    *   Penggunaan *wallet* kripto (MetaMask) mungkin masih menjadi hambatan usabilitas (*barrier to entry*) bagi pengguna awam di institusi pendidikan.
    *   Fokus penelitian masih pada infrastruktur teknis; aspek regulasi hukum spesifik terkait kekuatan pembuktian NFT ijazah di Indonesia mungkin perlu kajian lebih lanjut (meskipun UU ITE disinggung).
*   **Pengembangan:**
    *   Integrasi langsung dengan Sistem Informasi Akademik (SIAKAD) yang sudah ada agar proses *minting* bisa otomatis saat wisuda.
    *   Pengembangan antarmuka verifikasi publik yang lebih *user-friendly* (tanpa perlu login wallet untuk sekadar memverifikasi).
