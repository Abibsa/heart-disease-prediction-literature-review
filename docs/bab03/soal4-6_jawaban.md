# Jawaban Soal 4, 5, dan 6 (Subbab 3.11: Latihan Soal Bab III)

**Nama**: Muhammad Ashab Ibnu Abdul Aziz  
**NIM**: 231240001399  
**Mata Kuliah**: Pemrograman Mobile Lanjut — UNISNU Jepara  

---

Dokumen ini memuat jawaban analitis untuk **Latihan Soal 4, 5, dan 6** pada materi studi literatur dan riset data (Subbab 3.11), serta sintesis lanjutan rumusan masalah penelitian berdasarkan studi literatur 10 artikel terverifikasi.

---

## Soal 4: Tiga Saringan Kelayakan Ide Penelitian Berbasis Data

> **Pertanyaan**:  
> *Jelaskan tiga saringan kelayakan ide penelitian berbasis data dan berikan contoh gagasan yang gagal pada masing-masing saringan.*

### Penjelasan dan Contoh

Sebuah ide penelitian berbasis data hanya layak maju menjadi topik penelitian (khususnya skripsi) jika berhasil lolos tiga saringan sederhana yang saling terkait (Buku Ajar Subbab 3.2):

### 1. Saringan Pertama: Ketersediaan Data (*Data Availability & Legality*)
- **Penjelasan**: Peneliti harus memastikan bahwa data benar-benar dapat diakses, diperoleh secara legal, memiliki izin atau lisensi yang jelas, dan bukan sekadar data yang "dijanjikan" oleh pihak eksternal tanpa kepastian hukum.
- **Contoh Gagasan yang GAGAL**:  
  > *Contoh*: Mahasiswa mengusulkan judul *"Prediksi Loyalitas Nasabah VIP Bank X Menggunakan Deep Learning"*, namun Bank X memiliki kebijakan privasi perbankan ketat (UU PDP / Rahasia Bank) yang melarang keras pengeluaran data transaksi nasabah ke pihak luar. Hingga pertengahan semester surat izin ditolak dan data tidak pernah didapatkan, sehingga penelitian batal di tengah jalan.

### 2. Saringan Kedua: Kebermaknaan (*Meaningfulness / Value*)
- **Penjelasan**: Hasil penelitian harus memberikan kegunaan nyata (*actionable insight*) atau manfaat praktis/teoretis bagi pihak tertentu (industri, masyarakat, atau sains), bukan sekadar mengolah data tanpa implikasi solusi.
- **Contoh Gagasan yang GAGAL**:  
  > *Contoh*: Mahasiswa meneliti *"Klasifikasi Warna Pakaian Mahasiswa yang Masuk Kampus Menggunakan K-Nearest Neighbors"*. Meskipun data video CCTV tersedia dan model dapat dibuat, hasil klasifikasi warna baju tidak memiliki manfaat nyata bagi perbaikan sistem akademik, keamanan kampus, maupun pengambilan keputusan institusi.

### 3. Saringan Ketiga: Kelayakan Teknis (*Technical Feasibility*)
- **Penjelasan**: Kompleksitas komputasi, volume data, kebutuhan perangkat keras (*hardware* GPU/RAM), serta alokasi waktu (umumnya 1 semester / 4–6 bulan bagi skripsi sarjana) harus realistis dan dapat diselesaikan oleh mahasiswa.
- **Contoh Gagasan yang GAGAL**:  
  > *Contoh*: Mahasiswa mengusulkan *"Pelatihan Ulang Arsitektur Fondasi Large Language Model Multimodal 70 Miliar Parameter dari Nol (Scratch) untuk Analisis Bahasa Daerah Jepara"*. Gagasan ini bermakna dan datanya mungkin ada, tetapi melatih model berukuran tersebut membutuhkan kluster GPU bernilai ratusan juta rupiah dan waktu komputasi berbulan-bulan yang mustahil diselesaikan dalam kurun satu semester dengan laptop standar mahasiswa.

---

## Soal 5: Alasan Pemilihan Dataset UCI untuk Riset Komparasi Algoritma

> **Pertanyaan**:  
> *Mengapa dataset UCI sering dipilih untuk skripsi yang membandingkan algoritma? Jelaskan dengan konsep perbandingan hasil antar penelitian.*

### Penjelasan Berdasarkan Konsep *Benchmark* dan *Fair Comparison*

Repositori *UCI Machine Learning Repository* telah menjadi standar emas (*de facto benchmark*) dalam literatur penambangan data internasional selama lebih dari tiga dekade karena alasan-alasan fundamental berikut:

1. **Tolok Ukur Standar (*Common Baseline & Benchmark*)**:  
   Untuk membuktikan bahwa suatu algoritma baru atau modifikasi (misalnya *Random Forest + Bayesian Optimization*) benar-benar unggul, pengujian harus dilakukan pada "medan uji" yang telah diketahui karakteristiknya oleh komunitas ilmiah. Dataset UCI seperti *Cleveland Heart Disease* (303 baris, 13 fitur) menyediakan tolok ukur yang telah diuji oleh ribuan peneliti terdahulu (seperti Naik et al., 2025; Chandrasekhar & Peddakrishna, 2023; Parapak et al., 2025).

2. **Keadilan Perbandingan (*Fair Comparison & Controlled Environment*)**:  
   Jika peneliti menggunakan data internal yang privat, pembaca atau penguji tidak dapat memverifikasi apakah akurasi tinggi disebabkan oleh kehebatan algoritma atau sekadar kemudahan datanya (*data leak / over-optimistic distribution*). Pada dataset UCI, seluruh atribut, label, dan distribusi kelas terdefinisi secara transparan, sehingga perbedaan performa murni mencerminkan keunggulan metodologi dan pra-pemrosesan.

3. **Replikasi dan Perluasan Riset (*Reproducibility & Extension*)**:  
   Sesuai prinsip sains, riset yang baik harus dapat direproduksi (*reproducible*). Dengan dataset UCI, penguji, dosen pembimbing, maupun peneliti lain di seluruh dunia dapat mengunduh berkas data yang identik, menjalankan kode program yang sama, dan memverifikasi klaim metrik (akurasi, F1, AUC) secara langsung.

---

## Soal 6: Studi Kasus Integritas Akademik dan Penanganan Halusinasi AI

> **Pertanyaan**:  
> *Studi kasus: AI memberi Anda lima referensi; tiga ditemukan persis di Google Scholar, satu ditemukan tetapi isi artikelnya berbeda dari klaim AI, dan satu tidak pernah ditemukan. Bagaimana perlakuan Anda terhadap masing-masing, dan apa yang Anda laporkan tentang penggunaan AI tersebut?*

### 1. Perlakuan Terhadap Masing-Masing Referensi

Sesuai prosedur verifikasi sitasi pada Subbab 3.7 Buku Ajar:

- **Kasus A (3 Referensi Ditemukan Persis di Google Scholar / Basis Data Resmi)**:  
  - *Tindakan*: Jangan langsung disalin mentah-mentah. Buka tautan DOI resminya, periksa nama penulis, judul, jurnal, volume, dan tahun terbit. Unduh dan baca minimal bagian **abstrak dan metodologi**. Pastikan angka dan temuan yang dikutip benar-benar ada di teks asli. Setelah terbukti akurat, simpan metadata ke manajer referensi (Zotero/Mendeley) dan tandai statusnya sebagai **TERVERIFIKASI**.

- **Kasus B (1 Referensi Ditemukan, Tetapi Isinya Berbeda dari Klaim AI)**:  
  - *Tindakan*: **Waspadai halusinasi konten (*misattribution*)**. AI sering mengambil artikel nyata namun mengaitkannya dengan hasil eksperimen, dataset, atau metrik yang salah. Baca isi artikel yang sebenarnya: jika topik aslinya ternyata masih relevan dengan penelitian, perbaiki kutipan dan sitasi sesuai isi naskah asli. Namun, jika isi artikel berbeda domain/topik dari yang dibutuhkan, **keluarkan referensi tersebut dari daftar pustaka** dan jangan gunakan klaim palsu AI.

- **Kasus C (1 Referensi Tidak Pernah Ditemukan Sama Sekali)**:  
  - *Tindakan*: **Identifikasi sebagai halusinasi total (*fabricated reference*)**. Model bahasa besar sering merangkai nama penulis sungguhan dengan judul fiktif yang terdengar sangat meyakinkan. Artikel ini **wajib dibuang sepenuhnya** dan dilarang keras dicantumkan dalam daftar pustaka atau skripsi. Mengutip artikel fiktif merupakan pelanggaran integritas akademik serius (*scientific misconduct*).

### 2. Hal yang Wajib Dilaporkan dalam Log Penggunaan AI (*Transparency*)

Sebagai bentuk kejujuran akademik, peneliti wajib menyusun laporan dokumentasi atau log transparansi penggunaan AI yang memuat:
1. **Peran AI**: Menjelaskan bahwa AI digunakan sebagai alat bantu pencarian awal (*brainstorming* kata kunci dan kandidat artikel).
2. **Keterbukaan atas Halusinasi**: Melaporkan secara transparan bahwa dari 5 referensi yang disarankan, 1 referensi fiktif telah digugurkan dan 1 referensi telah dikoreksi isinya setelah verifikasi manual.
3. **Metode Verifikasi**: Menjelaskan kanal verifikasi manusia yang digunakan (misalnya Crossref API, PubMed PMID, pengecekan DOI langsung).
4. **Tanggung Jawab Penulis**: Menegaskan bahwa seluruh sitasi yang akhirnya dipakai dalam laporan adalah tanggung jawab penuh mahasiswa yang telah membaca dan mengonfirmasi sumber primernya.

---

## Bagian Lanjutan: Rumusan Masalah, Kerangka Pemikiran, dan Kontribusi Riset (Studi Kasus Penyakit Jantung)

Sebagai penerapan konkret dari sintesis 10 artikel terverifikasi pada Soal 2 dan Soal 3, berikut dirumuskan proposal penelitian berbasis data Cleveland Heart Disease:

### A. Rumusan Masalah Riset
1. Bagaimana kinerja algoritma *Random Forest* yang dioptimasi menggunakan kombinasi penyeimbangan data *SMOTE* dan *Bayesian Optimization* pada dataset UCI Cleveland?
2. Bagaimana pengaruh penerapan *Explainable AI* berbasis SHAP (*SHapley Additive exPlanations*) dalam memberikan interpretasi fitur klinis risiko penyakit jantung secara transparan?
3. Bagaimana perbandingan performa model teroptimasi yang diusulkan terhadap model *state-of-the-art* dalam literatur (Naik et al., Chandrasekhar & Peddakrishna, dan Parapak et al.)?

### B. Kerangka Pemikiran (*Conceptual Framework*)
```text
┌─────────────────────────────────────────────────────────────────┐
│                     MASALAH KLINIS & DATA                       │
│  Penyakit Jantung: Penyebab kematian #1 di Indonesia dan dunia   │
│  Deteksi dini membutuhkan model ML akurat, seimbang & transparan│
└────────────────────────────────┬────────────────────────────────┘
                                 │
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                    STUDI LITERATUR (10 ARTIKEL)                 │
│  • Ensemble RF & Extra Trees terbukti unggul (Parapak et al.)   │
│  • Optimasi metaheuristik mendongkrak akurasi (Naik et al.)      │
│  • Gap: Ketiadaan interpretabilitas klinis (Explainable AI)      │
└────────────────────────────────┬────────────────────────────────┘
                                 │
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                      PENDEKATAN DIUSULKAN                       │
│      Pipeline: UCI Cleveland -> SMOTE -> Bayesian RF -> SHAP    │
└────────────────────────────────┬────────────────────────────────┘
                                 │
         ┌───────────────────────┼───────────────────────┐
         ▼                       ▼                       ▼
  ┌─────────────┐         ┌─────────────┐         ┌─────────────┐
  │ Preprocessing│        │  Modeling   │         │ Interpretasi│
  │ Missing val,│         │ Bayesian RF │         │ Analisis    │
  │ Normalisasi,│         │ (Optuna)    │         │ SHAP Global │
  │ & SMOTE     │         │ 5-Fold CV   │         │ & Lokal     │
  └─────────────┘         └─────────────┘         └─────────────┘
                                 │
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                      EVALUASI & KONTRIBUSI                      │
│  • Metrik: Akurasi (≥93%), Presisi, Recall, F1, dan ROC-AUC     │
│  • Model transparan dan dapat dipahami oleh praktisi medis      │
└─────────────────────────────────────────────────────────────────┘
```

### C. Kontribusi Penelitian
- **Kontribusi Teoretis/Metodologis**: Mengintegrasikan algoritma penyeimbangan kelas adaptif dengan *Bayesian Optimization* pada Random Forest serta menyediakan lapisan interpretabilitas *SHAP* untuk mengurangi sifat "black-box" model medis.
- **Kontribusi Praktis**: Menghasilkan model klasifikasi terstandar yang siap diintegrasikan sebagai modul pendukung keputusan klinis (*Clinical Decision Support System*) pada fasilitas kesehatan primer.

---
*Dokumen ini merupakan bagian dari Latihan Soal Bab III: Identifikasi Masalah dan Studi Literatur.*
