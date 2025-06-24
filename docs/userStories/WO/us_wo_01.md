# 🎯 US-03: Penerbitan Work Order (WO)
## ✅ User Story

>**Sebagai** Staf Sektor,  
**Saya ingin** membuat Work Order (WO) berdasarkan Sales Order (SO) yang telah disetujui,  
**Agar** pekerjaan dapat dimulai secara resmi dan terstruktur.

## ✅ Acceptance Criteria
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <thead>
    <tr style="background-color: #f2f2f2;">
      <th style="width: 60px; border: 1px solid #ccc; padding: 8px;">No</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Kriteria</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Penjelasan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-01</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Staf hanya dapat membuat WO dari SO yang berstatus approved</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Mencegah penerbitan WO dari SO yang belum sah.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-02</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Form WO otomatis mengambil data dari SO terkait</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Seperti nomor SO, nama proyek, customer, sektor usaha, jenis layanan.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-03</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Staf dapat melengkapi detail WO tambahan</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Contoh: nomor WO, tanggal mulai, estimasi selesai, penanggung jawab lapangan, catatan teknis.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-04</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Sistem mencatat waktu dan user yang menerbitkan WO</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Untuk kebutuhan audit dan pelacakan.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-05</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Setelah disimpan, WO berstatus aktif dan dikaitkan dengan SO</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Sistem menghubungkan WO dengan SO induknya.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-06</td>
      <td style="border: 1px solid #ccc; padding: 8px;">WO yang sudah diterbitkan tidak bisa dihapus</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Hanya bisa dibatalkan (void) oleh user berwenang.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-07</td>
      <td style="border: 1px solid #ccc; padding: 8px;">WO dapat dilihat oleh Manajer Proyek untuk proses selanjutnya (penganggaran)</td>
      <td style="border: 1px solid #ccc; padding: 8px;">WO jadi dasar budgeting.</td>
    </tr>
  </tbody>
</table>

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