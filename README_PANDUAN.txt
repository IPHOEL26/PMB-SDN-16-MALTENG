PANDUAN SINGKAT PEMASANGAN APLIKASI PMB SD NEGERI 27 MALUKU TENGAH

STATUS UPDATE:
- Google Sheet tujuan sudah diganti ke ID baru:
  1xjdc91mjjCSAyVn6wCegGfilkcBu-y004xcXbzaHLIg
- Link Google Sheet baru:
  https://docs.google.com/spreadsheets/d/1xjdc91mjjCSAyVn6wCegGfilkcBu-y004xcXbzaHLIg/edit?gid=0#gid=0
- Perubahan utama ada pada file Code.gs, konstanta SPREADSHEET_ID.
- script.js TIDAK perlu diganti selama Web App URL Apps Script masih sama dan deployment Apps Script sudah diperbarui.

FILE FRONTEND UNTUK GITHUB PAGES:
1. index.html
2. style.css
3. script.js

FILE BACKEND UNTUK GOOGLE APPS SCRIPT:
1. Code.gs

LANGKAH GOOGLE APPS SCRIPT:
1. Buka Google Sheet tujuan.
2. Klik Extensions / Ekstensi > Apps Script.
3. Hapus kode bawaan, lalu paste isi file Code.gs.
4. Simpan project.
5. Jalankan fungsi setupSheet sekali, lalu izinkan akses.
6. Jalankan fungsi testSpreadsheetAccess untuk memastikan Apps Script bisa membaca Google Sheet baru.
7. Klik Deploy > Manage deployments jika ingin memakai URL Web App lama, lalu edit deployment dan pilih versi baru.
   Atau klik Deploy > New deployment jika ingin membuat URL Web App baru.
8. Jika membuat URL Web App baru, salin URL tersebut.
9. Pilih Web app.
10. Execute as: Me / Saya.
11. Who has access: Anyone / Siapa saja.
12. Deploy.

LANGKAH GITHUB:
1. Upload index.html, style.css, dan script.js ke repository GitHub.
2. Buka script.js.
3. Jika Anda membuat Web App URL baru, ganti nilai WEB_APP_URL di script.js dengan URL baru tersebut.
   Jika Anda hanya memperbarui deployment lama, script.js tidak perlu diubah.
4. Aktifkan GitHub Pages dari Settings > Pages.
5. Buka link GitHub Pages untuk mencoba form.

CATATAN:
- Header Google Sheet otomatis dibuat pada baris 3 mulai kolom A.
- Data pendaftaran otomatis masuk mulai baris 4.
- Kolom No dibuat otomatis oleh Apps Script.
- Jangan simpan data pribadi murid di repository GitHub.


UPDATE:
URL Web App Google Apps Script sudah dipasang langsung di file script.js.


PERUBAHAN FILE:
- Code.gs: SPREADSHEET_ID diganti dari 1x1pSdL23VW9GBHH19P1eXhsRGCEtXqdUQukRdgwOPHE menjadi 1xjdc91mjjCSAyVn6wCegGfilkcBu-y004xcXbzaHLIg.
- Code.gs: fungsi setupSheet dibuat lebih aman karena toast sekarang memakai spreadsheet hasil openById.
- Code.gs: ditambahkan fungsi testSpreadsheetAccess untuk uji koneksi ke Google Sheet baru.
