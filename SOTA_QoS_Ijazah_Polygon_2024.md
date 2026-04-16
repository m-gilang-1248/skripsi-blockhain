# State of the Art (SOTA) - Analisis QoS Sistem Ijazah Blockchain (Polygon)

**1. Judul**
Quality of Service Diploma Recording System Using Smart Contracts and NFT Polygon Network on Layer-2 Ethereum Blockchain

**2. Nama dan Tahun**
*   **Penulis:** Rizky Rachman Judhie Putra, Muhamad Nursalman, Fawwaz Kautsar
*   **Tahun:** 2024
*   **Publikasi:** Jurnal Teknik Informatika (JUTIF), Vol. 5, No. 6, Desember 2024

**3. Latar Belakang Masalah dan Data yang Digunakan**
*   **Latar Belakang:** Maraknya pemalsuan ijazah (pelanggaran HAKI) dan kelemahan sistem verifikasi terpusat di Indonesia (SIVIL/PIN) yang rentan terhadap peretasan seperti SQL Injection. Penggunaan Blockchain Layer-1 (Ethereum) secara langsung memiliki kendala biaya transaksi (*gas fee*) yang sangat tinggi dan masalah skalabilitas.
*   **Data:** 35 buah sampel data ijazah mahasiswa yang digunakan untuk pengujian *minting* NFT dan pengukuran performa jaringan (QoS).

**4. Metode / Algoritma**
*   **Konsep Utama:** Implementasi ijazah sebagai *Soulbound Tokens* (SBTs) — varian NFT yang tidak dapat dipindahtangankan — menggunakan jaringan **Polygon (Layer-2)** untuk efisiensi biaya.
*   **Platform Blockchain:** Jaringan Polygon Mainnet (skalabilitas L2 Ethereum).
*   **Penyimpanan Terdesentralisasi:** IPFS (*InterPlanetary File System*) untuk menyimpan file gambar ijazah dan metadata JSON.
*   **Tools & Infrastruktur:**
    *   **Smart Contract:** Solidity (ERC-721/SBT).
    *   **Development Framework:** Truffle & Ganache.
    *   **API Service:** Alchemy (Node Provider) dan Infura (IPFS Gateway).
    *   **Wallet:** MetaMask.
    *   **Analisis QoS:** Wireshark (untuk mengukur *throughput*, *packet loss*, dan *latency*).

**5. Bagaimana Metode / Algoritma Digunakan**
*   **Alur Penelitian (Waterfall Model):** Dimulai dari analisis kebutuhan, desain sistem, pengembangan, hingga pengujian.
*   **Alur Penerbitan Ijazah (Technical Flow):**
    1.  **Input Data:** Admin menginput data mahasiswa melalui DApp.
    2.  **Hasing:** *Secret Private Key* mahasiswa dibuat menggunakan algoritma SHA-256 sebagai identitas unik.
    3.  **Upload IPFS:** File ijazah diunggah ke IPFS untuk mendapatkan CID (*Content Identifier*).
    4.  **Metadata NFT:** Data ijazah dan CID IPFS disusun dalam format JSON, lalu diunggah kembali ke IPFS.
    5.  **Minting di Polygon:** Smart contract merekam CID metadata ke dalam ledger Polygon. Biaya dibayar menggunakan koin MATIC.
    6.  **Verifikasi:** Ijazah yang telah menjadi NFT dapat dilacak melalui Polygonscan atau diimpor ke MetaMask mahasiswa menggunakan *private key* mereka.

**6. Hasil Akhir**
*   **Efisiensi Biaya:** Biaya transaksi di jaringan Polygon hanya menghabiskan **2,26%** dari biaya di jaringan Ethereum (jauh lebih murah).
*   **Performa QoS (Quality of Service):**
    *   **Throughput:** 48,6 - 49,6 Kbps (Sangat Baik menurut standar TIPHON).
    *   **Packet Loss:** **0%** (Sangat Baik), mengungguli Ethereum yang memiliki *packet loss* 0,45%.
    *   **Latency:** 42,07 - 44,13 ms (Sangat Baik, di bawah 150 ms).
*   **Integritas:** Penggunaan NFT SBT memastikan ijazah tidak dapat dijual atau dipindahtangankan, menjaga fungsi ijazah sebagai kredensial pribadi yang permanen.

**7. Gap / Kekurangan / Pengembangan yang Dapat Dilakukan**
*   **Gap/Tantangan:** 
    *   *Throughput* Polygon dalam penelitian ini (48-49 Kbps) masih jauh di bawah Ethereum (486 Kbps), meskipun masih dalam kategori sangat baik. Hal ini dipengaruhi oleh jumlah *validator node* yang lebih sedikit (105 vs 7.356 pada saat penelitian).
    *   Ketergantungan pada layanan pihak ketiga seperti Alchemy dan Infura (sentralisasi di level API).
*   **Pengembangan:**
    *   Optimasi kode smart contract untuk mengurangi *gas usage* lebih lanjut.
    *   Integrasi *Digital Rights Management* (DRM) untuk perlindungan konten digital yang lebih ketat.
    *   Peningkatan antarmuka pengguna (UX) agar pihak perusahaan/verifikator dapat melakukan validasi dengan lebih instan tanpa kendala teknis blockchain.
