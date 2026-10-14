# Peta PLTS Komunal Lisdes – 53 Lokasi

Peta interaktif 53 lokasi PLTS Komunal + BESS Program Lisdes TA 2026 Tahap II.

- `index.html`: halaman peta, berdiri sendiri (data dan garis pantai sudah tertanam). Library Leaflet 1.9.4 dimuat dari cdnjs.
- `data/lokasi-53.geojson`: data titik lokasi untuk dipakai di QGIS, Google Earth, dan aplikasi lain.

## Fitur
- Warnai titik berdasarkan wilayah, kluster A/B, atau paket per opsi klusterisasi (Opsi 1–5)
- Ukuran titik sebanding kapasitas PV (kWp)
- Peta dasar: garis pantai (offline), OpenStreetMap, atau citra satelit Esri
- Batas lahan dari KMZ, pencarian lokasi, dan catatan data yang perlu diverifikasi

## Publikasi ke GitHub Pages
1. Buat repository baru di GitHub.
2. Unggah `index.html`, `README.md`, dan folder `data/` ke root repository.
3. Buka Settings → Pages, pilih *Deploy from a branch*, branch `main`, folder `/ (root)`.
4. Halaman akan tersedia di `https://<username>.github.io/<nama-repo>/`.

## Sumber data
- KMZ `PLTS KOMUNAL LISDES 53 LOKASI_Okt 26.kmz`
- Excel `Opsi Klusterisasi PLTS Komunal 53 Lokasi.xlsx` (sheet Data Lokasi)
- Garis pantai: Natural Earth 1:10m (domain publik), via world-atlas

Nilai RAB/pagu tidak dimuat.
