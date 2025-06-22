# 🎯 User Story US-01: Input Sales Order
## ✅ User Story
> **Sebagai** Petugas Sektor,
**Saya ingin** menginput Sales Order (SO) ke sistem,
**Agar** proses bisnis sektor bisa dimulai secara terstruktur dan terdokumentasi.

## ✅ Acceptance Criteria
|<div style="width: 60px;">No</div>	|Kriteria |Penjelasan|
|-------|------|------|
|AC-01	|Petugas dapat mengakses form input SO	|Form tersedia sesuai hak akses petugas sektor.
|AC-02	|Form SO memiliki field yang lengkap	|Misalnya: nomor SO, tanggal, nama proyek, nama customer, sektor usaha, jenis layanan, nilai estimasi, deskripsi, dsb.|
|AC-03	|SO yang diinput akan disimpan sebagai status draft	|SO tidak langsung aktif sebelum ada approval.|
|AC-04	|Petugas dapat menyimpan, mengedit, atau menghapus SO sebelum di-approve	|Memberi fleksibilitas sebelum dikunci.|
|AC-05	|Setelah submit, sistem mencatat waktu input dan user yang membuat|	Audit trail disimpan.|
|AC-06	|Sistem memberi notifikasi ke manajer sektor untuk approval	|Proses approval dipicu otomatis.|
|AC-07	|Validasi dilakukan pada field wajib (required fields)	|Tidak bisa disubmit jika data belum lengkap.|

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
