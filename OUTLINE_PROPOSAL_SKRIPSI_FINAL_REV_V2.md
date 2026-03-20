**OUTLINE PROPOSAL SKRIPSI**

**PROGRAM STUDI TEKNIK INFORMATIKA**

**Nama**                : [Nama Anda]
**NIM**                 : [NIM Anda]
**Pembimbing**          : [Nama Pembimbing]

**Judul Penelitian**    : **Analisis Komparasi Efisiensi Biaya Gas dan Latensi Transaksi Smart Contract pada Validasi Sertifikat Digital Organisasi Mahasiswa: Studi Kasus Ethereum Sepolia dan Polygon Amoy**

**Latar Belakang**      :

Sertifikat kegiatan yang diterbitkan oleh organisasi kemahasiswaan, seperti Himpunan Mahasiswa Program Studi Teknik Informatika (HMPSIF), memiliki peran vital sebagai bukti kompetensi non-akademik bagi mahasiswa. Namun, kredibilitas dokumen ini seringkali dipertanyakan oleh pihak industri atau eksternal karena rentannya format digital terhadap manipulasi, seperti penyuntingan nama atau predikat menggunakan perangkat lunak grafis. Di era digital yang menuntut keamanan informasi tinggi, sebagaimana ditekankan oleh **Alvali Zaqi Taufan & Wahyu Wibowo (2024)**, perlindungan terhadap integritas data privasi menjadi urgensi yang tidak bisa ditawar. Oleh karena itu, diperlukan mekanisme validasi yang *tamper-proof* (tahan perusakan) dan transparan untuk mengembalikan kepercayaan publik terhadap sertifikat organisasi mahasiswa.

Teknologi Blockchain menawarkan solusi ideal untuk permasalahan ini melalui sifat desentralisasi dan *immutability*-nya. Secara global, pendekatan ini telah divalidasi oleh **Rahman Tasfia et al. (2023)** yang merancang sistem *Verifi-Chain* menggunakan kombinasi Blockchain dan IPFS untuk mencegah kandidat kerja menggunakan kredensial palsu. Di Indonesia, implementasi serupa telah dieksplorasi, salah satunya oleh **Hariani et al. (2025)** yang membangun sistem pengelolaan data akademik transkrip nilai menggunakan jaringan lokal. Meskipun sistem tersebut terbukti aman secara fungsional, mayoritas penelitian terdahulu masih terbatas pada implementasi di jaringan lokal (*Localhost/Ganache*) atau jaringan privat (*Private Network*) seperti yang dilakukan oleh **Nur Hazbiy Shaffan et al. (2025)**.

Kesenjangan (*gap*) yang muncul adalah minimnya analisis mengenai implementasi di jaringan publik (*Mainnet/Testnet*) yang sebenarnya, terutama terkait tantangan biaya operasional atau *Gas Fee*. Bagi organisasi nirlaba seperti HMPSIF, penggunaan jaringan Blockchain Layer-1 seperti Ethereum seringkali terhambat oleh biaya transaksi yang fluktuatif dan mahal, serta latensi yang lambat saat jaringan padat. Sementara itu, solusi jaringan privat membutuhkan infrastruktur server mandiri yang kompleks perawatannya. Belum banyak penelitian yang secara spesifik membandingkan efisiensi antara jaringan Layer-1 dengan solusi Layer-2 (seperti Polygon) menggunakan data riil organisasi mahasiswa dalam jumlah masif.

Berdasarkan permasalahan tersebut, penelitian ini mengajukan analisis komparasi performa antara jaringan Ethereum Sepolia (representasi Layer-1) dan Polygon Amoy (representasi Layer-2) menggunakan 280 data sertifikat riil dari HMPSIF. Penelitian ini tidak hanya akan menguji fungsionalitas, tetapi fokus mengukur metrik efisiensi biaya (*Gas Used*) dan kecepatan (*Latency*) dengan membandingkan metode pencetakan tunggal (*Single Minting*) dan pencetakan massal (*Batch Minting*). Hasil penelitian ini diharapkan dapat memberikan rekomendasi solusi validasi sertifikat yang paling ekonomis dan cepat untuk diterapkan oleh organisasi kemahasiswaan.

**Rumusan Masalah**     :
1.  Bagaimana perbandingan biaya transaksi (*gas fee*) yang dibutuhkan untuk memvalidasi 280 sertifikat digital antara jaringan Ethereum Sepolia dan Polygon Amoy?
2.  Bagaimana perbandingan latensi waktu (*confirmation time*) transaksi antara metode *Single Minting* dan *Batch Minting* pada kedua jaringan tersebut?
3.  Apakah penerapan metode *Batch Minting* pada jaringan Layer-2 dapat menjadi solusi efisiensi biaya yang signifikan bagi organisasi mahasiswa?

**Referensi/Pustaka Utama** :

**Windra Swastika, Hermawan Wira Santoso, & Oesman Hendra Kelana. (2022).** *"Rancang Bangun Website Akademik Dengan Penyimpanan Sertifikat Digital Menggunakan Teknologi Blockchain"*. Jurnal Teknologi Informasi dan Ilmu Komputer (JTIIK), Vol. 9, No. 1.

*   **Latar Belakang Penelitian:**
    Penelitian ini dilatarbelakangi oleh maraknya platform belajar *online* yang menerbitkan sertifikat digital, namun masih menggunakan penyimpanan terpusat yang rentan terhadap risiko kehilangan data, kerusakan server, dan pemalsuan dokumen. Peneliti menawarkan solusi penyimpanan terdesentralisasi menggunakan blockchain Ethereum untuk menjamin keaslian sertifikat dan memudahkan verifikasi tanpa pihak ketiga.

*   **Data dan Alur Penelitian:**
    Penelitian menggunakan data simulasi kelas akademik yang diambil dari *Firebase Firestore* dan data transaksi penerbitan sertifikat yang diuji coba pada jaringan lokal. Alur penelitian dimulai dari mahasiswa menyelesaikan kelas *online*, kemudian sistem secara otomatis memanggil fungsi *Smart Contract* (ditulis dalam Solidity) untuk menerbitkan sertifikat. Transaksi penerbitan ini divalidasi oleh *miner* (dalam simulasi Geth) dan dicatat dalam blok. Pengguna (mahasiswa) menggunakan dompet digital *MetaMask* untuk menandatangani transaksi dan membayar biaya gas (dalam lingkungan tes).

*   **Hasil dan Manfaat yang Dicapai:**
    Hasil pengujian reliabilitas menunjukkan bahwa sistem mampu memproses **200 transaksi secara bersamaan dalam waktu kurang lebih 8 detik**, yang membuktikan bahwa blockchain memiliki performa yang memadai untuk menangani volume penerbitan sertifikat skala institusi. Selain itu, peneliti juga melakukan estimasi skalabilitas, di mana untuk menyimpan 10 juta blok data transaksi, sebuah *node* hanya membutuhkan kapasitas penyimpanan sekitar **22,6 GB**. Temuan ini menjadi landasan empiris bagi proposal penelitian saya, karena membuktikan secara kuantitatif bahwa implementasi validasi sertifikat di blockchain adalah solusi yang *feasible* (layak) secara teknis, berkinerja tinggi, dan efisien dalam penggunaan sumber daya penyimpanan. Penelitian saya akan memperluas temuan ini dengan menguji aspek biaya (*cost-efficiency*) pada jaringan publik.
