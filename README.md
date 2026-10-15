# Peta PLTS Komunal Lisdes

Data koordinat mengacu pada KMZ *Lokasi 53 PLTS Komunal* (rekap 30-09-26).

Peta interaktif lokasi PLTS Komunal + BESS Program Lisdes TA 2026. Peta membaca data dari file CSV di folder `data/`, jadi data cukup diubah lewat CSV tanpa menyentuh `index.html`.

## Struktur file
| File | Isi | Perlu diedit? |
|---|---|---|
| `index.html` | Halaman peta (kode, tampilan, garis pantai) | Tidak |
| `data/lokasi.csv` | Daftar lokasi, satu baris per lokasi | **Ya, ini file utamanya** |
| `data/titik-kmz-luar-daftar.csv` | Titik di KMZ yang tidak ada di daftar | Opsional |
| `data/lahan.geojson` | Batas lahan dari KMZ | Jarang |

## Kolom `data/lokasi.csv`
| Kolom | Keterangan |
|---|---|
| `no` | Nomor urut |
| `nama` | Nama lokasi/dusun (wajib) |
| `provinsi`, `kabupaten`, `kecamatan`, `desa`, `unit` | Administrasi dan unit PLN |
| `wilayah` | Pengelompokan wilayah, misal `Papua`. Nilai baru otomatis jadi grup baru di legenda |
| `lat`, `lon` | Koordinat desimal (wajib). Contoh: `-3.56166` dan `133.33679` |
| `sumber_koordinat` | `KMZ` = titik penuh; selain itu (mis. `Indikatif`) = titik putus-putus |
| `pv_kwp`, `bess_kwh`, `capel` | Kapasitas PV, BESS, jumlah calon pelanggan |
| `jtm_kms`, `jtr_kms` | Panjang JTM/JTR |
| `kluster` | `A` atau `B` |
| `opsi1` … `opsi5` | Nomor paket di tiap opsi klusterisasi |
| `config` | Kode konfigurasi dari rekap koordinat (mis. `config_e_6`) |
| `catatan` | Kalau diisi, lokasi diberi tanda CEK dan catatannya muncul di popup |

## Cara edit data
**Langsung di GitHub (paling aman):** buka `data/lokasi.csv` → ikon pensil (Edit) → ubah → **Commit changes**. Peta ikut berubah 1–2 menit kemudian (tekan Ctrl+F5 bila masih versi lama).

**Lewat Excel:** download `lokasi.csv`, buka di Excel, edit, lalu **Save As → CSV UTF-8 (Comma delimited)**. Upload kembali lewat *Add file → Upload files* dengan nama yang sama. Pemisah titik koma (`;`) dan desimal koma (`0,13`) tetap terbaca.

Baris dengan nama kosong atau koordinat di luar wilayah Indonesia tidak ditampilkan dan dicantumkan di panel **Catatan data**, lengkap dengan nomor barisnya.

## Catatan
- Peta hanya tampil lewat GitHub Pages (atau server web). Jika `index.html` dibuka langsung dari komputer, CSV tidak bisa dibaca browser.
- Peta dasar: citra satelit Esri (default), OpenStreetMap, atau garis pantai Natural Earth.
- Nilai RAB/pagu tidak dimuat.
