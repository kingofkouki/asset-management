# AssetVault Pro — Sistem Manajemen Aset & Peminjaman

Aplikasi manajemen inventaris, peminjaman aset, dan pelacakan label **QR Code & Barcode** yang ultra-ringan dalam satu file (`index.html`). Dirancang tanpa proses *build* dan siap langsung di-deploy ke **GitHub Pages** maupun dijalankan secara lokal.

---

## Fitur Utama

* **Autentikasi & Keamanan Sesi:** Halaman login dengan PIN/Password default **`555`** (dapat diubah melalui menu *Settings*).
* **Dashboard KPI & Penyusutan Otomatis:** Ringkasan total nilai perolehan, kalkulasi **nilai buku saat ini** (*straight-line depreciation*), status kondisi unit, dan grafik distribusi nilai per kategori.
* **Manajemen Peminjaman Aset (*Asset Loan & Return*):** Pencatatan peminjaman perangkat oleh staf/divisi, pelacakan tenggat pengembalian, serta proses pengembalian 1-klik yang otomatis memperbarui status dan riwayat aset.
* **Label Generator (QR Code & Barcode 1D):** Pembuatan stiker label otomatis lengkap dengan QR Code (berisi tautan detail aset) dan Barcode `CODE128` siap cetak.
* **Barcode & QR Scanner Terpadu:**
  * Pemindaian langsung melalui kamera perangkat (*Android/iOS/Webcam*).
  * Dukungan penuh untuk perangkat **USB / Bluetooth Barcode Scanner**.
* **Audit Trail & Riwayat Kronologis:** Pencatatan log inspeksi rutin, mutasi lokasi, serah terima PIC, dan biaya perbaikan.
* **Pengaturan Dinamis (*Settings*):** Kustomisasi nama perusahaan, upload logo instansi, pengaturan prefix kode aset, manajemen kategori dinamis, dan fitur *Export CSV*.

---

## Akses Login Default

* **Password / PIN Awal:** `555`

---

## Cara Menjalankan & Deploy ke GitHub Pages

1. **Upload ke Repository GitHub:**
   Unggah file `index.html` dan `README.md` ke dalam repository GitHub Anda.
2. **Aktifkan GitHub Pages:**
   * Buka tab **Settings** pada repository GitHub Anda.
   * Pilih menu **Pages** di bilah samping kiri.
   * Pada bagian **Build and deployment → Source**, pilih **Deploy from a branch**.
   * Pilih branch `main` dan folder `/ (root)`, lalu klik **Save**.
3. **Akses Aplikasi:**
   Tunggu beberapa saat hingga URL publik muncul (contoh: `https://username.github.io/nama-repository/`), lalu buka dan masukkan password **`555`**.

---

## Teknologi yang Digunakan

* **UI Framework:** [Pico CSS v2](https://picocss.com/) (Classless, ringan, responsif)
* **Reaktivitas:** [Alpine.js v3](https://alpinejs.dev/)
* **QR & Barcode Engine:** `QRCode.js`, `JsBarcode`, dan `html5-qrcode`
* **Penyimpanan Lokal:** Browser `LocalStorage` (Zero-backend / Zero-database setup)

---

## Catatan Penyimpanan Data

Karena aplikasi ini berjalan 100% di sisi klien (*client-side*), seluruh perubahan data aset, transaksi peminjaman, logo, dan pengaturan disimpan pada **`LocalStorage` browser** perangkat yang digunakan. Gunakan tombol **Export CSV** secara berkala untuk mencadangkan data inventaris ke dalam file spreadsheet.
