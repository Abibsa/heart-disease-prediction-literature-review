# Soal 2 — Penelusuran Literatur

**Nama**: Muhammad Ashab Ibnu Abdul Aziz  
**NIM**: 231240001399  
**Mata Kuliah**: Metodologi Penelitian (24TIF505) — UNISNU Jepara  

---

## 2.1 Topik Penelitian

**"Prediksi Penyakit Jantung Menggunakan Algoritma Random Forest dan Metode Machine Learning Lainnya pada Dataset UCI Cleveland"**

Topik ini dirumuskan berdasarkan ketersediaan data benchmark klasik *UCI Heart Disease (Cleveland)* yang telah dianalisis pada Soal 1, dengan fokus pada eksplorasi performa algoritma *supervised learning* berbasis pohon keputusan (*ensemble*) dan optimasi hiperparameter.

---

## 2.2 Strategi Pencarian Literatur

### Basis Data dan Antarmuka Pencarian
Untuk memastikan literatur yang dikumpulkan sahih, bebas dari halusinasi sitasi, dan mencakup publikasi nasional maupun internasional, penelusuran dilakukan melalui:
1. **OpenAlex API** — Basis data bibliografi terbuka global yang mengindeks lebih dari 250 juta karya ilmiah, termasuk ribuan jurnal nasional terakreditasi di Indonesia.
2. **Crossref API** — Lembaga registrasi DOI internasional untuk memverifikasi keaslian naskah, volume, nomor terbitan, dan tahun.
3. **PubMed / MEDLINE** — Basis data biomedis resmi *National Library of Medicine* (NLM/NIH) untuk verifikasi indeks medis (PMID).
4. **Portal Jurnal Indonesia (OJS & Sinta-indexed)** — Penelusuran publikasi terbitan perguruan tinggi di Indonesia.

### Query Boolean yang Digunakan
Kombinasi kata kunci disusun menggunakan logika Boolean untuk menyaring artikel yang relevan:

```text
("heart disease" OR "cardiovascular disease" OR "penyakit jantung")
AND
("prediction" OR "classification" OR "klasifikasi" OR "prediksi")
AND
("machine learning" OR "random forest" OR "ensemble" OR "boosting")
AND
("Cleveland" OR "UCI" OR "dataset")
```

### Kriteria Inklusi dan Eksklusi

| Parameter | Kriteria Inklusi | Kriteria Eksklusi |
|:----------|:-----------------|:------------------|
| **Rentang Tahun** | 2021–2026 (5 tahun terakhir) | Sebelum tahun 2021 |
| **Jenis Dokumen** | Artikel jurnal ilmiah primer (*peer-reviewed*) | Skripsi/tesis yang belum diterbitkan, artikel opini, blog |
| **Akses** | *Open Access* atau metadata lengkap terverifikasi | Artikel tanpa DOI resmi atau teks lengkap tidak jelas |
| **Bahasa** | Bahasa Indonesia dan Bahasa Inggris | Bahasa selain Indonesia dan Inggris |
| **Dataset** | Dataset UCI Heart Disease (Cleveland) atau varian CVD benchmark | Dataset non-medis atau dataset tanpa deskripsi fitur |
| **Komposisi Wilayah** | **Minimal 3 artikel dari jurnal nasional Indonesia** | Kurang dari 3 artikel jurnal Indonesia |

---

## 2.3 Hasil Penelusuran (10 Artikel Terpilih)

Dari 84 kandidat artikel yang disaring melalui penelusuran OpenAlex API dan Crossref API (terekam pada [docs/kandidat_jurnal.csv](../kandidat_jurnal.csv)), dipilih **10 artikel primer** yang memiliki kesesuaian metodologis tertinggi dengan topik penelitian. Seluruh artikel telah berstatus **TERVERIFIKASI** pada basis data Crossref dan OpenAlex.

### Tabel 10 Artikel Terverifikasi

| No | Penulis (Tahun) | Judul Artikel | Nama Jurnal | Asal Jurnal | DOI |
|:--:|:----------------|:--------------|:------------|:-----------:|:----|
| 1 | Parapak, Robet, & Hendrik (2025) | *Application of Bagging and Boosting Methods for Heart Disease Classification* | *Journal of Applied Computer Science and Technology* (JACOST) | **Indonesia** | `10.52158/we9asn06` |
| 2 | Nursyahrina et al. (2024) | *MODELING HEART DISEASE CLASSIFICATION USING ROUGH NEURAL NETWORK: A DATA-DRIVEN APPROACH TO THE CLEVELAND HEART DISEASE DATASET* | *Jurnal Sistem Informasi dan Ilmu Komputer Prima* (JUSIKOM PRIMA) | **Indonesia** | `10.34012/jurnalsisteminformasidanilmukomputer.v7i2.4848` |
| 3 | Ramadhan et al. (2024) | *Comparison of Machine Learning Models for Heart Disease Classification with Web-Based Implementation* | *Journal of Applied Informatics and Computing* (JAIC) | **Indonesia** | `10.30871/jaic.v8i2.8744` |
| 4 | Narasimhan & Victor (2025) | *A hybrid approach with metaheuristic optimization and random forest in improving heart disease prediction* | *Scientific Reports* (Nature Portfolio) | Internasional | `10.1038/s41598-024-73867-x` |
| 5 | Naik, Tejani, & Mousavirad (2025) | *SGO enhanced random forest and extreme gradient boosting framework for heart disease prediction* | *Scientific Reports* (Nature Portfolio) | Internasional | `10.1038/s41598-025-02525-7` |
| 6 | Bouqentar et al. (2024) | *Early heart disease prediction using feature engineering and machine learning algorithms* | *Heliyon* (Elsevier) | Internasional | `10.1016/j.heliyon.2024.e38731` |
| 7 | Li, Chen, & Xu (2024) | *Coronary heart disease prediction based on hybrid deep learning* | *Review of Scientific Instruments* (AIP) | Internasional | `10.1063/5.0172368` |
| 8 | Yasmeen, Khan, & Choi (2025) | *Heart disease prediction using hybrid TabNet architecture with stacked ensemble learning* | *Frontiers in Physiology* | Internasional | `10.3389/fphys.2025.1665128` |
| 9 | Chandrasekhar & Peddakrishna (2023) | *Enhancing Heart Disease Prediction Accuracy through Machine Learning Techniques and Optimization* | *Processes* (MDPI) | Internasional | `10.3390/pr11041210` |
| 10 | Paladino et al. (2023) | *Evaluating the Performance of Automated Machine Learning (AutoML) Tools for Heart Disease Diagnosis and Prediction* | *AI* (MDPI) | Internasional | `10.3390/ai4040053` |

---

## 2.4 Analisis Pemenuhan Syarat

1. **Pemenuhan Syarat Jurnal Indonesia**:
   - Artikel #1 (*Parapak et al., 2025*) terbit di *Journal of Applied Computer Science and Technology* (JACOST), Universitas Kristen Indonesia Toraja.
   - Artikel #2 (*Nursyahrina et al., 2024*) terbit di *Jurnal Sistem Informasi dan Ilmu Komputer Prima* (JUSIKOM PRIMA), Universitas Prima Indonesia Medan.
   - Artikel #3 (*Ramadhan et al., 2024*) terbit di *Journal of Applied Informatics and Computing* (JAIC), Politeknik Negeri Batam.
   Ketiga artikel tersebut diterbitkan oleh jurnal ber-ISSN resmi di Indonesia dan meneliti klasifikasi penyakit jantung secara komparatif.

2. **Keterkaitan Erat dengan Dataset Benchmark Cleveland**:
   Mayoritas artikel di atas secara langsung dan eksplisit menggunakan dataset **UCI Heart Disease (Cleveland)**:
   - Parapak et al. (2025), Nursyahrina et al. (2024), Narasimhan & Victor (2025), Naik et al. (2025), Bouqentar et al. (2024), Yasmeen et al. (2025), Chandrasekhar & Peddakrishna (2023), dan Paladino et al. (2023) seluruhnya memanfaatkan dataset Cleveland sebagai tolok ukur utama.
   Hal ini menjamin bahwa sintesis literatur pada Soal 3 dan usulan masalah pada Soal 4 berpijak pada data yang sama persis dengan yang diunduh pada Soal 1.

---

## 2.5 Manajemen Referensi

Seluruh metadata kesepuluh artikel disimpan dalam dua format standar yang kompatibel dengan perangkat lunak pengelola referensi:
- **[`docs/references.bib`](../references.bib)** — Format BibTeX standar untuk LaTeX dan Overleaf.
- **[`docs/references.ris`](../references.ris)** — Format Research Information Systems (RIS) standar untuk Zotero, Mendeley, dan EndNote.

Bukti verifikasi dan tautan digital masing-masing artikel didokumentasikan secara rinci pada berkas **[`docs/verifikasi.md`](../verifikasi.md)**.

---
*Dokumen ini merupakan bagian dari Latihan Soal Bab III: Identifikasi Masalah dan Studi Literatur.*
