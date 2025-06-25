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
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Actor</td>
    <td style="border: 1px solid #000; padding: 8px;">Manajer Sektor </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Melihat detail dari SO yang masuk untuk disetujui.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Alur Normal</td>
    <td style="border: 1px solid #000; padding: 8px;">
      <ol style="margin: 0; padding-left: 20px;">
        <li>Manajer login ke sistem.</li>
        <li>Membuka daftar SO yang menunggu approval.</li>
        <li>Memilih salah satu SO dan membaca detailnya.</li>
      </ol>
    </td>
  </tr>
</table>
<br>

**🔹 Use Case 2: Approve Sales Order**
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Actor</td>
    <td style="border: 1px solid #000; padding: 8px;">
    Manajer Sektor  
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Menyetujui SO agar dapat dilanjutkan ke proses Work Order.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Alur Normal</td>
    <td style="border: 1px solid #000; padding: 8px;">
      <ol style="margin: 0; padding-left: 20px;">
        <li>Manajer meninjau SO.</li>
        <li>Klik “Setujui”.</li>
        <li>Sistem mengubah status SO menjadi approved.</li>
        <li>Notifikasi dikirim ke petugas sektor.</li>
      </ol>
    </td>
  </tr>
</table>

<br>

**🔹 Use Case 3: Reject Sales Order**
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Actor</td>
    <td style="border: 1px solid #000; padding: 8px;">Manajer Sektor </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Menolak SO jika ada kesalahan atau ketidaksesuaian.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Alur Normal</td>
    <td style="border: 1px solid #000; padding: 8px;">
      <ol style="margin: 0; padding-left: 20px;">
        <li>Manajer memilih SO.</li>
        <li>Klik “Tolak”, mengisi alasan penolakan.</li>
        <li>Sistem mengubah status menjadi rejected.</li>
        <li>Notifikasi dikirim ke petugas sektor beserta alasan.</li>
      </ol>
    </td>
  </tr>
</table>
<br>

**🔹 Use Case 4: Audit Approval Log**
<table style="width: 100%; border-collapse: collapse; font-family: sans-serif;">
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Actor</td>
    <td style="border: 1px solid #000; padding: 8px;">Sistem (dapat juga diakses oleh Auditor/Admin)</td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Deskripsi</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Menyimpan log siapa yang menyetujui/menolak dan kapan.
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid #000; padding: 8px; font-weight: bold;">Output</td>
    <td style="border: 1px solid #000; padding: 8px;">
      Catatan log tersedia untuk kebutuhan audit.
    </td>
  </tr>
</table>
