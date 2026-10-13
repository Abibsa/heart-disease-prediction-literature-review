# Soal 1 — Dokumentasi Dataset

**Nama**: Muhammad Ashab Ibnu Abdul Aziz  
**NIM**: 231240001399  
**Mata Kuliah**: Metodologi Penelitian (24TIF505) — UNISNU Jepara  

---

## 1.1 Paragraf Dokumentasi dan Hipotesis Masalah Penelitian

Dataset **Heart Disease (Cleveland)** diunduh dari repositori publik resmi **UCI Machine Learning Repository** (<https://archive.ics.uci.edu/dataset/45/heart+disease>, DOI: `10.24432/C52P4X`) pada tanggal **13 Oktober 2026** di bawah ketentuan lisensi terbuka **Creative Commons Attribution 4.0 International (CC BY 4.0)**. Dataset klasik ini mencakup 303 sampel rekam medis pasien dengan 13 fitur klinis (terdiri atas parameter demografis, hemodinamik, dan hasil uji diagnostik seperti `age`, `cp`, `trestbps`, `chol`, `thalach`, `ca`, serta `thal`) dan 1 atribut target diagnosis penyakit kardiovaskular (`num`). Hipotesis masalah yang dapat diteliti dari dataset ini adalah: *kombinasi algoritma ensemble pohon keputusan (seperti Random Forest) yang dioptimasi menggunakan penalaan hiperparameter Bayesian mampu mengklasifikasikan risiko penyakit jantung dengan tingkat akurasi mencapai ≥ 93% dan skor AUC ≥ 0,95, dengan atribut cacat perfusi thalassemia (`thal`), depresi segmen ST (`oldpeak`), dan jumlah pembuluh darah utama berfluoroskopi (`ca`) sebagai indikator klinis paling berpengaruh terhadap hasil prediksi.*

---

## 1.2 Identitas Dataset

| Atribut | Keterangan |
|---|---|
| **Nama Dataset** | Heart Disease (Cleveland Database) |
| **Sumber Repositori** | UCI Machine Learning Repository |
| **URL Resmi** | <https://archive.ics.uci.edu/dataset/45/heart+disease> |
| **DOI Dataset** | `10.24432/C52P4X` |
| **Lisensi** | Creative Commons Attribution 4.0 (CC BY 4.0) |
| **Tanggal Unduh** | 13 Oktober 2026 |
| **Format Asli** | Multivariate Data Table (diakses via `ucimlrepo`) |
| **Jumlah Instans** | 303 baris pasien |
| **Jumlah Fitur** | 13 fitur input + 1 variabel target |

---

## 1.3 Deskripsi Fitur

| No | Nama Fitur | Tipe Data | Deskripsi Klinis |
|:--:|:-----------|:----------|:-----------------|
| 1 | `age` | Kontinu (Numerik) | Usia pasien (dalam tahun) |
| 2 | `sex` | Kategorikal (Biner) | Jenis kelamin biologis (1 = laki-laki, 0 = perempuan) |
| 3 | `cp` | Kategorikal (Nominal) | Tipe nyeri dada: 1 = angina tipikal, 2 = angina atipikal, 3 = non-angina, 4 = asimptomatik |
| 4 | `trestbps` | Kontinu (Numerik) | Tekanan darah istirahat saat masuk rumah sakit (mm Hg) |
| 5 | `chol` | Kontinu (Numerik) | Kadar kolesterol serum (mg/dL) |
| 6 | `fbs` | Kategorikal (Biner) | Gula darah puasa > 120 mg/dL (1 = ya, 0 = tidak) |
| 7 | `restecg` | Kategorikal (Nominal) | Hasil elektrokardiografi istirahat (0 = normal, 1 = gelombang ST-T abnormal, 2 = hipertrofi ventrikel kiri) |
| 8 | `thalach` | Kontinu (Numerik) | Detak jantung maksimum yang dicapai saat uji beban (*exercise*) |
| 9 | `exang` | Kategorikal (Biner) | Terjadinya angina akibat aktivitas fisik (1 = ya, 0 = tidak) |
| 10 | `oldpeak` | Kontinu (Numerik) | Depresi segmen ST yang diinduksi latihan relatif terhadap saat istirahat |
| 11 | `slope` | Kategorikal (Ordinal) | Kemiringan segmen ST pada puncak latihan (1 = naik/upsloping, 2 = datar/flat, 3 = turun/downsloping) |
| 12 | `ca` | Kontinu / Diskrit | Jumlah pembuluh darah utama (0–3) yang diwarnai fluoroskopi |
| 13 | `thal` | Kategorikal (Nominal) | Hasil skintigrafi talium: 3 = normal, 6 = cacat permanen (*fixed defect*), 7 = cacat reversibel |
| 14 | `num` | **Target (Kategorikal)** | Diagnosis penyakit jantung: 0 = tidak ada penyakit (<50% diameter penyempitan pembuluh darah), 1–4 = ada penyakit jantung |

---

## 1.4 Analisis Missing Value

| Fitur | Jumlah Missing | Persentase | Status Penanganan |
|:------|:--------------:|:----------:|:------------------|
| `ca`  | 4              | 1,32 %     | Diimputasi median/modus (0) |
| `thal`| 2              | 0,66 %     | Diimputasi modus (3 / normal) |
| Fitur lainnya (12 fitur) | 0 | 0,00 % | Bersih |
| **Total Sel Missing** | **6** | **0,30 %** | Sangat rendah (dari 303 × 14 = 4.242 sel) |

---

## 1.5 Distribusi Kelas Target

### Distribusi Multi-kelas (Tingkat Keparahan)
- **Kelas 0** (Normal / Tidak Ada Penyakit): 164 sampel (54,13 %)
- **Kelas 1** (Tingkat Keparahan Ringan): 55 sampel (18,15 %)
- **Kelas 2** (Tingkat Keparahan Sedang): 36 sampel (11,88 %)
- **Kelas 3** (Tingkat Keparahan Berat): 35 sampel (11,55 %)
- **Kelas 4** (Tingkat Keparahan Kritis): 13 sampel (4,29 %)

### Distribusi Biner (Klasifikasi Diagnostik Standar)
- **Kelas 0 (Negatif / Sehat)**: 164 sampel (54,13 %)
- **Kelas 1 (Positif / Sakit Jantung)**: 139 sampel (45,87 %)

> **Catatan Analisis**: Distribusi kelas biner tergolong sangat seimbang (rasio 54% : 46%), sehingga model klasifikasi memiliki probabilitas belajar yang adil tanpa risiko bias ekstrem terhadap kelas mayoritas.

---

## 1.6 File Dataset yang Dihasilkan

Berkas data tersimpan di folder `data/`:
- [data/raw/heart_disease_cleveland.csv](../../data/raw/heart_disease_cleveland.csv) — Berkas dataset dalam format tabel CSV.
- [data/ringkasan_dataset.json](../../data/ringkasan_dataset.json) — Berkas metadata ringkasan statistik dataset.

---
*Dokumen ini merupakan bagian dari Latihan Soal Bab III: Identifikasi Masalah dan Studi Literatur.*
