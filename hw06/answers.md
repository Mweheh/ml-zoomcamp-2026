# HW6 — Decision Trees and Ensemble Learning

Sumber soal: [HW6 2026 resmi](https://github.com/DataTalksClub/machine-learning-zoomcamp/blob/main/cohorts/2026/homework/06-trees/homework.md)

Dataset resmi yang diminta: `car_fuel_efficiency_2026.csv`. Persiapan mengikuti instruksi: missing values menjadi nol, split persis sesuai seed 1, DictVectorizer sparse.

## Hasil yang sudah terverifikasi

| Soal | Hasil | Status |
|---|---|---|
| Q1 | `model_year` | Terverifikasi: fitur split decision tree depth 1 |
| Q2 | `1.837` | Terverifikasi: RMSE random forest 10 trees, seed 1 = 1.837054 |
| Q3 | Belum final | Dari 10 vs 50 trees, RMSE 10 = 1.837054 dan 50 = 1.771567. Belum menjalankan 100 dan 150; jangan pilih jawaban sebelum lengkap |
| Q4 | Belum dijalankan | Grid 4 depth × 4 jumlah trees belum selesai |
| Q5 | Belum dijalankan | Feature importance model 10 trees, depth 20 belum selesai |
| Q6 | Belum dijalankan | Perbandingan XGBoost eta 0.3 dan 0.1 belum selesai |

## Kenapa validasi berhenti

Dua percobaan grid Random Forest memerlukan waktu berlebihan pada mesin ini. Percobaan pertama memakai worker paralel yang tertinggal setelah proses utama diinterupsi; percobaan kedua berjalan serial tetapi tetap terlalu lambat. Karena hasil grid tidak lengkap, Q3–Q6 tidak saya isi dengan tebakan.

## Langkah manual untuk menuntaskan

Jalankan notebook/script HW6 pada komputer dengan runtime yang memadai dan ikuti jumlah estimator, depth, seed, serta 100 boosting rounds persis sesuai [instruksi resmi](https://github.com/DataTalksClub/machine-learning-zoomcamp/blob/main/cohorts/2026/homework/06-trees/homework.md). Catat RMSE setiap kombinasi, feature importance, dan RMSE kedua nilai eta. Setelah itu pilih opsi jawaban yang paling dekat sesuai instruksi. Hindari `n_jobs=-1` jika mesin membiarkan worker tidak terkendali.

Terakhir, buat post/screenshot learning-in-public dengan `#mlzoomcamp`, tag Alexey Grigorev atau DataTalksClub, dan submit form [HW6](https://courses.datatalks.club/ml-zoomcamp-2026/homework/hw06). URL repo dapat digunakan pada kolom Homework URL. Deadline yang tercantum adalah 2 Nov 2026; halaman kursus menunjukkan HW6 masih Open.
