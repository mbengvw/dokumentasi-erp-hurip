# 🎯 User Story US-04: Penyusunan Anggaran oleh Manajer Proyek
## ✅ User Story
>**Sebagai** Manajer Proyek,  
**Saya ingin** menyusun anggaran berdasarkan Work Order yang telah diterbitkan,  
**Agar** kebutuhan biaya proyek dapat diperkirakan dan dikendalikan sejak awal.

## ✅ Acceptance Criteria
<table border="1" cellpadding="8" cellspacing="0">
  <thead>
    <tr>
      <th>No.</th>
      <th>Kriteria</th>
      <th>Penjelasan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>AC-01</td>
      <td>Hanya WO berstatus <em>aktif</em> yang bisa digunakan</td>
      <td>Mencegah penyusunan anggaran untuk proyek yang belum disahkan.</td>
    </tr>
    <tr>
      <td>AC-02</td>
      <td>Form anggaran dapat diisi dengan rincian biaya</td>
      <td>Komponen seperti material, subkontrak, alat berat, tenaga kerja.</td>
    </tr>
    <tr>
      <td>AC-03</td>
      <td>Setiap komponen biaya memiliki detail</td>
      <td>Deskripsi, volume, satuan, harga satuan, dan total.</td>
    </tr>
    <tr>
      <td>AC-04</td>
      <td>Anggaran dapat disimpan sebagai draft atau final</td>
      <td>Memungkinkan pengisian bertahap dan koreksi sebelum finalisasi.</td>
    </tr>
    <tr>
      <td>AC-05</td>
      <td>Setelah final, anggaran terkunci</td>
      <td>Tidak dapat diubah sembarangan dan siap diproses lebih lanjut.</td>
    </tr>
    <tr>
      <td>AC-06</td>
      <td>Sistem mencatat user dan waktu penyusunan</td>
      <td>Untuk audit trail dan tanggung jawab.</td>
    </tr>
    <tr>
      <td>AC-07</td>
      <td>Anggaran dapat dibandingkan dengan realisasi</td>
      <td>Untuk kebutuhan kontrol biaya proyek saat pelaksanaan.</td>
    </tr>
  </tbody>
</table>


## ✅ Use Case Terkait
**🔹 Use Case 1: Buat Anggaran Proyek**
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Actor</td>
    <td style="border: 1px solid #000; padding: 8px;">Manajer Proyek</td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Menyusun dan menyimpan rencana anggaran proyek berdasarkan Work Order yang telah diterbitkan.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Alur Normal</td>
    <td style="border: 1px solid #000; padding: 8px;">
      <ol style="margin: 0; padding-left: 20px;">
        <li>Manajer login ke sistem dan membuka modul Work Order.</li>
        <li>Memilih WO yang ingin dibuatkan anggaran.</li>
        <li>Mengklik tombol "Buat Anggaran".</li>
        <li>Mengisi rincian komponen biaya seperti bahan, tenaga kerja, alat, dan subkontrak.</li>
        <li>Menyimpan anggaran sebagai <em>draft</em> atau <em>final</em>.</li>
      </ol>
    </td>
  </tr>
</table>
<br>

**🔹 Use Case 2: Lihat Anggaran Proyek**
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Aktor</td>
    <td style="border: 1px solid #000; padding: 8px;">Manajer Proyek, Auditor, Bagian Keuangan</td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Menampilkan rincian anggaran yang sudah disusun untuk proyek tertentu.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Alur Normal</td>
    <td style="border: 1px solid #000; padding: 8px;">
      <ol style="margin: 0; padding-left: 20px;">
        <li>User membuka daftar WO.</li>
        <li>Klik "Lihat Anggaran" untuk WO tertentu.</li>
        <li>Sistem menampilkan rincian dan status anggaran.</li>
      </ol>
    </td>
  </tr>
</table>
<br>

**🔹 Use Case 3: Revisi Anggaran (Opsional)**
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Aktor</td>
    <td style="border: 1px solid #000; padding: 8px;">Manajer Proyek</td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Melakukan revisi anggaran jika masih berstatus draft sebelum dikunci sebagai final.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Alur Normal</td>
    <td style="border: 1px solid #000; padding: 8px;">
      <ol style="margin: 0; padding-left: 20px;">
        <li>Buka anggaran yang berstatus draft.</li>
        <li>Lakukan perubahan pada komponen biaya.</li>
        <li>Simpan ulang sebagai draft atau final.</li>
      </ol>
    </td>
  </tr>
</table>
<br>

**🔹 Use Case 4: Bandingkan Anggaran vs Realisasi (di tahap pelaksanaan)**
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Aktor</td>
    <td style="border: 1px solid #000; padding: 8px;">Sistem / Manajer Proyek</td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Sistem menampilkan perbandingan antara nilai anggaran awal dengan realisasi biaya proyek secara berkala.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Alur Normal</td>
    <td style="border: 1px solid #000; padding: 8px;">
      <ol style="margin: 0; padding-left: 20px;">
        <li>Sistem menghitung total biaya aktual berdasarkan transaksi yang masuk.</li>
        <li>Menampilkan perbandingan terhadap anggaran awal.</li>
        <li>Menampilkan selisih dalam nilai dan persentase deviasi.</li>
        <li>User dapat memilih tampilan berdasarkan kategori (bahan, tenaga kerja, alat, dll).</li>
        <li>Laporan dapat diunduh atau dicetak jika diperlukan.</li>
      </ol>
    </td>
  </tr>
</table>


