# Dashboard Monitoring Toko · Area Hasan

Dashboard web statis modern & responsif untuk **GitHub Pages**, terhubung otomatis ke Google Sheets. Memiliki 3 tab monitoring utama: **Produktivitas**, **Member & Fair**, dan **Akumulasi Bulan**, lengkap dengan fitur **Download Gambar Resolusi Tinggi (Siap Share WhatsApp)**.

---

## 🚀 Cara Deploy Gratis ke GitHub Pages

1. Buat **Repository Baru** di GitHub (misal: `dashboard-area-hasan`).
2. Upload file `index.html` dan `README.md` ke folder utama (`root`) repository.
3. Buka menu **Settings → Pages** di repository Anda.
4. Pada bagian **Build and deployment**:
   - **Source**: Pilih `Deploy from a branch`
   - **Branch**: Pilih `main` (atau `master`) dan folder `/(root)`
5. Klik **Save**.
6. Tunggu ~1 menit, link website publik Anda akan langsung aktif!

---

## 🛠️ Konfigurasi Utama (`index.html`)

Buka file `index.html` dan periksa variabel berikut pada tag `<script>` jika ingin mengubah data:
- `SHEET_ID`: ID spreadsheet Google Sheets sumber data (`1ylxNHZGFvu2-AE_62H9qBPFuVa6CJHpTw6pfot2AaY8`).
- `STORE_MASTER`: Daftar urutan resmi 18 toko Area Hasan.
- `TARGET` & `TOTAL_T`: Target produktivitas indikator (PSM, SERTIS, PWP, SEGER, CEBAN).
- `REFRESH_DETIK`: Interval otomatis refresh data (default: 30 detik).

> **Penting**: Google Sheet wajib disetting sebagai **Public / Anyone with the link (Viewer)** agar GitHub Pages dapat membaca data secara langsung tanpa login.

---

## ✨ Fitur & Perbaikan Utama

- **Zero Dummy Data**: Menyaring otomatis baris template / header kosong (`KODE TOKO` / `Nama Toko`) dari spreadsheet.
- **Export HD Image Siap Share WA**: Fitur download gambar hasil monitoring dengan header profesional & angka yang sangat jelas di HP/WA.
- **Super Fast Parallel Fetching**: Penarikan data cepat dengan timeout otomatis & penanganan error yang baik.
- **Auto Fallback Tanggal**: Jika tanggal aktif belum diisi, otomatis mengambil tanggal terbaru yang tersedia.
- **100% Responsif**: Tampilan rapi di layar Komputer, Tablet, maupun Smartphone.
