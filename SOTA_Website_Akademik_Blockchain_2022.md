# State of the Art (SOTA) - Website Akademik Blockchain 2022

**1. Judul**
RANCANG BANGUN WEBSITE AKADEMIK DENGAN PENYIMPANAN SERTIFIKAT DIGITAL MENGGUNAKAN TEKNOLOGI BLOCKCHAIN

**2. Nama dan Tahun**
*   **Penulis:** Windra Swastika, Hermawan Wira Santoso, Oesman Hendra Kelana
*   **Tahun:** 2022
*   **Publikasi:** Jurnal Teknologi Informasi dan Ilmu Komputer (JTIIK), Vol. 9, No. 1, Februari 2022

**3. Latar Belakang Masalah dan Data yang Digunakan**
*   **Latar Belakang:** Sertifikat fisik maupun digital konvensional memiliki risiko kerusakan, kehilangan, dan pemalsuan yang dapat mempengaruhi kredibilitas lembaga penerbit. Penyimpanan terpusat (sentralisasi) juga memiliki risiko keamanan dan manipulasi data. Penelitian ini bertujuan menerapkan teknologi blockchain pada platform belajar *online* untuk menyimpan sertifikat digital secara aman, permanen, dan transparan.
*   **Data:** Data yang digunakan adalah data simulasi kelas akademik (diambil dari Firebase Firestore) dan data transaksi penerbitan sertifikat yang diuji coba pada sistem (sampel pengujian 200 transaksi).

**4. Metode / Algoritma**
*   **Platform Blockchain:** Ethereum (menggunakan implementasi Geth / Go Ethereum).
*   **Konsensus:** *Proof of Work* (PoW).
*   **Smart Contract:** Bahasa pemrograman Solidity.
*   **Arsitektur Sistem:**
    *   *Blockchain Network:* Jaringan *Peer-to-Peer* privat menggunakan Geth.
    *   *Backend/Tools:* Truffle (untuk migrasi kontrak), Node.js (lite-server), Firebase Firestore (untuk data non-krusial seperti detail kelas).
    *   *Frontend:* Web application (Bootstrap 4).
    *   *Wallet:* MetaMask (jembatan antara browser dan blockchain).

**5. Bagaimana Metode / Algoritma Digunakan**
*   **Alur Penerbitan:** Pengguna mengikuti kelas *online*, dan setelah lulus, sistem memanggil fungsi pada *smart contract* untuk menerbitkan sertifikat.
*   **Transaksi:** Pengguna menandatangani transaksi menggunakan *Private Key* di MetaMask (membayar *gas fee* dengan Ether).
*   **Penyimpanan:** Data sertifikat (pemilik, tanggal, ID unik) disimpan dalam struktur data `map` di dalam *smart contract* yang tersebar di seluruh *node*.
*   **Verifikasi:** Fitur cek sertifikat memanggil fungsi di *smart contract* untuk mencocokkan ID sertifikat dengan data di blockchain. Jika cocok, data valid ditampilkan; jika tidak, dianggap tidak valid/palsu.

**6. Hasil Akhir**
*   **Keamanan:** Sistem berhasil mencegah manipulasi; *smart contract* tidak dapat diganti oleh pihak tidak berwenang.
*   **Reliabilitas:** Pengujian menunjukkan sistem mampu memproses **200 transaksi dalam waktu ±8 detik**.
*   **Skalabilitas (Estimasi):** Untuk menyimpan 10 juta blok (dengan asumsi rata-rata 10 transaksi per blok), sebuah *node/miner* membutuhkan kapasitas penyimpanan sekitar **22,6 GB**.
*   **Fungsionalitas:** Integrasi MetaMask berjalan baik untuk menangani pembayaran dan otentikasi transaksi.

**7. Gap / Kekurangan / Pengembangan yang Dapat Dilakukan**
*   **Gap/Kekurangan:**
    *   Penggunaan konsensus *Proof of Work* (PoW) membutuhkan sumber daya komputasi (CPU) yang besar.
    *   Pengujian masih dilakukan pada jaringan lokal; tantangan koneksi dan sinkronisasi pada jaringan publik yang lebih luas belum sepenuhnya teruji.
*   **Pengembangan:**
    *   Peningkatan reliabilitas jaringan dengan menggunakan *boot node* yang di-*hosting* pada layanan web (*web service*) agar sinkronisasi *node* baru lebih cepat.
    *   Penerapan pengujian otomatis (*automated testing*) untuk simulasi jumlah transaksi dan data yang jauh lebih besar guna menguji batas performa sistem secara ekstrem.
