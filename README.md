# Halaman pendukung Sistem Pembimbingan Tugas Akhir

Repository publik untuk halaman informasi dan Google Identity Services yang
dipakai aplikasi. Backend/database/config berada di proyek terpisah:
[sistem-asistensi-skripsi](https://github.com/r4hm4tD3ddy/sistem-asistensi-skripsi).

| Path | Fungsi |
|---|---|
| `/aplikasi/` | Informasi aplikasi dan tautan portal produksi |
| `/privasi/` | Penggunaan, penyimpanan, pembagian data dan pencabutan izin |
| `/ketentuan/` | Penggunaan akun, dokumen, layanan dan pembayaran |
| `/login/` | Login GIS produksi yang sudah ada |
| `/drive/` | Halaman GIS Drive/Billing legacy yang sudah ada |
| `/` | Diagnostik GIS historis; bukan homepage OAuth produksi |

Base URL: `https://r4hm4td3ddy.github.io/sistem-asistensi-gis-diagnostic/`.
Workflow `.github/workflows/deploy-gis-diagnostic.yml` menerbitkan isi repository
melalui GitHub Pages saat main diperbarui.

## Pelengkapan Branding OAuth — 2 November 2026

Source awal GitHub `1250177`. Checkout lokal lama `bfd4e34` diselaraskan dengan
fast-forward; tidak ada perubahan lokal pengguna. Tiga halaman informasi/CSS
ditambahkan beserta tautan statis login/Drive. Root diagnostik, target SERVER,
Client ID, callback/POST token dan semua blok script lama tetap. Tidak mengubah
source Apps Script atau deployment SERVER296/AUTH297.

Halaman App domain proyek Cloud produksi `encoded-source-510002-m8` memakai
kontak dari screenshot Branding pengguna. Isi berdasarkan source/kontrak aktif
Drive, draf, foto dan Billing. Tidak menjanjikan penghapusan otomatis, enkripsi
tambahan atau keberhasilan verifikasi Google. Halaman informasi tidak memuat
JavaScript, analytics, form, token atau Client Secret. Data Google, database,
Script Properties, Drive pemilik, akses pengelola serta retensi dijelaskan.
Perubahan praktik penggunaan data harus diselaraskan di halaman privasi.

Pemeriksaan meliputi source/paritas script lama, tautan lokal dan pratinjau HTML
statis; tidak menjalankan tes/login/OAuth/fungsi aplikasi. Keberhasilan Pages
dan akses HTTP dicatat setelah rilis. Halaman publik bukan bukti domain sudah
terverifikasi Search Console, Branding diterima atau scope disetujui Google.
Jangan commit Secret/token, data akun atau backup database ke repository publik.

---

## Histori setup diagnostik awal (sebelum login produksi ditambahkan)

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
