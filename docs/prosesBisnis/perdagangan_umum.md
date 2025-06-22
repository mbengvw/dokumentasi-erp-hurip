# Proses Bisnis: Perdagangan Umum
## 1. Pendahuluan
Sektor Perdagangan Umum di perusahaan ini berfokus pada penjualan barang dagangan kepada pelanggan. Proses bisnis dimulai dari input Sales Order (SO) oleh staf sektor, kemudian disetujui oleh pimpinan sektor, dan berlanjut hingga pembuatan Work Order (WO) dan pengelolaan anggaran. Alur proses bisnis ini memastikan bahwa setiap transaksi tercatat dengan baik dan terkelola dengan tepat.

## 2. Alur Proses Bisnis Perdagangan Umum
**A. Pencatatan Sales Order (SO)**
Staf sektor menerima pesanan dari pelanggan, yang kemudian dicatat sebagai Sales Order (SO). Sales Order ini berisi detail produk yang dipesan, jumlah barang, harga, dan informasi pelanggan.

*Langkah-langkah*:

- Staf sektor menerima pesanan dari pelanggan.
- Data pesanan yang diterima dicatat dalam formulir atau dokumen Sales Order.  

>Data yang dicatat: Nama pelanggan, Produk yang dipesan, Jumlah produk yang dipesan, Harga produk, Alamat pengiriman, Tanggal pengiriman yang diinginkan

- Sales Order yang telah dicatat diserahkan untuk diproses lebih lanjut.

**B. Persetujuan Sales Order oleh Pimpinan Sektor**
Setelah Sales Order dicatat, Pimpinan Sektor akan memeriksa dan memberikan persetujuan terhadap pesanan yang diajukan. Proses ini memastikan bahwa pesanan sesuai dengan kebijakan perusahaan dan stok tersedia.

*Langkah-langkah:*

- Pimpinan sektor menerima Sales Order dari staf sektor.
Pimpinan sektor memeriksa informasi dalam Sales Order, seperti ketersediaan barang dan harga.
- Pimpinan sektor memberikan persetujuan atau penolakan terhadap Sales Order.
- Jika disetujui: Pesanan dilanjutkan ke tahap pembuatan Work Order (WO).
- Jika ditolak: Staf sektor diminta untuk melakukan revisi atau pembatalan pesanan.

**C. Pembuatan Work Order (WO)**
Setelah Sales Order disetujui, dibuat Work Order (WO) sebagai instruksi untuk pengolahan dan pengiriman barang sesuai dengan pesanan yang diterima.

Langkah-langkah:
- Pimpinan sektor atau staf sektor membuat Work Order berdasarkan Sales Order yang sudah disetujui.
>WO berisi informasi: Nomor SO yang terkait, Produk yang dipesan, Jumlah yang harus diproduksi atau disiapkan, Tanggal pengiriman yang dijadwalkan

- WO diserahkan kepada bagian produksi atau gudang untuk diproses lebih lanjut.

**D. Penganggaran oleh Pimpinan Projek**
Pimpinan Projek akan membuat anggaran untuk menjalankan pesanan yang tercatat dalam WO. Anggaran ini mencakup semua biaya yang dibutuhkan untuk menjalankan pesanan tersebut, seperti biaya barang, pengiriman, dan biaya lainnya.

*Langkah-langkah:*
- Pimpinan projek menilai semua biaya yang terkait dengan pesanan.
- Pimpinan projek menyusun anggaran yang mencakup biaya produksi, biaya pengiriman, dan biaya tambahan lainnya.
- Anggaran yang telah disusun akan diperiksa dan disetujui oleh pihak terkait sebelum dilanjutkan ke proses berikutnya.

**E. Verifikasi Anggaran oleh Verifikator**
Setelah anggaran disusun, Verifikator perusahaan akan memeriksa anggaran tersebut untuk memastikan bahwa semua biaya tercatat dengan benar dan sesuai dengan kebijakan perusahaan.

*Langkah-langkah:*

- Verifikator menerima anggaran yang telah disusun oleh pimpinan projek.
- Verifikator memeriksa anggaran dengan membandingkan estimasi biaya dengan pengeluaran yang diharapkan.
- Jika anggaran disetujui, verifikator memberikan tanda tangan persetujuan.
- Jika tidak, verifikator memberikan catatan untuk revisi.

**F. Pengajuan Kebutuhan Keuangan untuk Running Projek**
Setelah anggaran disetujui, Pimpinan Projek mengajukan kebutuhan keuangan untuk menjalankan proyek sesuai dengan anggaran yang telah diverifikasi.

*Langkah-langkah:*

- Pimpinan projek mengidentifikasi kebutuhan dana untuk setiap aspek dari proyek, termasuk biaya bahan, biaya tenaga kerja, dan biaya pengiriman.
- Pimpinan projek mengajukan permintaan dana kepada bagian keuangan untuk memulai proses pembayaran dan pengeluaran.

**G. Proses Pengadaan Barang**
Deskripsi Proses: Jika dalam pesanan terdapat kebutuhan untuk pengadaan barang atau bahan, maka Bagian Pengadaan akan melakukan proses pengadaan sesuai dengan anggaran yang telah disetujui.

*Langkah-langkah:*

- Bagian pengadaan memeriksa stok barang di gudang.

- Jika barang yang dibutuhkan tidak ada, bagian pengadaan mencari pemasok yang sesuai.

- Bagian pengadaan melakukan pemesanan barang dari pemasok dan mengatur pengiriman.

- Barang yang diterima akan diteruskan ke bagian produksi atau pengiriman sesuai dengan kebutuhan.


## 3. Diagram Alur Proses Bisnis

## 4. Analisis Sistem
Pada bagian sebelumnya telah dijelaskan proses bisnis sektor perdagangan yang berjalan di perusahaan, mulai dari inisiasi permintaan oleh pelanggan hingga penyelesaian pekerjaan dan pelaporan keuangan. Proses tersebut mencakup beberapa tahapan penting seperti pembuatan Sales Order (SO), approval oleh manajer sektor, penerbitan Work Order (WO), penyusunan anggaran, hingga pengadaan barang jika diperlukan.

Untuk dapat membangun sistem informasi akuntansi yang mendukung proses tersebut secara efektif, diperlukan pemahaman yang komprehensif terhadap kebutuhan pengguna (user needs) di setiap tahapan bisnis. Oleh karena itu, pada bab ini akan dibahas analisis sistem berdasarkan pendekatan Agile melalui penyusunan user story, acceptance criteria, dan use case sebagai representasi dari kebutuhan pengguna terhadap fitur sistem yang akan dibangun.

Pendekatan ini tidak hanya membantu merinci fungsionalitas sistem dari sudut pandang pengguna, tetapi juga menjadi dasar yang kuat bagi tim pengembang dalam merancang dan mengimplementasikan solusi yang tepat sasaran. Fokus pada sektor perdagangan ini akan mencakup seluruh alur operasional mulai dari pencatatan permintaan pelanggan (Sales Order) hingga tahap persiapan operasional (Work Order), yang akan dijabarkan secara sistematis dalam bagian-bagian berikut.

> [User Story US-SO-01: Input Sales Order](/docs/userStories/SO/us_so_01.md)

> [User Story US-SO-02: Approval Sales Order](/docs/userStories/SO/us_so_02.md)
