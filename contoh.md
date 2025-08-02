## ✅ 1. Project Overview

**Judul Proyek**:
Analisis Sentimen dan Aspirasi Mahasiswa Indonesia terhadap Dunia Kerja dan Ekonomi menggunakan AI Granite IBM

**Tujuan Proyek**:
Memahami perasaan, keresahan, dan harapan mahasiswa serta fresh graduate Indonesia terhadap dunia kerja dan situasi ekonomi melalui analisis tweet. Proyek ini menangkap suara otentik generasi muda Indonesia secara langsung dari media sosial, lalu dianalisis menggunakan teknologi AI dari IBM Granite.

**Latar Belakang**:
Banyak mahasiswa merasa kecewa setelah lulus karena sulitnya mendapatkan pekerjaan, mahalnya biaya pendidikan, serta ketimpangan antara kompetensi akademik dan tuntutan industri. Sentimen ini diekspresikan luas di Twitter. Proyek ini bertujuan menganalisis pola emosi, aspirasi, dan harapan generasi muda untuk menemukan insight dan solusi nyata.

**Pendekatan**:
Kami menggunakan pendekatan berbasis AI dengan IBM Granite untuk klasifikasi sentimen, emosi, dan niat dari tweet mahasiswa. Proyek ini menggunakan scraping, preprocessing, klasifikasi menggunakan LLM, visualisasi data, hingga penyusunan insight dan rekomendasi.

---

## ✅ 2. Analysis Process

**Langkah-langkah Analisis**:

1. **Data Collection**:

   * Scraping tweet bertema pekerjaan, kuliah, dan ekonomi mahasiswa sejak Januari 2024
   * Tools: `snscrape`, `crawl` keyword satu per satu
   * Total data mentah setelah dibersihkan: **262 tweet**

2. **Preprocessing**:

   * Menghapus simbol, mention, link, angka
   * Normalisasi teks informal
   * Menyimpan hasil bersih ke file: `dataset_capstone_cleaned.csv`

3. **Batching dan Classification**:

   * Batch: 10 tweet per prompt (untuk efisiensi dan menjaga konteks)
   * Model: IBM Granite 3B-8B-Instruct via LangChain
   * Output klasifikasi: Sentiment, Emotion, Intent

4. **Parsing Output**:

   * Parsing hasil AI ke struktur tabel `classified_tweets.csv`
   * Hanya tweet dengan hasil lengkap yang digunakan
   * Total tweet berhasil diklasifikasi: **162**

5. **Visualization & EDA**:

   * Pie chart dan bar chart: Distribusi sentimen, emosi, niat
   * Wordcloud: kata yang paling sering muncul
   * Grouping dan simplifikasi multi-label agar visual tidak padat duplikat

---

## ✅ 3. Insight & Findings

**Ringkasan Temuan Akhir:**

1. **Dominant Emotions & Sentiments**:

   * Sentimen **negatif** paling dominan, dengan **frustration** dan **disappointment** sebagai emosi utama
   * Sekitar **23% tweet mengandung harapan**, meski disertai rasa lelah dan kecewa
   * Sentimen **mixed dan netral** menunjukkan kebingungan dan ketidakpastian

2. **Sumber Kekecewaan**:

   * **Ekonomi sulit**: Mahasiswa kerja sambil kuliah, struggle biaya hidup
   * **Pasar kerja tidak adil**: Lulusan baru merasa tertolak tanpa alasan, tidak siap industri
   * **Pendidikan mahal**: Biaya tinggi tidak sebanding dengan outcome kerja
   * **Tidak percaya sistem**: Pemerintah, kampus, dan perusahaan dinilai gagal dengar aspirasi

3. **Pergeseran Emosional**:

   * Ada transisi dari optimisme ke sinisme
   * Harapan di awal lulus berganti kecewa, bahkan apatis
   * Ini menunjukkan pentingnya intervensi sebelum frustrasi berubah menjadi putus asa

4. **Visual Insight**:

   * Wordcloud: kata "nganggur", "kerja", "lulus", "mahal" sangat dominan
   * Pie & bar chart memperkuat dominasi emosi negatif

---

## ✅ 4. Conclusion & Recommendation

**Kesimpulan Utama**:
Suara mahasiswa Indonesia di media sosial menunjukkan krisis kepercayaan dan realitas keras pasca-lulus. Mereka merasa sistem tidak berpihak dan tidak relevan dengan kebutuhan nyata dunia kerja.

**Rekomendasi**:

* **Untuk Universitas**:

  * Perbanyak kursus vokasi dan praktikal
  * Bangun program beasiswa dan pendampingan karier
  * Libatkan mahasiswa dalam penyesuaian kurikulum

* **Untuk Pemerintah**:

  * Turunkan biaya pendidikan tinggi
  * Buat program kerja dan pelatihan bagi fresh graduate
  * Transparansi anggaran pendidikan dan sistem rekrutmen

* **Untuk Dunia Industri**:

  * Buka peluang magang, apprentice, dan job fair
  * Kurangi syarat tidak realistis (pengalaman kerja)
  * Buat roadmap karier yang manusiawi dan adil

**Catatan Penting**:
Pesan mereka tegas: *kami ingin didengar, kami ingin masa depan yang bisa diperjuangkan.*

---

## ✅ 5. AI Support Explanation

**Model yang Digunakan**:

* IBM Granite 3.3B–8B Instruct via LangChain dan Replicate API

**Fungsi AI dalam Proyek**:

* **Text Classification**:

  * Menganalisis tweet dan mengklasifikasikan 3 aspek: Sentiment, Emotion, Intent
* **Summarization**:

  * Menggunakan AI untuk menyusun ringkasan insight berbasis data klasifikasi
* **Prompt Engineering**:

  * Prompt disusun agar AI memahami konteks bahasa Indonesia informal

**Alasan Relevansi AI**:

* Efektif membaca teks tidak baku dari media sosial
* Konsisten dan objektif dalam klasifikasi emosi dan intensi
* Mempercepat proses analisis dengan hasil yang terstruktur
