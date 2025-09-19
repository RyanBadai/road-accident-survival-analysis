# 🚦 Analisis Prediktif Faktor Keselamatan pada Kecelakaan Lalu Lintas  

Repositori ini merupakan **capstone project** untuk program **IBM SkillsBuild** yang bertujuan menganalisis serta memprediksi faktor-faktor yang memengaruhi **keselamatan korban dalam kecelakaan lalu lintas**.  
Proyek ini menggabungkan **eksplorasi data**, **pemodelan machine learning**, dan **klasifikasi menggunakan Large Language Model (LLM)**.  

---

## 🎯 Ringkasan Proyek  
Kecelakaan lalu lintas adalah isu serius dengan dampak besar bagi masyarakat.  
Proyek ini bertujuan untuk:  
1. Mengidentifikasi faktor-faktor kunci yang memengaruhi keselamatan korban.  
2. Membangun dan membandingkan beberapa model machine learning untuk memprediksi status keselamatan.  
3. Memberikan rekomendasi berbasis data untuk mendukung kebijakan dan edukasi publik.  

---

## 📊 Dataset  
- **Sumber:** [Road Accident Survival Dataset – Kaggle](https://www.kaggle.com/datasets/himelsarder/road-accident-survival-dataset)  
- **Fitur utama:**  
  - `Age`  
  - `Gender`  
  - `Speed_of_Impact`  
  - `Helmet_Used`  
  - `Seatbelt_Used`  
  - `Survived` (target)  

Dataset awal berjumlah **200 baris**, setelah pembersihan data tersisa **196 baris** yang siap dipakai.  

---

## ⚙️ Alur Analisis  
1. **Pembersihan Data:** Menangani nilai hilang agar kualitas data tetap terjaga.  
2. **EDA (Exploratory Data Analysis):** Visualisasi distribusi usia, jenis kelamin, dan kecepatan.  
3. **Persiapan Data:** Encoding variabel kategorikal & scaling variabel numerik.  
4. **Pemodelan:** Melatih dan mengevaluasi enam model klasifikasi:  
   - Logistic Regression  
   - K-Nearest Neighbors (KNN)  
   - Support Vector Machine (SVM)  
   - Decision Tree  
   - Random Forest  
   - XGBoost  

---

## ✨ Insight Utama  

### Faktor Penentu Keselamatan  
Berdasarkan analisis **LLM Granite** dan **Confusion Matrix**, faktor paling berpengaruh adalah:  
- Penggunaan **sabuk pengaman**  
- **Kecepatan kendaraan**  
- Penggunaan **helm**  

### Profil Umum Kecelakaan  
- **Jenis kelamin:** Perempuan lebih sering terlibat dibanding laki-laki.  
- **Usia:** Kelompok usia >45 tahun memiliki keterlibatan tertinggi.  
- **Kecepatan:** Kecelakaan lebih sering terjadi pada kecepatan tinggi.  

---

## 🤖 Kinerja Model  

### Perbandingan Hasil Evaluasi  
| Model Name                |   Accuracy Score |   F1 Score |   Precision Score |   Recall Score |
|:--------------------------|-----------------:|-----------:|------------------:|---------------:|
| Logistic Regression       |            0.525 |   0.512821 |          0.47619  |       0.555556 |
| K-Nearest Neighbors       |            0.55  |   0.571429 |          0.5      |       0.666667 |
| Support Vector Machine    |            0.6   |   0.636364 |          0.538462 |       0.777778 |
| Decision Tree             |            0.525 |   0.55814  |          0.48     |       0.666667 |
| Random Forest             |            0.475 |   0.511628 |          0.44     |       0.611111 |
| Extreme Gradient Boosting |            0.425 |   0.378378 |          0.368421 |       0.388889 |

### Model Terbaik  
- **Support Vector Machine (SVM)**  
  - Akurasi: **0.60**  
  - F1-Score: **0.63**  
  - Precision: **0.54**  
  - Recall: **0.78**  

### LLM Granite  
- **Model:** ibm-granite/granite-3.3-8b-instruct  
- Digunakan sebagai pendekatan alternatif klasifikasi. LLM mampu menganalisis pola dan memprediksi kasus baru secara efektif.  

---

## 📜 Rekomendasi  
1. **Kampanye keselamatan:** Fokus pada edukasi bahaya kecepatan tinggi & pentingnya sabuk pengaman.  
2. **Pelatihan khusus:** Program untuk perempuan dan kelompok usia lanjut.  
3. **Pengembangan model:** Tambahkan variabel baru (jenis kendaraan, cuaca, tipe jalan) untuk meningkatkan akurasi.  

---
