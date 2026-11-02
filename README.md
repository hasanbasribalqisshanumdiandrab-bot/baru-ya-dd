# Dashboard Monitoring Toko · Area Hasan

Dashboard web statis untuk GitHub Pages, terhubung ke Google Sheets dan memiliki tiga tampilan: Produktivitas, Member & Fair, serta Akumulasi Bulan.

## Deploy ke GitHub Pages

1. Buat repository GitHub baru.
2. Upload `index.html` dan `README.md` ke folder utama repository.
3. Buka **Settings → Pages**.
4. Pada **Build and deployment**, pilih **Deploy from a branch**.
5. Pilih branch `main` dan folder `/(root)`, lalu klik **Save**.
6. Tunggu proses selesai; alamat situs akan tampil di halaman Pages.

## Konfigurasi penting

Buka bagian `<script>` di `index.html`, lalu periksa:
- `SHEET_ID`: ID spreadsheet sumber data.
- `BLOCK`: baris awal blok data untuk jam 10:00, 15:00, 19:00, dan 23:00.
- `JAMS`: label jam pemantauan.
- `TARGET` dan `TOTAL_T`: target produktivitas.
- `STORE_MASTER`: urutan 18 toko yang diberikan. Jika spreadsheet memiliki toko ke-19, nama dan kodenya dibaca dari sheet dan ditampilkan setelah daftar utama.

**Penting:** spreadsheet harus dapat dibaca publik dengan izin Viewer (atau dipublikasikan sesuai kebijakan organisasi). Nama tab harian mengikuti pola `Tgl_01`, `Tgl_02`, ... `Tgl_31`. Struktur kolom dan baris sumber harus tetap sesuai konfigurasi.

## Fitur

- Sinkronisasi otomatis setiap 30 detik, dengan pencegahan request bertumpuk.
- Fallback ke tanggal sebelumnya jika sheet tanggal aktif belum tersedia.
- Pengambilan data akumulasi bulanan bertahap agar tidak membanjiri Google Sheets.
- Tab Produktivitas, Member & Fair, dan Akumulasi Bulan.
- Download tampilan aktif menjadi PNG resolusi tinggi, termasuk judul dan tanggal.
- Tampilan responsif untuk desktop dan ponsel.
- Validasi akses sheet, pesan kesalahan yang lebih jelas, dan escaping teks dari spreadsheet.

## Catatan

Dashboard membaca data dari spreadsheet; GitHub Pages hanya menjadi tempat hosting halaman. Jika data tidak muncul, periksa `SHEET_ID`, izin spreadsheet, nama tab, dan posisi blok data.
