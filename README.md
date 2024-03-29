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
<p align='justify'>Setelah selesai memilih data yang akan digunakan, proses selanjutnya adalah menghilangkan atau membuat tulisan pada kolom full_text bisa dibaca secara baik dengan menggunakan syntax yang ada pada bahasa pemrograman python. Maka hasilnya bisa dilihat seperti dibawah ini.</p>

<img src="https://github.com/kartikajls/Analisis-Sentimen/assets/98092595/43bf2aeb-a51d-45e8-8fd3-33906922dadc"></img>

<p align='justify'>Selanjutnya adalah proses normalisasi. Proses ini digunakan untuk menormalisasi tulisan atau mengganti kata singkatan, seperti "yg, jdi, utk, koq, utk, dll" menjadi "yang, jadi, untuk" , menghilangkan emoticon, dan menghilangkan tulisan yang tidak ada hubungannya sepert "anis dan prabowo". Sehingga dengan menggunakan python proses normalisasi kata-kata tersebut dilakukan.</p>

<img src="https://github.com/kartikajls/Analisis-Sentimen/assets/98092595/e050d242-bcdd-4716-bc31-57edf0ecf59f"></img>

### Analisis TextBlob
<p align='justify'>Menggunakan analisis textBlob, kita sudah dapat menganalisis dan mengetahui berapa nilai yang dihasilkan dari komentar positif, netral, dan negatif. Textblob merupakan salah satu tools atau lebih tepatnya library python untuk pemprosesan dibidang "Natural Language Processing (NLP)" menggunakan bahasa python. Melalui textblob, kita dapat melakukan berbagai proses terhadap data teks mulai dari yang sederhana seperti tokenisasi (pemotongan kata) sampai analisa sentiment. Maka hasilnya akan bisa dilihat</p>

<img src="https://github.com/kartikajls/Analisis-Sentimen/assets/98092595/8bd89f80-577a-4bb1-a9fd-f36031cb38ce"></img>

<p align='justify'>Bisa dilihat dari gambar diatas. Setelah pemilu 2024 berakhir, komentar masyarakat di aplikasi twitter atau X masih tergolong positif. Hasil menunjukan komentar positif sebesar 82, netral 73, dan negatif 34. Hal ini mungkin terjadi karena masih adanya kepercayaan masyarakat pada calon presiden Ganjar Pranowo dengan melihat rekam jejak beliau yang pernah menjadi Gubernur Jawa Tengah.</p>

<p align='justify'>Setelah menganalisis dengan menggunakan library TextBlob, data yang dianalisis dapat divisualkan menjadi gambar seperti ini.</p>

<img src="https://github.com/kartikajls/Analisis-Sentimen/assets/98092595/694ca85b-d373-4048-badb-b91feb594799"></img>

### Analisis Sentimen
<p align='justify'>Jika kita sudah melihat jumlah komentar positif, netral, dan negatif dengan menggunakan tools TextBlob. Sekarang dengan menggunakan metode Naive Bayes, akan menghasilkan komentar positif, netral, dan negatif dengan tingkat akurasi sebesar 0.75 atau 75 persen. Metode Naive Bayes merupakan metode pengklasifikasian berdasarkan probabilitas sederhana dan dirancang agar dapat dipergunakan dengan asumsi antar variabel penjelas saling bebas (independen). Pada algoritma ini pembelajaran lebih ditekankan pada pengestimasian probabilitas. Keuntungan algoritma naive bayes adalah tingkat nilai error yang didapat lebih rendah ketika dataset berjumlah besar, selain itu akurasi naive bayes dan kecepatannya lebih tinggi pada saat diaplikasikan ke dalam dataset yang jumlahnya lebih besar.</p>

<p align='justify'>Sehingga setelah dilakukan proses analisis dengan menggunakan metode Naive Bayes, hasil yang didapat cukup berbeda dengan menggunakan tools TextBlob. Hal ini dikarenakan metode yang digunakan Naive Bayes memiliki tingkat akurasi 0.75 atau 75 persen, sehinggal hasil yang didapat seperti berikut.</p>

<img src="https://github.com/kartikajls/Analisis-Sentimen/assets/98092595/4028e431-c71a-46c7-8fbb-889bc65d53cd"></img>

<img src="https://github.com/kartikajls/Analisis-Sentimen/assets/98092595/6d6a472c-8110-48e2-ad57-c18db3c0d586"></img>
