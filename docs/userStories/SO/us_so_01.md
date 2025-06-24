# 🎯 User Story US-01: Input Sales Order
## ✅ User Story
> **Sebagai** Petugas Sektor,
**Saya ingin** menginput Sales Order (SO) ke sistem,
**Agar** proses bisnis sektor bisa dimulai secara terstruktur dan terdokumentasi.

## ✅ Acceptance Criteria
<table style="width: 100%; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="width: 60px; border: 1px solid #ccc; padding: 8px;">No</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Kriteria</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Penjelasan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-01</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Manajer dapat melihat daftar SO yang menunggu persetujuan</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Sistem menampilkan SO dengan status draft/menunggu approval.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-02</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Manajer dapat melihat detail isi SO</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Termasuk informasi proyek, customer, nilai estimasi, jenis layanan, deskripsi, dsb.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-03</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Manajer dapat menyetujui atau menolak SO</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Tersedia opsi “Setujui” dan “Tolak” pada setiap SO.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-04</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Jika disetujui, status SO menjadi approved dan tidak dapat diedit lagi oleh petugas sektor</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Mencegah manipulasi setelah persetujuan.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-05</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Jika ditolak, status menjadi rejected dan disertai catatan alasan</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Dikirim kembali ke petugas sektor untuk perbaikan.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-06</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Sistem mencatat siapa yang meng-approve atau menolak, dan kapan waktunya</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Audit trail tersedia.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">AC-07</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Notifikasi dikirim ke petugas sektor setelah keputusan dibuat</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Untuk feedback langsung ke pembuat SO.</td>
    </tr>
  </tbody>
</table>

## ✅ Use Case yang Terlibat 

**🔹 Use Case UC-SO-01: Buat Sales Order**

**Actor:** Petugas Sektor  
**Deskripsi :** Petugas mengisi form Sales Order dan menyimpannya sebagai draft.  
**Alur Normal:**  
- Petugas login dan buka modul Sales Order.
- Klik tombol “Buat Baru”.
- Mengisi data proyek dan layanan.
- Menyimpan SO (status: draft).

**Output:** Sales Order baru dengan status draft tersimpan.
<hr>

**🔹 Use Case UC-SO-02: Edit Sales Order**  
**Actor:** Petugas Sektor  
**Deskripsi:** Petugas dapat mengubah data SO selama masih dalam status draft.  
**Alur Normal:**
- Petugas membuka daftar SO.
- Memilih SO dengan status draft.
- Melakukan pengeditan lalu menyimpan kembali.
<hr>

**🔹 Use Case UC-SO-03: Hapus Sales Order**  
**Actor:** Petugas Sektor  
**Deskripsi:** Petugas menghapus SO selama belum di-approve.  
**Alur Normal:**
- Petugas membuka daftar SO draft.
- Klik tombol “Hapus”.
- Sistem meminta konfirmasi, lalu menghapus.
<hr>

**🔹 Use Case 4: Kirim Notifikasi Approval ke Manajer**
**Actor :** Sistem  
**Trigger :** SO berhasil dibuat atau diubah dan disubmit untuk approval.  
**Deskripsi :** Sistem mengirimkan notifikasi otomatis ke manajer sektor terkait.  
**Output :** Manajer mendapat notifikasi untuk review dan approval.  
