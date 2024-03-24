# Analisis-Sentimen
<ul>
  <li>Source = Ganjar_Pranowo.csv</li>
  <li>Analyze = ganjar_pranowo.ipynb</li>
  <li>Data lain hasil olahan = terjemahanganjarpranowo.csv dan tokenizedganjarproanowo.csv</li>
</ul>

## Introduction
<p align='justify'>Pada tulisan kali ini, Saya akan mencoba untuk mengenalisis sentimen masyarakat terhadap Calon Presiden Ganjar Pranowo di Tahun 2024 dengan menggunakan metode Naive Bayes. Metode Naive Bayes merupakan sebuah metode yang digunakan untuk memprediksi peluang di masa depan berdasarkan pengalaman di masa sebelumnya dengan memperhatikan asumsi yg sangat kuat (naïf) akan independensi dari masing-masing kondisi / kejadian. Data yang digunakan bersumber dari asumsi masyarakat yang diambil dari komentar tweet di sosial media twitter atau X. Dengan menggunakan teknik "Scrapping Data", sampel yang diambil 200 komentar masyarakat dengan kata kunci yaitu "Ganjar-Pranowo". Kata kunci "Ganjar Pranowo" sempat menjadi tranding topik setelah Pemilu tahun 2024 berakhir, tepatnya data ini diambil pada tanggal 15 Maret 2024.</p>

## Data 
<p align='justify'>Data yang digunakan adalah komentar yang diambil pada platform tweeter atau X yang menjadi trending topik "Ganjar-Pranowo" pada tanggal 15 Maret 2024. Data ini diambil dengan menggunakan teknik Scrapping data, yaitu dengan menarik data pada platform X atau twitter dengan menggunakan bahasa pemrograman python sebanyak 200 komentar atau 200 sampel. Data tersebut akan berbentuk seperti ini.</p>

<img src="https://github.com/kartikajls/InstagramAnalyze/assets/98092595/b1269d88-1036-4195-b4ce-a983dff1dd47"></img>

## Proses Pengolahan Data
### Cleaning Data
<p align='justify'>Berdasarkan data mentah diatas, proses "cleaning data" dilakukan untuk memisahkan variabel yang tidak dibutuhkan. Pada tahap ini data yang akan diambil adalah data pada kolom full_text, username, dan created_at. Pada kolom full_text terdapat isi komentar masyarakat pada platform X atau twitter yang akan digunakan untuk proses analisis, kolom username dan created_at digunakan untuk melihat username yang menulis dan waktu komentar itu dibuat.</p>
