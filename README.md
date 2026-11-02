# Dashboard Monitoring Toko · Area Hasan

Dashboard Monitoring Toko Realtime (V20 Light Theme) yang menarik data otomatis dari Google Sheets.

## Cara Deploy ke GitHub Pages (Sangat Mudah & Gratis):

1. Buat Repository Baru di GitHub (misal: `dashboard-area-hasan`).
2. Upload file `index.html` dan `README.md` ini ke repository tersebut.
3. Buka menu **Settings** > **Pages** di repository GitHub Anda.
4. Pada bagian **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** (atau **master**) / folder `/(root)`
5. Klik **Save**. 
6. Tunggu ~1 menit, website Anda langsung online di link: `https://<username-github>.github.io/<nama-repo>/`

## Fitur Utama:
- **Super Fast Fetching**: Penarikan data paralel otomatis dari Google Sheet tanpa macet.
- **Auto Fallback**: Mengambil sheet tanggal aktif paling mutakhir secara otomatis.
- **3 Tab Monitoring**:
  1. **Produktivitas**: KPI Target, Persentase, Evaluasi Minus Qty.
  2. **Member & Fair**: Persentase Redeem vs Lost, Skor Fair.
  3. **Akumulasi Bulan**: Poin kesalahan harian (Tgl 1-31).
- **Export HD Image**: Fitur download gambar hasil monitoring per shift/harian.
