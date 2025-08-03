# 📘 Capstone Project: Analisis Sentimen dan Aspirasi Mahasiswa Indonesia terhadap Dunia Kerja dan Ekonomi di Indonesia menggunakan AI Granite IBM

## 🚀 Project Overview

Banyak mahasiswa dan fresh graduate Indonesia mengungkapkan keresahan mereka di media sosial, terutama di Twitter. Mereka menghadapi kenyataan pahit setelah lulus: sulitnya mencari pekerjaan, tingginya biaya pendidikan, dan ketimpangan antara kuliah dan dunia industri. Curhatan ini mencerminkan krisis kepercayaan terhadap sistem pendidikan, ketenagakerjaan, dan kebijakan ekonomi.

Melalui proyek ini, Saya ingin menangkap **suara otentik generasi muda Indonesia** dan menganalisisnya secara sistematis menggunakan teknologi AI, khususnya **IBM Granite**. Hasilnya akan digunakan untuk menggali emosi, aspirasi, dan tantangan yang mereka alami, lalu menyajikannya dalam bentuk insight yang bermanfaat bagi pemerintah, universitas, dan dunia industri.

### 🎯 Tujuan Proyek

- Menganalisis **sentimen**, **emosi**, dan **niat** mahasiswa dan lulusan baru terhadap dunia kerja dan kondisi ekonomi.
- Mengidentifikasi pola frustrasi, harapan, dan ketidakpuasan mereka yang diungkapkan di media sosial.
- Menyediakan **rekomendasi nyata** berbasis data untuk universitas, pemerin, dan perusahaan agar lebih mendengar dan memahami generasi muda.

### 🧠 Tools & Teknologi

* **Python**, `snscrape`, `pandas`, `matplotlib`, `wordcloud`
* **IBM Granite (via LangChain + Replicate)** untuk klasifikasi & analisis
* **Google Colab** untuk notebook & visualisasi

---

## 🔍 Langkah Analisis

### 1. Data Collection

* Scraping tweet menggunakan query spesifik seperti: "biaya kuliah", "fresh graduate cari kerja", "lulus tapi nganggur", "gaji fresh graduate", "#kaburajadulu".
* Bahasa: Indonesia, Rentang waktu: Januari 2024 - sekarang
* Total data yang dikumpulkan: **±1300 tweet**

### 2. Preprocessing

* Bersihkan mention, URL, emoji, angka, karakter khusus
* Setelah dibersihkan: **262 tweet** valid disimpan ke `dataset_capstone_cleaned.csv`

### 3. Klasifikasi AI

* Batch: 10 tweet per prompt
* Prompt disusun dalam bahasa Inggris untuk akurasi IBM Granite
* Output klasifikasi: **Sentiment**, **Emotion**, **Intent**
* Output disimpan di `classified_tweets.csv` (**162 tweet berhasil**)
* **100 tweet gagal klasifikasi** karena output model tidak terstruktur atau kosong

> 📌 **Catatan Penting**
> Model AI (Granite) memiliki keterbatasan dalam memahami konteks informal atau ambigu dari tweet. Dari total 262 tweet bersih, hanya 162 yang berhasil diklasifikasi lengkap. 
> Hal ini menunjukkan pentingnya validasi manusia dalam proses AI generatif. Saya memilih hanya memasukkan data yang hasil klasifikasinya lengkap untuk menjaga akurasi analisis.

### 4. Visualisasi

* Wordcloud: Kata dominan seperti "nganggur", "kerja", "kuliah", "mahal"
* Pie & Bar Chart: Distribusi emosi, niat, dan sentimen
* Penyederhanaan label untuk menghindari duplikasi

* **Alasan penggunaan metode**:
  - Memudahkan pembaca awam untuk memahami tren
  - Menyaring informasi paling relevan secara visual
  - Membantu mendukung insight dari hasil klasifikasi AI

---

## 📊 Hasil & Insight

### 💔 Sentimen Dominan:

* 60%+ tweet bernada **negatif**, dengan emosi utama **frustrasi** dan **kecewa**
* Sekitar 23% masih memiliki **harapan**, namun disertai nada skeptis

### 😩 Masalah Utama:

* **Ekonomi sulit**: Banyak mahasiswa kerja sambilan dan stres biaya kuliah
* **Pasar kerja tidak adil**: IPK tinggi tidak menjamin keterima kerja
* **Pendidikan mahal**: Banyak merasa "gagal investasi" setelah lulus
* **Tidak percaya sistem**: Pemerintah, kampus, dan perusahaan dianggap tidak peduli

### 📉 Pergeseran Emosi:

* Dari optimis saat lulus, menjadi apatis karena realita pekerjaan dan ekonomi

---

## ✅ Rekomendasi Kebijakan

### Untuk Universitas:

* Perbanyak program praktikal dan magang
* Bangun career center yang aktif dan nyata
* Kurangi biaya atau perluas beasiswa

### Untuk Pemerintah:

* Turunkan biaya kuliah & subsidi pendidikan
* Dorong transparansi job market dan rekrutmen
* Program kerja untuk fresh graduate

### Untuk Industri:

* Kurangi syarat pengalaman tidak masuk akal
* Bangun program magang dan mentor
* Bangun roadmap karier yang manusiawi

> "Kami tidak takut kerja keras, kami hanya ingin sistem yang adil."

---

## 🤖 Penjelasan Penggunaan AI

### 🔧 Model:

* **IBM Granite (granite-3.3-8b-Instruct)** — powerful untuk intruksi yang spesifik seperti classification dan summarization

### 📌 Fungsi IBM Granite:

* **Text Classification**: Mengenali emosi, niat, dan sentimen tweet
* **Summarization**: Menyusun ringkasan insight berbasis data klasifikasi
* **Prompt Engineering**: Dirancang agar paham bahasa Indonesia informal

### Kenapa Pakai IBM Granite ?

* Cepat dan konsisten dalam membaca tweet tidak baku
* Mengurangi bias manusia dalam interpretasi emosi dan intentsi
* Mampu menyarikan insight dari data sosial secara efisien
* Mempercepat proses analisis dengan hasil yang terstruktur

---

## 📎 Output Proyek

* `classified_tweets.csv`: Dataset hasil klasifikasi AI
* `summary_output.txt`: Insight & rekomendasi akhir
* `visuals/`: Pie chart, bar chart, dan wordcloud

---

## 🏁 Penutup

Proyek ini bukan sekadar analisis, tapi panggilan untuk mendengar suara generasi muda. Harapannya, insight yang dihasilkan bisa mendorong perubahan nyata — dari ruang kuliah, ke dunia kerja, hingga kebijakan negara.

> "Frustrasi mereka bukan sekadar curhat — itu tanda bahwa sistem sedang tidak sehat."

---

🧠 Dibuat untuk publik dan proyek Capstone Project Data Classification and Summarization Using IBM Granite IBM x Hacktiv8 Student Development Initiative 2025

📁 [Link Google Colab Notebook](https://colab.research.google.com/drive/1Q8Fkyb8SS79zigMc60bCrfSyffNteJuJ?usp=sharing) | 🔗 [GitHub Repository]() | 🖼️ [Slide Presentasi]()
