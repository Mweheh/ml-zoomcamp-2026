# HW5 — Deploying Machine Learning Models

Sumber soal dan artefak resmi: [HW5 2026](https://github.com/DataTalksClub/machine-learning-zoomcamp/tree/main/cohorts/2026/homework/05-deployment)

## Jawaban

| Soal | Jawaban | Status pemeriksaan |
|---|---|---|
| Q1 | Catat hasil lokal `uv --version` | Setup check, tidak dinilai; belum berhasil dibaca pada sesi ini |
| Q2 | `1.7.2` | Cocok dengan lockfile dan environment lokal Python 3.11.15 |
| Q3 | `0.533` | Model resmi dimuat; probability aktual 0.532994 |
| Q4 | `0.770` | Handler API diuji langsung dengan payload resmi; probability aktual 0.769799, response memuat probability dan boolean conversion |
| Q5 | `python:3.11.15-slim-bookworm` | Cocok dengan Dockerfile resmi |
| Q6 | Belum dapat disahkan | Docker Engine tidak tersedia, jadi container dan endpoint container belum dijalankan |

Pemeriksaan model lokal: SHA256 pipeline cocok dengan nilai resmi `1646bbdcd38d4f044da6b630c5b332c93a314245a8c21929011c42de51f629f1`; environment pengujian Python 3.11.15 / scikit-learn 1.7.2.

## Sisa langkah manual untuk menuntaskan Q6

Pasang/aktifkan Docker Desktop, buka terminal di folder HW5 setelah artefak resmi tersedia, lalu jalankan:

```bash
docker build -t zoomcamp-model:2026-hw5 .
docker run --rm -p 9696:9696 zoomcamp-model:2026-hw5
```

Di terminal kedua:

```bash
python q6_test.py
curl -s http://localhost:9696/health
```

Pastikan health berstatus `ok`, checksum model sesuai metadata, dan request kedua menghasilkan probability sekitar `0.769799` (submit `0.770`). Jangan menandai Q6 selesai sebelum respons dari container benar-benar terlihat.

## Review terhadap soal

Payload Q3 dan Q4 diambil dari HW resmi; Q3 dijalankan dengan model terpin. Untuk Q4, fungsi handler diuji secara langsung; server HTTP dan container belum diuji. Deadline course yang tercantum adalah 26 Okt 2026; halaman kursus menunjukkan HW5 masih Open.

## Yang perlu kamu lakukan

- Verifikasi Q6 di container memakai langkah di atas.
- Buat post/screenshot learning-in-public, pakai `#mlzoomcamp`, tag Alexey Grigorev atau DataTalksClub, kemudian submit form [HW5](https://courses.datatalks.club/ml-zoomcamp-2026/homework/hw05). URL repo ini bisa dipakai pada kolom Homework URL.
