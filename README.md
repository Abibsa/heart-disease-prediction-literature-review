# Tugas Bab III: Identifikasi Masalah dan Studi Literatur
## Mata Kuliah Metodologi Penelitian (24TIF505)

Repositori ini memuat hasil pengerjaan **Latihan Soal Bab III: Identifikasi Masalah dan Studi Literatur** berdasarkan buku ajar *Metodologi Penelitian: Riset Berbasis Data dan Data Mining untuk Informatika* (Akhmad Khanif Zyen, S.Kom., M.Kom., UNISNU Jepara, 2026).

---

## Identitas Mahasiswa

| Atribut | Keterangan |
|:--------|:-----------|
| **Nama Lengkap** | Muhammad Ashab Ibnu Abdul Aziz |
| **NIM** | 231240001399 |
| **Program Studi** | Teknik Informatika |
| **Fakultas** | Sains dan Teknologi |
| **Perguruan Tinggi** | Universitas Islam Nahdlatul Ulama (UNISNU) Jepara |
| **Mata Kuliah** | Metodologi Penelitian (24TIF505) |
| **Dosen Pengampu** | Akhmad Khanif Zyen, S.Kom., M.Kom. |

---

## Deskripsi Singkat Repositori

Proyek ini mendokumentasikan proses ilmiah identifikasi masalah dan penelusuran literatur pada penelitian *data mining* dan *machine learning*. Fokus kajian diarahkan pada deteksi dini risiko penyakit kardiovaskular menggunakan pendekatan algoritma *ensemble* teroptimasi berbasis data rekam medis pasien.

Seluruh literatur yang digunakan telah melalui proses verifikasi ganda melalui **OpenAlex API**, **Crossref REST API**, dan **PubMed**, menghasilkan 10 artikel primer yang 100% terverifikasi (mencakup **3 artikel dari jurnal nasional Indonesia ber-ISSN resmi** dan 7 artikel dari jurnal internasional bereputasi).

---

## Informasi Resmi Dataset

Dataset yang digunakan dalam penelitian ini adalah dataset tolok ukur (*benchmark*) standar internasional dari UCI Machine Learning Repository:

| Parameter | Keterangan Resmi UCI |
|:----------|:---------------------|
| **Nama Dataset** | Heart Disease (Cleveland Database) |
| **Repositori Asal** | UCI Machine Learning Repository |
| **URL Resmi** | [https://archive.ics.uci.edu/dataset/45/heart+disease](https://archive.ics.uci.edu/dataset/45/heart+disease) |
| **Digital Object Identifier (DOI)** | `10.24432/C52P4X` |
| **Lisensi Resmi** | Creative Commons Attribution 4.0 International (CC BY 4.0) |
| **Pemberi Hibah / Donatur Data** | Robert Detrano, M.D., Ph.D. (V.A. Medical Center, Long Beach and Cleveland Clinic Foundation) |
| **Dimensi Data** | 303 sampel instans pasien, 13 atribut fitur klinis + 1 atribut target diagnosis |
| **Tipe Tugas Pembelajaran Mesin** | Klasifikasi Biner / Multi-kelas |

---

## Pemetaan Soal dan Berkas Hasil

Tabel berikut memetakan setiap butir penugasan pada Bab III ke berkas yang relevan di dalam repositori:

| Butir Soal | Deskripsi Tugas | Berkas Hasil |
|:-----------|:----------------|:-------------|
| **Soal 1** | Pemilihan dataset publik, pengunduhan data, dokumentasi satu paragraf (sumber, lisensi, deskripsi singkat), dan perumusan hipotesis penelitian. | [`docs/bab03/soal1_dokumentasi_dataset.md`](docs/bab03/soal1_dokumentasi_dataset.md)<br>[`data/raw/heart_disease_cleveland.csv`](data/raw/heart_disease_cleveland.csv)<br>[`data/ringkasan_dataset.json`](data/ringkasan_dataset.json) |
| **Soal 2** | Penelusuran 10 artikel jurnal primer (2021–2026) dengan kata kunci Boolean, pemenuhan syarat minimal 3 jurnal Indonesia, dan ekspor manajer referensi. | [`docs/bab03/soal2_penelusuran_literatur.md`](docs/bab03/soal2_penelusuran_literatur.md)<br>[`docs/verifikasi.md`](docs/verifikasi.md)<br>[`docs/references.bib`](docs/references.bib)<br>[`docs/references.ris`](docs/references.ris)<br>[`docs/kandidat_jurnal.csv`](docs/kandidat_jurnal.csv) |
| **Soal 3** | Penyusunan tabel penelitian terdahulu komparatif (*Peneliti, Dataset, Algoritma, Metrik, Hasil, Celah*) dan sintesis celah penelitian (*research gap*). | [`docs/bab03/soal3_tabel_penelitian_terdahulu.md`](docs/bab03/soal3_tabel_penelitian_terdahulu.md)<br>[`docs/bab03/soal3_tabel_penelitian_terdahulu.xlsx`](docs/bab03/soal3_tabel_penelitian_terdahulu.xlsx) |
| **Soal 4** | Penjelasan 3 saringan kelayakan ide penelitian berbasis data (Ketersediaan data, Kebermaknaan, Kelayakan teknis) beserta contoh gagasan yang gagal. | [`docs/bab03/soal4-6_jawaban.md`](docs/bab03/soal4-6_jawaban.md) *(Subbab Soal 4)* |
| **Soal 5** | Analisis konseptual pemilihan dataset UCI dalam penelitian komparasi algoritma (*common baseline*, keadilan komparasi, dan replikasi). | [`docs/bab03/soal4-6_jawaban.md`](docs/bab03/soal4-6_jawaban.md) *(Subbab Soal 5)* |
| **Soal 6** | Studi kasus integritas akademik dan prosedur penanganan halusinasi referensi dari asisten AI (verifikasi primer, koreksi kutipan, dan eliminasi). | [`docs/bab03/soal4-6_jawaban.md`](docs/bab03/soal4-6_jawaban.md) *(Subbab Soal 6)* |

---

## Struktur Repositori

```text
bab3_latihan/
├── .gitignore
├── README.md
├── data/
│   ├── raw/
│   │   └── heart_disease_cleveland.csv
│   └── ringkasan_dataset.json
└── docs/
    ├── kandidat_jurnal.csv
    ├── references.bib
    ├── references.ris
    ├── verifikasi.md
    └── bab03/
        ├── soal1_dokumentasi_dataset.md
        ├── soal2_penelusuran_literatur.md
        ├── soal3_tabel_penelitian_terdahulu.md
        ├── soal3_tabel_penelitian_terdahulu.xlsx
        └── soal4-6_jawaban.md
```

---

## Status Verifikasi Literatur

- **Total Artikel Dianalisis**: 10 artikel jurnal primer (*peer-reviewed*).
- **Komposisi Wilayah**: 3 artikel dari jurnal nasional Indonesia (JACOST, JUSIKOM PRIMA, JAIC) + 7 artikel internasional bereputasi (*Nature Scientific Reports*, *Heliyon*, *Processes*, *AI*, *Review of Scientific Instruments*, *Frontiers in Physiology*).
- **Status Crossref & DOI**: 100% Terverifikasi (Daftar lengkap dan tautan digital dapat dilihat pada [`docs/verifikasi.md`](docs/verifikasi.md)).
