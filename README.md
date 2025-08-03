# Eksplorasi-Model-IBM-Granite-Instruct-untuk-Klasifikasi-Tipe-Kepribadian-Ekstrovert-Introvert

# 🧠 Personality Classification using IBM Granite Instruct - Caspstone Project Data Classification and Summaraization Using IBM Granite

> Made by **Muh. Syahwal**

## 📝 Deskripsi Proyek

Proyek ini mengeksplorasi kemampuan model **IBM Granite Instruct** untuk melakukan klasifikasi kepribadian manusia (Introvert vs Ekstrovert) berdasarkan **data perilaku sederhana** yang disusun dalam bentuk **deskripsi teks**.

### 🎯 Tujuan
- Mengklasifikasikan kepribadian berdasarkan data perilaku tanpa menggunakan tes psikologis konvensional.
- Mengevaluasi kemampuan model LLM seperti IBM Granite untuk tugas klasifikasi berbasis teks.
- Menyediakan pendekatan alternatif dalam personalisasi layanan digital, rekrutmen, dan edukasi.

---

## 📂 Dataset

Dataset diambil dari Kaggle:  
🔗 [Extrovert vs Introvert Behavior Data](https://www.kaggle.com/datasets/rakeshkapilavai/extrovert-vs-introvert-behavior-data/data)

### 🔢 Rincian Dataset
- Jumlah baris: 2.900
- Jumlah kolom: 8
- Fitur numerik: `time_spent_alone`, `social_event_attendance`, `going_outside`, `friends_circle_size`, `post_frequency`
- Fitur kategorikal: `stage_fear`, `drained_after_socializing`, `personality (target)`

---

## 📊 Analisis Data

- Distribusi kepribadian: **51.4% Ekstrovert**, **48.6% Introvert**
- Ciri khas:
  - Introvert: waktu sendiri tinggi, interaksi sosial rendah
  - Ekstrovert: aktif keluar rumah, banyak teman, sering bersosialisasi

---

## 🧪 Implementasi

Model: **IBM Granite Instruct (via Replicate API)**  
Input berupa **prompt teks** yang dikonversi dari data numerik dan kategorikal.

### ✍️ Contoh Prompt:
> Saya menghabiskan 11 jam sendirian dalam sehari, menghadiri 2 acara sosial per minggu, memiliki 2 teman dekat, membuat 1 postingan media sosial per minggu, keluar rumah sebanyak 1 kali per minggu, saya takut berbicara di depan umum, dan merasa lelah setelah bersosialisasi.

### 🔧 Parameter Model:
| Parameter           | Nilai     |
|---------------------|-----------|
| temperature         | 0.2 - 0.3 |
| top_k               | 40        |
| top_p               | 0.9       |
| max_new_tokens      | 100       |
| repetition_penalty  | 1.1       |

---

## 📈 Hasil Klasifikasi

Dari 6 data testing:
- **Introvert**: 5 (83.3%)
- **Ekstrovert**: 1 (16.7%)

### 🧩 Pola Kepribadian:
**Introvert**:
- >5 jam sendiri, sedikit acara sosial, sedikit teman, merasa lelah saat bersosialisasi, takut tampil

**Ekstrovert**:
- Sosial tinggi, banyak teman, aktif keluar rumah, nyaman bersosialisasi

---

## ✅ Rekomendasi

### Pengembangan Model
- Tambahkan variasi data input
- Batasi panjang output model
- Tampilkan **confidence score**

### Untuk Aplikasi Nyata
- Buat UI dengan Streamlit/WebApp
- Tampilkan label hasil klasifikasi dengan jelas
- Tambahkan saran atau rekomendasi berdasarkan kepribadian

---

## 📌 Kesimpulan

Model **IBM Granite Instruct** menunjukkan potensi besar dalam klasifikasi kepribadian berbasis deskripsi perilaku. Dengan pendekatan ini, identifikasi kepribadian bisa dilakukan secara otomatis dan efisien tanpa tes psikologi tradisional.

---

## 🚀 Teknologi

- Python (Pandas, Seaborn, Matplotlib)
- IBM Granite Instruct (via Replicate API)
- Streamlit (opsional untuk deployment)

---

## 📬 Kontak

Made by **Muh. Syahwal**  
📧 Email: *muh.syahwal@gmail.com*  
📍 Indonesia


