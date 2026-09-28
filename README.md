# ML Zoomcamp 2026

Repo ini khusus Machine Learning Zoomcamp 2026 dari DataTalksClub.

## HW1 — Introduction to Machine Learning

- [Notebook dengan output](hw01/hw01.ipynb)
- [Dataset resmi yang digunakan](hw01/car_fuel_efficiency_2026.csv)
- [Jawaban dan bukti numerik](hw01/answers.json)
- [Instruksi resmi](https://github.com/DataTalksClub/machine-learning-zoomcamp/blob/main/cohorts/2026/homework/01-intro/homework.md)
- [Form submission](https://courses.datatalks.club/ml-zoomcamp-2026/homework/hw01)

| Soal | Jawaban submission |
| --- | --- |
| Q1 | 3.0.5 |
| Q2 | 10000 |
| Q3 | 3 |
| Q4 | 2 |
| Q5 | 41.2 |
| Q6 | Yes, it decreased |
| Q7 | 0.369 |

Median horsepower berubah dari 254.0 menjadi 252.0 setelah nilai kosong diisi dengan mode 252.0. Jumlah bobot Q7 sebelum dipetakan ke pilihan jawaban adalah `0.36919696904925486`.

## Menjalankan ulang

Gunakan Python 3.14.5. Pasang dependency dari `requirements.txt`, buka `hw01/hw01.ipynb` di Jupyter, VS Code, atau Colab, lalu jalankan seluruh cell secara berurutan. Di Colab, unggah CSV ke direktori kerja sebelum menjalankan notebook. Versi Pandas untuk Q1 harus sesuai environment yang benar-benar digunakan.

```sh
python -m pip install -r requirements.txt
python -m pip install jupyterlab
python -m jupyterlab
```

Seluruh 9 cell kode sudah dijalankan melalui kernel Jupyter dari awal tanpa error, dan output disimpan di notebook. Q7 juga lolos perbandingan dengan `numpy.linalg.lstsq`. `answers.json` dibuat langsung oleh cell terakhir.

Dataset: file resmi `car_fuel_efficiency_2026.csv`, diambil dari repo DataTalksClub pada 29 September 2026. SHA-256: `00a5cab178a8b7cd6e9157ee71dabc236ba7f20b1832336d358b07af14ba431f`.

Notebook dan repo berisi hasil pengerjaan; keduanya tidak otomatis mengirim form course. Status submission harus dikonfirmasi pada platform setelah login.
