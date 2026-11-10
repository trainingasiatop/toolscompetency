# Tools Competency Assessment Karyawan Baru Asiatop

Versi online tools penilaian kompetensi karyawan baru, termasuk Form Coaching (Coaching 1, Coaching 2, Perbandingan).
Halaman: https://trainingasiatop.github.io/toolscompetency/

## Cara kerja penyimpanan (tanpa server/database tambahan)
- Semua data disimpan di satu file terenkripsi: `data/db.json`.
- **Membaca** data (daftar nama untuk atasan) bisa dari perangkat mana pun.
- **Menyimpan** hanya bisa dari perangkat yang sudah diisi token GitHub di *Admin Recap › Database › Pengaturan Penyimpanan*.
  Di perangkat itu, setiap pengisian karyawan, atasan, dan Form Coaching tersimpan otomatis.
- Di perangkat lain, tools menampilkan **kode** sebagai cadangan. PD Officer menempelkan kode itu di *Admin Recap › Database › Tambah dari Kode*.
- Nama yang tercatat lebih dari sekali ditandai **Dobel** di tab Database.

## Membuat token GitHub (sekali saja, untuk perangkat PD Officer)
1. GitHub › Settings › Developer settings › Personal access tokens › **Fine-grained tokens** › Generate new token.
2. Resource owner: **trainingasiatop**. Repository access: **Only select repositories** › `toolscompetency`.
3. Permissions › Repository permissions › **Contents: Read and write**.
4. Salin token, buka tools › Admin Recap (password admin) › Database › Pengaturan Penyimpanan › tempel › **Simpan & Tes Koneksi**.

Token hanya tersimpan di browser perangkat tersebut dan tidak pernah masuk ke repo.

## Catatan keamanan
Repo publik dapat dilihat siapa saja. File data dienkripsi agar tidak terbaca langsung atau terindeks, tetapi kunci pembukanya ada di kode halaman,
sehingga orang yang cukup teknis tetap bisa membukanya. Untuk kerahasiaan penuh, jadikan repo private (GitHub Pages untuk repo private membutuhkan paket berbayar).
