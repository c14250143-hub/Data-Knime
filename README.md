# 📚 Analisis Visual Minat Baca (Reading Interest)

File **"Tes visual analysis of reading interest.knwf"** adalah alur kerja (workflow) yang dibuat menggunakan **KNIME Analytics Platform**. Alur kerja ini dirancang untuk memproses, membersihkan, dan memvisualisasikan data terkait minat baca.

Berikut adalah rincian langkah demi langkah dari analisis yang dilakukan, berdasarkan node-node yang teridentifikasi:

---

## 1. 📥 Input dan Persiapan Data

| Node KNIME | ID Node | Fungsi dalam Analisis Minat Baca |
| :--- | :--- | :--- |
| **CSV Reader** | (#1) | Langkah pertama adalah **membaca data mentah** yang tersimpan dalam format file CSV. Data ini kemungkinan berisi variabel-variabel minat baca (misalnya, usia, genre favorit, frekuensi membaca, dll.). |

## 2. 🧹 Pembersihan dan Seleksi Data

Alur kerja ini melakukan pembersihan data untuk memastikan kualitas dan fokus analisis:

* **Row Filter** **(#2)**
    * **Tujuan:** Memilih (atau mengecualikan) **baris (responden) tertentu** berdasarkan kriteria yang ditetapkan.
    * *Contoh:* Hanya menganalisis responden dengan usia 18-25 tahun.
* **Column Filter** **(#3)**
    * **Tujuan:** Memilih **variabel (kolom) yang relevan** dan menghapus kolom yang tidak diperlukan dari dataset.
    * *Contoh:* Menghapus kolom "Nomor ID Responden" karena tidak diperlukan untuk visualisasi.
* **Duplicate Row Filter** **(#4)**
    * **Tujuan:** Menghilangkan **data duplikat** untuk memastikan setiap entri adalah unik, menjaga integritas statistik analisis.

## 3. 📊 Eksplorasi dan Visualisasi Data (Visual Analysis)

Langkah-langkah ini mengubah data yang telah dibersihkan menjadi representasi visual untuk memudahkan interpretasi pola minat baca:

| Node KNIME | ID Node | Jenis Visualisasi | Interpretasi Data Minat Baca |
| :--- | :--- | :--- | :--- |
| **Scatter Plot** | (#7) | Grafik Sebar | Digunakan untuk mengidentifikasi **hubungan (korelasi)** antara dua variabel numerik. *Contoh: Apakah ada hubungan antara frekuensi kunjungan ke perpustakaan dan jumlah buku yang dibaca?* |
| **Pie Chart** | (#9) | Diagram Lingkaran | Menunjukkan **proporsi atau persentase** dari kategori. *Contoh: Distribusi persentase responden berdasarkan genre buku (Fiksi vs. Non-Fiksi).* |
| **Histogram** | (#10) | Histogram | Menampilkan **distribusi frekuensi** dari suatu variabel numerik. *Contoh: Sebaran usia atau sebaran skor tes minat baca di antara responden.* |
| **Bar Chart** | (#11) | Diagram Batang | Digunakan untuk **membandingkan nilai** di berbagai kategori. *Contoh: Perbandingan rata-rata minat baca antara responden dari berbagai wilayah.* |

---

### 📝 Kesimpulan

Alur kerja ini mencerminkan metodologi analisis data yang kuat dan bertujuan untuk **mendapatkan wawasan mendalam (insight)** mengenai **minat baca** dengan serangkaian tahap pembersihan data yang teliti, diikuti oleh eksplorasi visual yang komprehensif.
