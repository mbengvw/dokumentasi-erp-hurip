# 🎯 User Story US-02: Approval Sales Order oleh Manajer Sektor
## ✅ User Story

> **Sebagai** Manajer Sektor,
**Saya ingin** melakukan review dan approval terhadap Sales Order,
**Agar** hanya SO yang layak saja yang diteruskan ke proses Work Order.

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

**🔹 Use Case 1: Review Sales Order**

**Actor:** Manajer Sektor  
**Deskripsi:** Melihat detail dari SO yang masuk untuk disetujui.  
**Alur Normal:**
- Manajer login ke sistem.
- Membuka daftar SO yang menunggu approval.
- Memilih salah satu SO dan membaca detailnya.
<hr>

**🔹 Use Case 2: Approve Sales Order**

**Actor:** Manajer Sektor  
**Deskripsi:** Menyetujui SO agar dapat dilanjutkan ke proses Work Order.  
**Alur Normal:**

- Manajer meninjau SO.
- Klik “Setujui”.
- Sistem mengubah status SO menjadi approved.
- Notifikasi dikirim ke petugas sektor.
<hr>

**🔹 Use Case 3: Reject Sales Order**

**Actor:** Manajer Sektor  
**Deskripsi:** Menolak SO jika ada kesalahan atau ketidaksesuaian.  
**Alur Normal:**

- Manajer memilih SO.
- Klik “Tolak”, mengisi alasan penolakan.
- Sistem mengubah status menjadi rejected.
- Notifikasi dikirim ke petugas sektor beserta alasan.
<hr>

**🔹 Use Case 4: Audit Approval Log**

**Actor:** Sistem (dapat juga diakses oleh Auditor/Admin)  
**Deskripsi:** Menyimpan log siapa yang menyetujui/menolak dan kapan.  
**Output:** Catatan log tersedia untuk kebutuhan audit.