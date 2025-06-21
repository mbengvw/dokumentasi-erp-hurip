# 🎯 User Story US-02: Approval Sales Order oleh Manajer Sektor
## ✅ User Story

> **Sebagai** Manajer Sektor,
**Saya ingin** melakukan review dan approval terhadap Sales Order,
**Agar** hanya SO yang layak saja yang diteruskan ke proses Work Order.

## ✅ Acceptance Criteria
|<div style="width: 60px;">No</div>	|Kriteria |Penjelasan|
|-------|------|------|
|AC-01|	Manajer dapat melihat daftar SO yang menunggu persetujuan	|Sistem menampilkan SO dengan status draft/menunggu approval.|
|AC-02|	Manajer dapat melihat detail isi SO	|Termasuk informasi proyek, customer, nilai estimasi, jenis layanan, deskripsi, dsb.|
|AC-03|	Manajer dapat menyetujui atau menolak SO|	Tersedia opsi “Setujui” dan “Tolak” pada setiap SO.|
|AC-04|	Jika disetujui, status SO menjadi approved dan tidak dapat diedit lagi oleh petugas sektor	|Mencegah manipulasi setelah persetujuan.|
|AC-05|	Jika ditolak, status menjadi rejected dan disertai catatan alasan	|Dikirim kembali ke petugas sektor untuk perbaikan.|
|AC-06|	Sistem mencatat siapa yang meng-approve atau menolak, dan kapan waktunya|	Audit trail tersedia.|
|AC-07|	Notifikasi dikirim ke petugas sektor setelah keputusan dibuat	|Untuk feedback langsung ke pembuat SO.|

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