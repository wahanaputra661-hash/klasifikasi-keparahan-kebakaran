# Klasifikasi Tingkat Keparahan Kebakaran Hutan dan Lahan di Indonesia

Project akhir mata kuliah Kecerdasan Artifisial, S1 Sains Data, Universitas Negeri Surabaya (Gasal 2026/2027).

Project ini mengklasifikasikan tingkat keparahan setiap kejadian kebakaran hutan dan lahan di Indonesia ke dalam tiga kelas (rendah, sedang, tinggi) berdasarkan faktor spasial, temporal, dan lingkungan, lalu membandingkan tiga algoritma: Random Forest, Decision Tree, dan K-Nearest Neighbors.

## Tim

| Nama | NIM |
|---|---|
| Doni Wahana Putra | 25031554248 |
| Abdulah Mubarok | 250031554009 |
| Muhammad Raditya Rafli Aldiansyah | 25031554063 |

Dosen pengampu: [nama dosen]

## Status

Tahap 1 (pemaparan ide). Notebook saat ini membaca dataset, membentuk tabel per kejadian, dan membuat kelas keparahan. Pemodelan dan evaluasi dikerjakan pada tahap berikutnya.

## Dataset

Dataset tidak disertakan di repositori karena ukurannya besar. Unduh sendiri dari Dryad:

- Cattau, M. E. dan Sloan, S. (2022). Discrete fire events, their severity, and their ignitions (Indonesia, 2002–2019). https://doi.org/10.5061/dryad.msbcc2g1t

Dua berkas yang dipakai:

| Berkas | Baris | Kolom |
|---|---|---|
| nfire4_all_spatial_fire_2002_2019_joins_sp_LC.csv | 1.232.377 | 49 |
| nfire4_all_spatial_fire_2002_2019_igs_sp_LC.csv | 720.795 | 31 |

Setelah diringkas per kejadian (nfireID2), diperoleh 484.366 kejadian unik.

Data pendukung yang direncanakan: ERA5-Land (https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land).

## Kelas keparahan

Kelas dibentuk dari FRP_Days dengan batas persentil ke-33,3 dan ke-66,7.

| Kelas | Batas FRP_Days | Jumlah |
|---|---|---|
| Rendah | ≤ 14,0 | 161.963 |
| Sedang | > 14,0 dan ≤ 41,6 | 161.013 |
| Tinggi | > 41,6 | 161.390 |

## Cara menjalankan

Notebook dijalankan di Google Colab.

1. Unduh dua CSV dari Dryad, lalu unggah ke Google Drive (folder bebas).
2. Buka `notebook/pre_project_kebakaran_colab.ipynb` di Google Colab.
3. Jalankan semua sel dari atas. Izinkan akses Drive saat diminta.
4. Notebook mencari dua CSV di Drive berdasarkan nama berkas, jadi path tidak perlu diubah.

Pustaka yang dipakai: pandas, seaborn, matplotlib (sudah tersedia di Colab).

## Isi notebook

1. Menyambungkan Colab ke Google Drive.
2. Fungsi untuk menampilkan tabel.
3. Membaca dua CSV, meringkas menjadi satu baris per kejadian, dan membentuk kelas keparahan.
4. Ringkasan baris dan kolom serta batas persentil.
5. Distribusi kelas dalam bentuk grafik dan tabel.

## Referensi

Daftar lengkap ada di laporan (bagian Daftar Pustaka).
