# 🎯 US-03: Penerbitan Work Order (WO)
## ✅ User Story

>**Sebagai** Staf Sektor,  
**Saya ingin** membuat Work Order (WO) berdasarkan Sales Order (SO) yang telah disetujui,  
**Agar** pekerjaan dapat dimulai secara resmi dan terstruktur.

## ✅ Acceptance Criteria
|<div style="width: 60px;">No</div>	|Kriteria |Penjelasan|
|-------|------|------|
|AC-01|	Staf hanya dapat membuat WO dari SO yang berstatus approved	|Mencegah penerbitan WO dari SO yang belum sah.|
|AC-02	|Form WO otomatis mengambil data dari SO terkait	|Seperti nomor SO, nama proyek, customer, sektor usaha, jenis layanan.|
|AC-03	|Staf dapat melengkapi detail WO tambahan	|Contoh: nomor WO, tanggal mulai, estimasi selesai, penanggung jawab lapangan, catatan teknis.|
|AC-04	|Sistem mencatat waktu dan user yang menerbitkan WO	|Untuk kebutuhan audit dan pelacakan.|
|AC-05	|Setelah disimpan, WO berstatus aktif dan dikaitkan dengan SO	|Sistem menghubungkan WO dengan SO induknya.|
|AC-06|	WO yang sudah diterbitkan tidak bisa dihapus	|Hanya bisa dibatalkan (void) oleh user berwenang.|
|AC-07|	WO dapat dilihat oleh Manajer Proyek untuk proses selanjutnya (penganggaran)	|WO jadi dasar budgeting.|

## ✅ Use Case yang Terlibat

**🔹 Use Case 1: Buat Work Order**

**Actor:** Staf Sektor  
**Deskripsi:** Staf memilih SO yang sudah disetujui, lalu mengisi dan menyimpan WO.  
**Alur Normal:**

- Staf login dan buka daftar SO yang approved.
- Memilih salah satu SO, klik “Buat WO”.
- Form WO otomatis terisi sebagian dari data SO.
- Melengkapi data tambahan WO.
- Menyimpan → WO berstatus aktif dan ditautkan ke SO.
<hr>

**🔹 Use Case 2: Lihat Daftar Work Order**

**Actor:** Semua peran yang relevan (Staf, Manajer Proyek, dll.)  
**Deskripsi:** Melihat daftar WO yang telah diterbitkan.  
**Alur Normal:**
- User login dan buka modul WO.
- Filter berdasarkan sektor, status, proyek, dsb.
<hr>

**🔹 Use Case 3: Batalkan Work Order (opsional)**

**Actor:** User berwenang (misalnya: Kepala Sektor)  
**Deskripsi:** Melakukan void WO jika terjadi kesalahan.  
**Alur Normal:**

- Buka WO → Klik “Batalkan”.
- Masukkan alasan → Sistem ubah status WO jadi void.
<hr>

**🔹 Use Case 4: Tautkan WO ke proses selanjutnya**

**Actor:** Sistem  
**Deskripsi:** WO yang diterbitkan dapat diproses oleh Manajer Proyek untuk membuat penganggaran.