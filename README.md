# Sistem Asistensi GIS Diagnostic

Repository **public** khusus TEST-ONLY untuk menguji Google Identity Services (GIS) pada origin HTTPS eksternal.

## Batas

Repository ini tidak berisi kode login production Sistem Asistensi Skripsi, database, secret, atau credential rahasia.

## GitHub Pages

Target URL:

https://r4hm4td3ddy.github.io/sistem-asistensi-gis-diagnostic/

URL aktual dikonfirmasi setelah workflow GitHub Pages berhasil.

## OAuth Client

Gunakan OAuth Client tipe **Web application**.

Authorized JavaScript origin:

https://r4hm4td3ddy.github.io

Jangan gunakan origin Apps Script `script.googleusercontent.com`.

## Pengujian

Buka halaman Pages, masukkan OAuth Client ID Web, lalu klik **Mulai Diagnostic GIS**.

Hasil yang dicari:

- GIS library = TER-MUAT
- Google Sign-In = TERSEDIA
- ID token = BERHASIL — ID token diterima

Payload hanya didecode secara lokal untuk diagnosis. Verifikasi token server-side wajib dilakukan sebelum token digunakan untuk autentikasi aplikasi.
