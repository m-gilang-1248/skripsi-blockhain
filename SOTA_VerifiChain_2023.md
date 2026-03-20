# State of the Art (SOTA) - Verifi-Chain Credentials Verifier

**1. Judul**
Verifi-Chain: A Credentials Verifier using Blockchain and IPFS

**2. Nama dan Tahun**
*   **Penulis:** Tasfia Rahman, Sumaiya Islam Mouno, Arunangshu Mojumder Raatul, Abul Kalam Al Azad, Nafees Mansoor
*   **Tahun:** 2023 (Berdasarkan cap arXiv:2307.05797v1 pada dokumen, meskipun nama file mencantumkan 2021)
*   **Publikasi:** arXiv (Computer Science - Cryptography and Security)

**3. Latar Belakang Masalah dan Data yang Digunakan**
*   **Latar Belakang:** Maraknya penyerahan sertifikat palsu oleh pelamar kerja, khususnya di Asia Tenggara, menghalangi kandidat yang memenuhi syarat untuk mendapatkan pekerjaan. Proses verifikasi manual dokumen akademik sangat memakan waktu, mahal, dan rentan terhadap penipuan (*fraud*). Sertifikat fisik juga berisiko hilang atau rusak. Dibutuhkan sistem yang tidak dapat dirusak (*tamper-proof*) dan efisien.
*   **Data:** Dokumen kredensial akademik (sertifikat/ijazah) digital yang diunggah oleh pelamar untuk diverifikasi dan disimpan.

**4. Metode / Algoritma**
*   **Teknologi Utama:** Integrasi Blockchain (Ethereum) dan *InterPlanetary File System* (IPFS).
*   **Konsep:** *Off-chain storage* (IPFS) untuk menyimpan file sertifikat berat, dan *On-chain storage* (Blockchain) hanya untuk menyimpan Hash unik (CID) dari file tersebut guna menjamin integritas.
*   **Tools & Framework:**
    *   **Blockchain:** Ethereum (menggunakan Ganache untuk jaringan lokal).
    *   **Smart Contract:** Solidity.
    *   **Frontend/Backend:** React.js, Node.js.
    *   **Wallet/Interface:** MetaMask, Web3.js.
    *   **Framework:** Truffle.

**5. Bagaimana Metode / Algoritma Digunakan**
*   **Alur Sistem:**
    1.  **Registrasi & Upload:** Pelamar mendaftar dan mengunggah kredensial ke sistem. Data sementara disimpan di database lokal.
    2.  **Verifikasi Admin:** Admin memverifikasi keaslian dokumen dengan institusi pendidikan terkait.
    3.  **Penyimpanan IPFS:** Setelah terverifikasi, dokumen diunggah ke IPFS. IPFS memecah file dan menghasilkan *hash code* unik (CID - *Content Identifier*).
    4.  **Pencatatan Blockchain:** CID dienkripsi dan disimpan di node Blockchain Ethereum melalui transaksi *smart contract* yang disetujui admin (via MetaMask).
    5.  **Verifikasi Pihak Ketiga:** Perusahaan/Perekrut dapat mencari pelamar menggunakan hash dan meminta akses untuk melihat sertifikat yang telah terverifikasi. Jika data di IPFS diubah, hash akan berubah dan tidak cocok dengan yang ada di Blockchain.

**6. Hasil Akhir**
*   **Prototipe Sistem:** Berhasil dikembangkan prototipe aplikasi berbasis web ("Verifi-Chain") yang menghubungkan antarmuka pengguna dengan jaringan blockchain lokal.
*   **Efisiensi Biaya:** Penggunaan IPFS sebagai penyimpanan perantara (*middleman storage*) berhasil menurunkan biaya penyimpanan data dibandingkan menyimpan seluruh data sertifikat langsung di dalam blok Blockchain (*on-chain*).
*   **Keamanan:** Sistem menjamin data tidak dapat diubah (*immutable*), transparan, dan aman dari pemalsuan.

**7. Gap / Kekurangan / Pengembangan yang Dapat Dilakukan**
*   **Gap/Kekurangan:**
    *   Sistem saat ini masih berupa prototipe yang diuji di jaringan lokal (Ganache), belum diuji skalabilitasnya pada jaringan publik (*Mainnet*) dengan beban transaksi nyata.
    *   Analisis performa mendalam terkait latensi dan *throughput* transaksi belum dibahas secara rinci dalam hasil pengujian.
*   **Pengembangan:**
    *   Eksplorasi integrasi dengan platform blockchain lain (interoperabilitas) selain Ethereum.
    *   Peningkatan fungsionalitas dan ketahanan (*robustness*) sistem untuk implementasi skala besar.
    *   Pengembangan fitur privasi yang lebih canggih bagi pemilik sertifikat dalam mengontrol akses data mereka.
