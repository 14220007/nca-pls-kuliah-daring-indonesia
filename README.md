# Syarat Perlu dan Faktor Penentu Keberhasilan Belajar Daring Mahasiswa Indonesia (NCA + PLS-SEM)

Data dan kode replikasi untuk artikel:

> Rumintarsih, A. (2026). *Syarat perlu dan faktor penentu keberhasilan belajar daring mahasiswa Indonesia: Pendekatan necessary condition analysis dan PLS-SEM* [Naskah dalam proses]. Fakultas Sistem Informasi.

## Isi repositori

| File | Isi |
|---|---|
| `Analisis_NCA_PLS_Kuliah_Daring.ipynb` | Notebook Jupyter lengkap: persiapan data, PLS-SEM, bootstrap, NCA, pemeriksaan tambahan, validasi |
| `Data_Indonesia_Global_Student_Survey_2020.csv` | Subsampel Indonesia (n = 604) dari Global Student Survey gelombang 1, beserta skor konstruk |
| `SmartPLS_Data_Indonesia_n209.csv` | 209 responden lengkap dengan nama butir pendek (TS1–LO3), siap diimpor ke SmartPLS |
| `Codebook_Variabel.csv` | Keterangan setiap kolom dan konstruk |
| `hasil/Hasil_Analisis_NCA_PLS.xlsx` | Semua tabel hasil (17 sheet) |
| `gambar/` | Gambar model penelitian, plot NCA, dan peta NCA vs PLS-SEM |
| `requirements.txt` | Paket Python yang dibutuhkan |

## Cara menjalankan

1. Pasang Python 3.10 atau lebih baru (misalnya lewat Anaconda).
2. Pasang paket: `pip install -r requirements.txt`
3. Buka `Analisis_NCA_PLS_Kuliah_Daring.ipynb` di Jupyter, dari folder yang sama dengan file CSV.
4. Jalankan **Kernel → Restart & Run All** (sekitar 3 menit).

Sel pertama berisi `FOLDER = r'F:\kuliah daring'`. Bila folder itu tidak ada di komputer Anda, notebook otomatis memakai folder tempat notebook berada.

*Seed* acak ditetapkan (2026), sehingga hasil *bootstrap* (5.000 sampel) dan uji permutasi NCA (10.000 kali) dapat direplikasi persis. Hasilnya sudah diuji identik di dua lingkungan (Python 3.11.8/numpy 1.26 dan Python 3.11.15/numpy 2.4).

## Sumber data

Data berasal dari:

> Aristovnik, A., Keržič, D., Ravšelj, D., Tomaževič, N., & Umek, L. (2021). Impacts of the Covid-19 pandemic on life of higher education students: Global survey dataset from the first wave. *Data in Brief, 39*, 107659. https://doi.org/10.1016/j.dib.2021.107659

Dataset asli tersedia di Mendeley Data (https://data.mendeley.com/datasets/88y3nffs82/5) dengan lisensi CC BY 4.0. Repositori ini hanya memuat subsampel Indonesia beserta skor konstruk turunan. Perubahan dari data asli:

- jawaban di luar 1–5 (termasuk "tidak berlaku") diubah menjadi kosong;
- butir Q20c dibalik (6 − nilai asli);
- kolom skor konstruk (TS, AS, SCO, ACO, LT, CS, WOR, PAE, NAE, LO) ditambahkan.

## Lisensi

- **Kode** (notebook): MIT License (lihat `LICENSE`).
- **Data**: CC BY 4.0, mengikuti lisensi dataset asli. Harap sitasi Aristovnik dkk. (2021) dan artikel ini bila memakai data.

## Sitasi

Lihat `CITATION.cff`. Setelah diunggah ke Zenodo, DOI repositori akan tercantum di sini.
