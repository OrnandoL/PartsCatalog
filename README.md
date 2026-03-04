# Honda Parts Catalog (GitHub Pages)

Website katalog suku cadang Honda berbasis static site.

Live site:
`https://ornandol.github.io/PartsCatalog/`

## Fitur Utama
- Tabel katalog per kategori: `Cub`, `Matic`, `Sport`
- Search client-side untuk:
  - tipe motor/kode motor
  - part number
  - deskripsi part (BOM)
- Hasil search menampilkan:
  - detail part dari BOM
  - harga HET (jika tersedia)
  - link ke viewer PDF dengan highlight otomatis
- PDF viewer dengan:
  - zoom controls
  - highlight kata kunci part number
  - bubble HET pada header viewer

## Struktur Repository
- `index.html`: halaman utama katalog + search
- `bom-index.js`: index BOM (`window.BOM_INDEX`)
- `het-index.js`: index harga HET (`window.HET_INDEX`)
- `het-index.json`: versi JSON dari index HET
- `pdf-highlight-viewer.html`: viewer PDF + highlight + info HET
- `downloads/`: semua aset PDF katalog
  - `downloads/cub/`
  - `downloads/matic/`
  - `downloads/sport/`
- `docs/`: dokumentasi internal
  - `docs/SEARCH_SYSTEM.md`
  - `docs/DEPLOYMENT.md`
- `WARNING.txt`: pemberitahuan hak cipta

## Data Index yang Dipakai Frontend
- BOM: dibaca dari `window.BOM_INDEX.parts`
- HET: dibaca dari `window.HET_INDEX.prices`
- Kunci part number dinormalisasi ke format compact tanpa karakter non-alfanumerik untuk matching yang konsisten.

## Deploy GitHub Pages
Gunakan source:
- Branch: `main`
- Folder: `/(root)`

Setelah push ke `main`, tunggu proses publish GitHub Pages selesai (biasanya 1-5 menit), lalu lakukan hard refresh browser (`Ctrl+F5`).

## Catatan Lisensi
Repository ini **bukan open-source**.
Semua hak cipta dilindungi. Lihat `WARNING.txt` untuk detail.
