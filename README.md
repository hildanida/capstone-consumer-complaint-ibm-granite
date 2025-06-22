# 📘 Capstone Project: Data Classification and Summarization using IBM Granite

## 📌 Project Overview
Proyek ini menganalisis data keluhan konsumen sektor keuangan di Amerika Serikat menggunakan model AI IBM Granite. Fokus utama adalah pada klasifikasi jenis keluhan dan ringkasan narasi keluhan yang tidak terstruktur. Tujuan utamanya adalah mengubah data teks menjadi insight yang *actionable* untuk mendukung pengambilan keputusan berbasis data.

## 🎯 Objectives
- Menyesuaikan parameter output dari IBM Granite agar lebih presisi dan ringkas.
- Mengelompokkan keluhan ke dalam kategori produk dan isu utama.
- Meringkas narasi panjang menjadi ringkasan pendek yang relevan.
- Menghasilkan insight visual dan temuan utama dari data keluhan.

## 🧠 AI Tools and Environment
- **Model**: `ibm-granite/granite-3.3-8b-instruct` via Replicate API
- **Environment**: Google Colab
- **Libraries**: `langchain_community`, `replicate`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `kaggle`

## 🗂 Dataset
- **Source**: [Consumer Financial Protection Bureau (CFPB)](https://www.consumerfinance.gov/data-research/consumer-complaints/)
- **Kaggle Mirror**: https://www.kaggle.com/datasets/hildanida/us-consumer-financial-complaints-dataset-raw
- **Format**: CSV
- **Jumlah Data**: >1 juta baris
- **Fitur Utama**: Produk, Masalah, Narasi Keluhan, Tanggal, Lokasi

## 🛠️ Methodology
### 1. Preprocessing
- Menghapus nilai kosong
- Membersihkan teks narasi keluhan
- Menyiapkan kolom 'cleaned_complaint' untuk input model

### 2. Klasifikasi Keluhan
- Uji dengan parameter default
- Uji dengan `top_k` 5 untuk fokus topik
- Uji dengan parameter `top_k`, `top_p`, `max_tokens`, `repetition_penalty` untuk output optimal

### 3. Ringkasan Narasi
- Ringkasan default
- Ringkasan pendek (`max_tokens=20`)
- Ringkasan optimal dengan parameter gabungan

### 4. Visualisasi & Insight
- Distribusi Produk dan Isu Keluhan
- Temuan dari klasifikasi dan ringkasan

## 📊 Hasil & Temuan
- Produk seperti *Credit Reporting* dan *Mortgage* adalah sumber keluhan utama
- Masalah seperti *Incorrect Credit Info* sangat dominan
- Model menghasilkan klasifikasi dan ringkasan lebih baik setelah parameter disesuaikan

## ✅ Rekomendasi
1. Fokus pada peningkatan layanan *credit reporting* dan *mortgage*.
2. Perbaiki proses investigasi laporan kredit.
3. Gunakan AI untuk membantu tim support memahami keluhan lebih cepat.
4. Tambahkan analisis sentimen untuk eksplorasi lebih dalam.
5. Monitor output model secara berkala untuk penyesuaian lanjutan.

## 👩‍💻 Author
Hilda Nida  
Capstone Project – Student Development Initiative Bootcamp

---

> *"AI bukan untuk menggantikan manusia, tapi untuk mempercepat keputusan yang lebih bijak."*

