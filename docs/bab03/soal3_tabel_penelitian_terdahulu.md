# Soal 3 — Tabel Penelitian Terdahulu dan Celah Penelitian (*Research Gap*)

**Nama**: Muhammad Ashab Ibnu Abdul Aziz  
**NIM**: 231240001399  
**Mata Kuliah**: Pemrograman Mobile Lanjut — UNISNU Jepara  

---

## 3.1 Tabel Penelitian Terdahulu

Tabel berikut merangkum 10 artikel penelitian primer terkait klasifikasi dan prediksi penyakit jantung berbasis *machine learning*, mencakup 3 artikel dari jurnal nasional Indonesia dan 7 artikel dari jurnal internasional bereputasi. Seluruh artikel telah terverifikasi melalui Crossref dan OpenAlex API. Berkas tabel dalam format spreadsheet juga tersedia di [`soal3_tabel_penelitian_terdahulu.xlsx`](./soal3_tabel_penelitian_terdahulu.xlsx).

| No | Peneliti (Tahun) | Judul Artikel | Metode / Algoritma | Dataset | Hasil Utama | Celah / Keterbatasan Penelitian |
|:--:|:-----------------|:--------------|:-------------------|:--------|:------------|:--------------------------------|
| 1 | Parapak, Robet, & Hendrik (2025) | *Application of Bagging and Boosting Methods for Heart Disease Classification* | Bagging (Random Forest, Extra Trees, Bagged DT) vs Boosting (AdaBoost, GradBoost, XGBoost) + SMOTE | UCI Cleveland Heart Disease (303 sampel) | Extra Trees + SMOTE mencapai akurasi 90%, presisi 96%, recall 82%, dan F1-score 88% | Belum menguji optimasi hiperparameter lanjutan (Bayesian/metaheuristik); belum mengkaji interpretabilitas model (SHAP) |
| 2 | Nursyahrina et al. (2024) | *MODELING HEART DISEASE CLASSIFICATION USING ROUGH NEURAL NETWORK: A DATA-DRIVEN APPROACH TO THE CLEVELAND HEART DISEASE DATASET* | Rough Neural Network (RNN): Reduksi himpunan kasar (9 fitur) + Jaringan Saraf Tiruan | Cleveland Heart Disease Dataset | Model RNN mencapai akurasi 88,52%, F1-score 88,14%, dan AUC 88,85% (melampaui ANN standar) | Belum membandingkan dengan algoritma ensemble pohon keputusan mutakhir; evaluasi terbatas pada metrik tanpa analisis signifikansi statistik |
| 3 | Ramadhan et al. (2024) | *Comparison of Machine Learning Models for Heart Disease Classification with Web-Based Implementation* | Komparasi 5 Algoritma (Random Forest, DT, LR, Naive Bayes, KNN) + Penyeimbangan Data (SMOTE, ADASYN) | Heart Disease Dataset (faktor risiko kardiovaskular) | Random Forest + ADASYN mencapai skor AUC tertinggi sebesar 0,920 (92,0%); LR terendah (AUC 0,500) | Tidak melakukan fine-tuning hiperparameter secara otomatis; faktor kepentingan fitur (*feature importance*) belum diuraikan secara klinis |
| 4 | Narasimhan & Victor (2025) | *A hybrid approach with metaheuristic optimization and random forest in improving heart disease prediction* | Genetic Algorithm Optimized Random Forest (GAORF) + Seleksi Fitur SelectKBest | UCI Cleveland Heart Disease | GAORF terbukti menghasilkan akurasi tertinggi dibanding PSO-RF, ACO-RF, dan RF dasar | Angka metrik numerik tidak dilaporkan secara eksplisit pada teks abstrak; belum divalidasi pada pengujian multi-senter eksternal |
| 5 | Naik, Tejani, & Mousavirad (2025) | *SGO enhanced random forest and extreme gradient boosting framework for heart disease prediction* | Social Group Optimization (SGO) + Random Forest dan eXtreme Gradient Boosting (XGB) | UCI Cleveland dan UCI Statlog | SGO-RF mencapai akurasi 95,08% dan ROC-AUC 95,26% (Cleveland); SGO-XGBoost mencapai akurasi 97,62% (Statlog) | Biaya komputasi optimasi SGO tidak diukur; belum mengintegrasikan modul interpretabilitas klinis (Explainable AI / SHAP) |
| 6 | Bouqentar et al. (2024) | *Early heart disease prediction using feature engineering and machine learning algorithms* | Rekayasa fitur komparatif + 6 Algoritma ML (DT, RF, SVM, LR, AdaBoost, KNN) dengan 10-fold CV | UCI Cleveland dan UCI Statlog | Rekayasa fitur meningkatkan akurasi seluruh algoritma klasifikasi secara signifikan | Angka persentase metrik akhir model terbaik tidak dicantumkan secara numerik di teks abstrak; belum membandingkan dengan AutoML |
| 7 | Li, Chen, & Xu (2024) | *Coronary heart disease prediction based on hybrid deep learning* | Hybrid Deep Learning (dua DNN + RNN) dengan pelatihan sekunder K-Nearest Neighbor (KNN) | Data klinis penyakit jantung koroner (CAD) & benchmark | Menghasilkan akurasi 82,8%, presisi 87,08%, recall 88,57%, F1-score 87,82%, dan AUC 0,80 | Akurasi masih berada di bawah ensemble pohon keputusan teroptimasi (>90%); kompleksitas komputasi model hybrid relatif tinggi |
| 8 | Yasmeen, Khan, & Choi (2025) | *Heart disease prediction using hybrid TabNet architecture with stacked ensemble learning* | Stacked ensemble TabNet (deep learning feature selection) + XGBoost dengan meta-learner LR/SVM | UCI CVD (Cleveland) dan Kaggle CVD | Ensemble TabNet-XGBoost secara konsisten melampaui seluruh baseline pada akurasi, F1, AUC, dan MCC | Kompleksitas arsitektur tinggi dan memerlukan komputasi besar; belum diuji kemampuannya untuk inferensi pada perangkat terbatas (*edge mobile*) |
| 9 | Chandrasekhar & Peddakrishna (2023) | *Enhancing Heart Disease Prediction Accuracy through Machine Learning Techniques and Optimization* | Soft voting ensemble (RF, KNN, LR, NB, GB, AdaBoost) dengan GridSearchCV (5-fold CV) | UCI Cleveland dan IEEE Dataport | Soft voting ensemble meningkatkan akurasi menjadi 93,44% pada dataset Cleveland dan 95% pada IEEE Dataport | Penentuan bobot voting bersifat seragam (*uniform weight*); belum menyediakan visualisasi interpretabilitas keputusan medis per pasien |
| 10 | Paladino et al. (2023) | *Evaluating the Performance of Automated Machine Learning (AutoML) Tools for Heart Disease Diagnosis and Prediction* | Komparasi AutoML (AutoGluon, PyCaret, AutoKeras) vs 10 model ML manual (5-fold CV) | Cleveland, Hungarian, dan Combined dataset | ML manual hanya mencapai akurasi 55%–60%; AutoGluon konsisten unggul dengan akurasi 78%–86% | Sifat model AutoML cenderung *black-box*; kestabilan AutoKeras masih rendah (akurasi berfluktuasi antara 54%–83%) |

---

## 3.2 Analisis Celah Penelitian (*Research Gap*)

Berdasarkan sintesis dari kesepuluh artikel di atas, ditemukan beberapa kesenjangan ilmiah (*research gaps*) yang relevan untuk dikembangkan:

### 1. Kesenjangan antara Akurasi Tinggi dan Interpretabilitas Medis (*Explainable AI*)
- **Temuan**: Algoritma ensemble dan optimasi metaheuristik berhasil mencatatkan akurasi sangat tinggi (Naik et al. mencapai 95,08%; Chandrasekhar & Peddakrishna mencapai 93,44%; Parapak et al. mencapai 90%).
- **Celah**: Mayoritas model berkinerja tinggi tersebut diperlakukan sebagai "kotak hitam" (*black box*). Tenaga medis membutuhkan justifikasi rasional mengapa seorang pasien diklasifikasikan berisiko penyakit jantung. Belum ada penggabungan terpadu antara optimasi hiperparameter (seperti Bayesian / GA) dengan teknik atribusi fitur global dan lokal (*SHAP - SHapley Additive exPlanations* atau *LIME*).

### 2. Kesenjangan Penanganan Ketidakseimbangan Kelas (*Class Imbalance*) pada Model Teroptimasi
- **Temuan**: Parapak et al. (2025) dan Ramadhan et al. (2024) membuktikan bahwa penyeimbangan data dengan SMOTE/ADASYN mampu mendongkrak performa klasifikasi secara drastis (AUC naik hingga 0,920 dan presisi mencapai 96%).
- **Celah**: Penelitian optimasi metaheuristik tingkat lanjut (seperti Naik et al., 2025 dan Narasimhan & Victor, 2025) umumnya menguji algoritma langsung pada dataset mentah tanpa tahap *resampling* adaptif untuk menangani potensi *class imbalance* pada sampel minoritas.

### 3. Kesenjangan Performa antara Ensemble Terarah vs Solusi AutoML
- **Temuan**: Paladino et al. (2023) menunjukkan bahwa tanpa *tuning* mendalam, model ML manual hanya memperoleh akurasi 55%–60%, sementara AutoML (AutoGluon) mampu mencapai 78%–86%. Namun, studi Chandrasekhar & Peddakrishna (2023) membuktikan bahwa ensemble manual dengan GridSearchCV dapat menembus akurasi 93,44%.
- **Celah**: Belum ada studi komparatif langsung yang membandingkan efisiensi komputasi, kestabilan, dan interpretabilitas antara model *Ensemble Random Forest teroptimasi Bayesian* dengan kakas AutoML mutakhir pada dataset benchmark Cleveland.

### 4. Kebutuhan Solusi Komputasi Efisien untuk Implementasi Klinis
- **Temuan**: Pendekatan *deep learning hybrid* (Li et al., 2024) dan arsitektur *TabNet stacked* (Yasmeen et al., 2025) memerlukan daya komputasi tinggi dan waktu pelatihan yang lama, tetapi akurasinya (82,8%) tidak selalu melampaui pohon ensemble teroptimasi (93%–95%).
- **Celah**: Diperlukan arsitektur model klasifikasi yang ringkas (*lightweight*), berakurasi tinggi (≥93%), dan memiliki waktu inferensi cepat agar layak diintegrasikan ke dalam sistem skrining berbasis web atau mobile di fasilitas layanan kesehatan primer.

---

## 3.3 Rumusan Usulan Penelitian

Berdasarkan identifikasi kesenjangan penelitian di atas, diusulkan topik penelitian lanjutan:

> **"Optimasi Hiperparameter Random Forest Menggunakan Bayesian Optimization dan Teknik SMOTE Disertai Analisis Interpretabilitas SHAP untuk Klasifikasi Penyakit Jantung pada Dataset UCI Cleveland"**

### Unsur Kebaruan (*Novelty*):
1. **Integrasi Pipeline Terpadu**: Menggabungkan pra-pemrosesan penyeimbangan kelas (*SMOTE*) dengan pencarian parameter optimal berbasis *Bayesian Optimization* (menggunakan *Optuna*) pada algoritma Random Forest.
2. **Penerapan *Explainable AI* (XAI)**: Menyediakan visualisasi interpretabilitas keputusan model medis melalui *SHAP Summary Plot* dan *Force Plot*, sehingga klinisi dapat memahami kontribusi masing-masing fitur (seperti *thal*, *cp*, *ca*, dan *thalach*).
3. **Validasi Komprehensif**: Menguji kinerja model dengan *stratified 5-fold cross validation* dan membandingkan performanya secara langsung terhadap baseline literatur (Naik et al., Chandrasekhar & Peddakrishna, dan Parapak et al.).

---
*Dokumen ini merupakan bagian dari Latihan Soal Bab III: Identifikasi Masalah dan Studi Literatur.*
