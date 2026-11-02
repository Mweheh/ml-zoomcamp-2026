# HW4 — Evaluation Metrics for Classification

Sumber soal: [HW4 2026 resmi](https://github.com/DataTalksClub/machine-learning-zoomcamp/blob/main/cohorts/2026/homework/04-evaluation/homework.md)

Data yang digunakan adalah release resmi 2026 `course_lead_scoring_2026.csv`. Mengikuti split `train_test_split` persis seperti instruksi; missing kategori diisi `NA`, numerik `0.0`. Model: DictVectorizer + LogisticRegression(solver="liblinear", C=1.0, max_iter=1000).

## Jawaban

| Soal | Jawaban | Hasil terukur |
|---|---|---|
| Q1 | `lead_score` | AUC `lead_score=0.788225`; tertinggi dari empat fitur |
| Q2 | `0.732` | validation ROC AUC `0.731822` |
| Q3 | `0.63` | selisih precision-recall terkecil setelah mengecualikan pasangan nol |
| Q4 | `0.41` | F1 maksimum `0.757616` |
| Q5 | `0.007` | std populasi lima fold `0.006853` |
| Q6 | `0.001` | mean ROC AUC terbaik dari C `[1e-6, 0.001, 1]` |

### Bukti ringkas

- Q1 AUC: number_of_courses_viewed 0.722989; annual_income 0.608198; interaction_count 0.764920; lead_score 0.788225.
- Q2 validation AUC: 0.731822.
- Q5 fold AUC: 0.730560, 0.729573, 0.736343, 0.741245, 0.720914; std ddof=0: 0.006853.
- Q6 mean AUC: C=1e-6 → 0.616734; C=0.001 → 0.749172; C=1 → 0.731727.

## Review terhadap soal

Split, imputasi, model, threshold grid 0.00–1.00 (langkah 0.01), KFold 5-fold dan pilihan C mengikuti HW resmi. Ambang precision/recall dihitung manual agar kompatibel dengan versi scikit-learn saat ini. Deadline course yang tercantum adalah 19 Okt 2026; halaman kursus menunjukkan HW4 masih Open.

## Yang perlu kamu lakukan

1. Buat post/screenshot/notebook excerpt learning-in-public dengan `#mlzoomcamp` dan tag Alexey Grigorev atau DataTalksClub.
2. Submit jawaban dan tautan post di [form HW4](https://courses.datatalks.club/ml-zoomcamp-2026/homework/hw04). URL repo ini bisa dipakai pada kolom Homework URL.
