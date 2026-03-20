# State of the Art (SOTA) - Implementasi Blockchain Data Akademik

**1. Judul**
IMPLEMENTASI TEKNOLOGI BLOCKCHAIN PADA PENGELOLAAN DATA AKADEMIK

**2. Nama dan Tahun**
*   **Penulis:** Hariani, Ahmad Muyassar Ibrahim, Zul Fadli Ahmad
*   **Tahun:** 2025
*   **Publikasi:** Jurnal INSTEK (Informatika Sains dan Teknologi), Vol. 10, No. 1, April 2025

**3. Latar Belakang Masalah dan Data yang Digunakan**
*   **Latar Belakang:** Pengelolaan data akademik, khususnya transkrip nilai, menghadapi tantangan risiko pemalsuan, manipulasi data, serta kurangnya transparansi dan efisiensi. Sistem tradisional yang terpusat rawan terhadap peretasan dan perubahan data tanpa izin. Tujuan penelitian ini adalah merancang sistem pengelolaan transkrip nilai berbasis blockchain untuk meningkatkan keamanan dan integritas data.
*   **Data:** Studi kasus dilakukan pada Program Studi Teknik Informatika, UIN Alauddin Makassar. Data yang digunakan dalam pengujian adalah data simulasi transkrip nilai mahasiswa (ID, Nama, Jurusan, Mata Kuliah, Nilai) sebanyak 10 data uji coba input.

**4. Metode / Algoritma**
*   **Metode Pengembangan:** SDLC (*Systems Development Life Cycle*) model *Waterfall* (Analisis, Desain, Implementasi, Pengujian, Pemeliharaan).
*   **Teknologi Utama:**
    *   **Blockchain:** Ethereum (menggunakan jaringan lokal Ganache).
    *   **Smart Contract:** Bahasa pemrograman Solidity.
    *   **Tools:** Truffle (framework), MetaMask (wallet), Web3.js (library interaksi), React.js (Frontend), Node.js.

**5. Bagaimana Metode / Algoritma Digunakan**
*   **Arsitektur Sistem:** Terdiri dari 3 lapisan:
    1.  *Frontend Layer:* Antarmuka pengguna berbasis React dan Bootstrap.
    2.  *Backend Layer:* *Node* blockchain lokal (Ganache) dan *Smart Contract* (Solidity) yang menyimpan logika bisnis dan data.
    3.  *Communication Layer:* Menggunakan Web3.js untuk menghubungkan frontend dengan smart contract di blockchain.
*   **Alur Kerja:**
    *   Dosen/Operator menginput nilai melalui frontend.
    *   Transaksi diverifikasi dan dicatat dalam blok oleh *Smart Contract* (`Transcript.sol`) di jaringan Ganache.
    *   MetaMask digunakan untuk otorisasi transaksi (gas fee simulasi).
    *   Data tersimpan secara *immutable* (tidak bisa diubah) dan terdesentralisasi.

**6. Hasil Akhir**
*   **Keberhasilan Fungsional:** Pengujian *Black Box* menunjukkan tingkat keberhasilan 100% pada 10 skenario uji coba (input data mahasiswa, tambah nilai, lihat data).
*   **Keamanan & Integritas:** Sistem berhasil mencatat data transkrip yang aman, transparan, dan tidak dapat dimanipulasi (*tamper-proof*).
*   **Efisiensi:** Mempercepat proses verifikasi nilai secara *real-time* dan memudahkan akses bagi mahasiswa dan dosen.

**7. Gap / Kekurangan / Pengembangan yang Dapat Dilakukan**
*   **Keterbatasan (Gap):**
    *   Implementasi masih terbatas pada jaringan lokal (Ganache) sebagai simulasi, belum di-deploy ke jaringan publik (Mainnet) atau *Testnet* publik yang sebenarnya.
    *   Masalah biaya transaksi (*gas fee*) pada jaringan Ethereum publik belum dibahas secara mendalam sebagai kendala implementasi riil.
*   **Tantangan:** Skalabilitas jaringan blockchain dan adopsi teknologi baru oleh institusi pendidikan.
*   **Pengembangan:** Perlu pengembangan lebih lanjut untuk penerapan di jaringan publik atau *private/consortium blockchain* antar universitas untuk standar industri yang lebih luas.
