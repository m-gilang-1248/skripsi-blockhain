# Roadmap & Kebutuhan Implementasi Blockchain (Skripsi)

Dokumen ini berisi panduan teknis untuk mengimplementasikan sistem validasi ijazah berbasis Blockchain (Polygon/Ethereum) yang dioptimalkan untuk laptop spesifikasi menengah (RAM 8GB).

---

## 🛠️ Bahan-Bahan (Tech Stack)

### 1. Lingkungan Pengembangan (Local)
*   **Node.js (v18+):** Mesin utama untuk menjalankan framework JavaScript.
*   **VS Code:** Editor kode (instal ekstensi: *Solidity by Juan Blanco*).
*   **Hardhat:** Framework blockchain paling populer dan ringan (CLI-based). Alternatif: Truffle.
*   **MetaMask:** Ekstensi browser untuk interaksi dengan DApp.

### 2. Bahasa Pemrograman
*   **Solidity:** Untuk menulis Smart Contract.
*   **JavaScript/TypeScript:** Untuk script pengujian (testing) dan integrasi frontend.

### 3. Layanan Pihak Ketiga (Cloud-based)
*   **Alchemy / Infura:** Sebagai "node gateway". Anda tidak perlu menjalankan blockchain di laptop, cukup hubungkan ke API mereka.
*   **Pinata / NFT.Storage:** Layanan IPFS untuk menyimpan file PDF ijazah secara terdesentralisasi.
*   **Polygonscan / Etherscan:** Untuk memantau transaksi secara publik.

---

## 🚀 Roadmap Implementasi (6 Tahap)

### Tahap 1: Setup Environment
1.  Instal Node.js.
2.  Buat folder proyek: `mkdir ijazah-blockchain && cd ijazah-blockchain`.
3.  Inisialisasi Hardhat: `npx hardhat init`.
4.  Daftar akun di **Alchemy** (Gratis) untuk mendapatkan kunci API Polygon Amoy (Testnet).

### Tahap 2: Penulisan Smart Contract (Solidity)
1.  Gunakan standar **ERC-721 (NFT)** atau **Soulbound Token (SBT)**.
2.  Fungsi utama:
    *   `mintDiploma()`: Menerbitkan ijazah baru (hanya Admin).
    *   `getDiplomaMetadata()`: Mengambil data ijazah berdasarkan ID.
    *   `revokeDiploma()`: Membatalkan ijazah jika terjadi kesalahan (opsional).

### Tahap 3: Local Testing & Debugging
1.  Jalankan blockchain lokal di terminal: `npx hardhat node`.
2.  Tulis script test di folder `test/` untuk memastikan fungsi *minting* berhasil.
3.  Deploy kontrak ke jaringan lokal: `npx hardhat run scripts/deploy.js --network localhost`.

### Tahap 4: Integrasi IPFS
1.  Pelajari alur: **Upload Ijazah (PDF) -> Dapatkan Hash (CID) -> Simpan CID di Smart Contract**.
2.  Gunakan library `pinata-sdk` untuk memudahkan upload dari DApp.

### Tahap 5: Pengembangan Frontend (DApp)
1.  Gunakan **React.js** atau **Next.js**.
2.  Gunakan library **Ethers.js** untuk menghubungkan website dengan MetaMask.
3.  Buat dua halaman:
    *   **Halaman Admin:** Form input data ijazah & tombol "Mint NFT".
    *   **Halaman Publik:** Kolom pencarian/verifikasi ijazah berdasarkan ID/Hash.

### Tahap 6: Deployment ke Testnet (Polygon Amoy)
1.  Ambil koin MATIC gratis dari *Faucet*.
2.  Ubah konfigurasi `hardhat.config.js` ke jaringan Polygon Amoy.
3.  Deploy kontrak asli ke internet: `npx hardhat run scripts/deploy.js --network amoy`.

---

## 💡 Tips Optimalisasi (Untuk RAM 8GB)
*   **Tutup aplikasi tidak perlu:** Saat menjalankan `npm start` (Frontend) dan `hardhat` bersamaan, RAM 8GB akan sangat mepet. Tutup Spotify, WhatsApp Desktop, dll.
*   **Gunakan Console.log di Solidity:** Hardhat mendukung `console.log` di dalam Smart Contract untuk memudahkan debugging tanpa harus membuka browser terus-menerus.
*   **Versi Node.js:** Pastikan menggunakan versi LTS (Long Term Support) agar tidak terjadi konflik library yang menyebabkan crash.

---

**Langkah Selanjutnya:**
Apakah Anda ingin saya buatkan draf kode **Smart Contract (Solidity)** sederhana untuk "Sistem Ijazah" sebagai titik awal pengerjaan?
