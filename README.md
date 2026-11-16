# AKUISISI DATA CAFE & RESTAURANT DI KOTA DENPASAR MENGGUNAKAN OPENSTREETMAP

Nama: Maryo Julio Rusbugowa Ndada

NIM: 2501010227

Mata Kuliah: Akuisisi dan Manajemen Data - BIFP-243

Program Studi: Teknik Informatika - MDA

Semester / Kelas: 3 / F

Dosen Pengampu: Dr. I Gede Totok Suryawan, S.Kom., M.T.

## Tujuan

Mengumpulkan data cafe & restaurant di Kota Denpasar sebagai bahan analisis kuliner, dan sebagai dataset mentah untuk RTM Tugas 1. Data cafe & restaurant dipilih karena Denpasar memiliki sebaran kuliner yang luas, dan datanya tersedia terbuka di OpenStreetMap.

## 1. Sumber data

- **Nama:** OpenStreetMap
- **URL:** https://www.openstreetmap.org/
- **Endpoint API:** https://overpass-api.de/api/interpreter
- **Penerbit:** OpenStreetMap contributors
- **Atribusi:** © OpenStreetMap contributors

## 2. Tanggal dan jam akses

2026-11-16 WITA (sama dengan waktu_akuisisi di docs/provenance.json)

## 3. Metode akuisisi

- **Jenis:** API resmi, Overpass API tanpa API key
- **Parameter:** query Overpass QL untuk objek dengan tag amenity=cafe dan amenity=restaurant di wilayah Kota Denpasar, output JSON, timeout 60 detik
- **Kode memakai** timeout, User-Agent dengan nama dan NIM pengambil, penanganan status code, dan jeda minimal 1 detik antar-request. Hanya memakai satu request utama agar tidak membebani server.
- **Wilayah:** Kota Denpasar, Bali

## 4. Batasan etika

- **Ketentuan:** ODbL, wajib atribusi © OpenStreetMap contributors; jangan mengirim query berulang
- **Lisensi:** Open Database License (ODbL); atribusi dicantumkan di atas
- **Data pribadi:** tidak diambil. Nama orang, nomor telepon, email, foto, dan akun media sosial perorangan tidak menjadi target pengumpulan, walaupun terlihat di sumber
- **Keterbatasan:** data bergantung pada kelengkapan kontribusi OpenStreetMap; alamat yang kosong di sumber dibiarkan kosong dan tidak dibuat-buat; cakupan hanya objek yang memiliki tag amenity=cafe atau amenity=restaurant di Denpasar

## 5. Penjelasan kolom (data/raw/osm_20261116.csv)

| Kolom | Tipe | Arti |
| --- | --- | --- |
| osm_id | angka | ID unik objek di OpenStreetMap |
| name | teks | Nama cafe / restaurant |
| amenity | teks | Jenis amenity: cafe / restaurant |
| cuisine | teks | Jenis masakan |
| addr_street | teks | Nama jalan |
| addr_suburb | teks | Kelurahan / area |
| phone | teks | Nomor telepon |
| website | teks | Website |
| opening_hours | teks | Jam buka |
| latitude | angka | Lintang |
| longitude | angka | Bujur |
