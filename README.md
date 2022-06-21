# proyekvisdat
Dokumentasi Proyek UAS Visualisasi Data dan Informasi

## Perancangan
Proses perancangan dashboard informasi sebagai bentuk visualisasi data kondisi dan kualitas lingkungan di Indonesia disesuaikan dengan kebutuhan pengguna dan tujuan awal dari visualisasi data, yaitu:
1.	Menyajikan data kondisi lingkungan di Indonesia 
2.	Menggambarkan kualitas lingkungan di Indonesia 
3.	Membantu proses monitoring kondisi dan kualitas lingkungan di Indonesia 
4.	Mengedukasi masyarakat mengenai kondisi dan kualitas lingkungan di Indonesia

Secara garis besar dilakukan melalui 4 tahap yaitu pengumpulan data, pengolahan data, visualisasi data, dan terakhir pembuatan dashboard. Berikut flowchart yang menunjukkan tahapan metodologi dari proyek ini:

![image](https://user-images.githubusercontent.com/107903297/174719591-962c1104-48c9-44a0-b6fa-38a7e44e0759.png)

## Dataset
Data yang digunakan dalam project ini merupakan data sekunder yang bersumber dari publikasi Statistik Lingkungan Hidup Indonesia 2021 yang merupakan seri publikasi tahunan Badan Pusat Statistik (BPS) yang menyajikan beragam jenis data mengenai kondisi lingkungan hidup di Indonesia, yang bersumber dari BPS dan Kementerian/Lembaga/ Institusi lain. 
Data SLHI 2021 berasal dari hasil survei atau sensus yang dilakukan oleh BPS dan laporan-laporan atau publikasi tahunan instansi terkait lingkungan hidup baik di pusat maupun daerah. Studi literatur dilakukan untuk mendukung publikasi SLHI 2021. Pengumpulan data dan informasi lingkungan hidup untuk publikasi SLHI 2021 dilakukan dengan terlebih dahulu menginventarisir instansi sebagai sumber pengumpulan data yang dibutuhkan. Pengumpulan data sekunder lingkungan hidup di instansi pusat dilaksanakan pada bulan Februari sampai November, sedangkan pengumpulan data sekunder di daerah sekitar bulan Maret sampai September.
Data tabel yang telah disediakan oleh BPS dalam Statistika Lingkungan Hidup 2021, secara keseluruhan terdapat 35 tabel yang terlampir dalam komponen kualitas dan kondisi lingkungan. 

## Data Preprocessing
Data preprocessing adalah teknik yang digunakan untuk mengubah data mentah dalam format yang berguna dan efisien. Inisiatif ini diperlukan karena data mentah seringkali tidak lengkap dan memiliki format yang tidak konsisten. Preprocessing dalam proyek ini melibatkan seleksi data yang meninggalkan tabel dengan isian tidak lengkap atau format data yang kurang sesuai untuk divisualisasikan. Setelah itu, akan dilakukan integrasi data agar sesuai dengan jenis visualisasi yang diinginkan, misal pengintegrasian data Indeks Kualitas Air dan Indeks Kualitas Udara agar dapat divisualisasikan menggunakan stacked column chart. Reduksi data juga dilakukan pada tabel yang memuat informasi yang kurang perlu, misal atribut persentase pada tabel Luas Ekosistem & Kawasan Konservasi Terumbu Karang.
Dalam tahap ini dipilih beberapa data dan tabel yang akan disajikan, yaitu:
1.	Luas Wilayah NKRI
2.	Luas Daratan Indonesia
3.	Luas Perairan Indonesia
4.	Jumlah Pulau di Indonesia
5.	Indeks Kualitas Air Tingkat Provinsi
6.	Indeks Kualitas Udara Tingkat Provinsi
7.	Indeks Kualitas Lingkungan Hidup Tingkat Provinsi
8.	Luas Ekosistem & Kawasan Konservasi Mangrove
9.	Luas Ekosistem & Kawasan Konservasi Terumbu Karang
10.	Luas Ekosistem & Kawasan Konservasi Padang Lamun

## Implementasi
Setelah data dikumpulkan dan diolah untuk mendapatkan variabel atau data spesifik yang ingin disajikan, proses visualisasi dilakukan. Visualisasi dilakukan dengan bantuan tools yaitu Tableau. Secara umum, Tableau berfungsi untuk mempercepat pembuatan visualisasi interaktif dari pengolahan data tertentu. Tableau juga dengan mudah digunakan untuk proses implementasi data serta mudah dipelajari. Tools ini juga secara khusus dapat menerjemahkan data ke dalam bentuk visual atau presentasi dan mengolah metadata. Selain itu, Tableau memungkinkan pengguna untuk membuat semua visualisasi ini tanpa melakukan pengodean dan juga dapat mengambil berbagai ukuran data ke dalamnya untuk diolah.
Empat data awal (Luas Wilayah NKRI, Luas Daratan Indonesia, Luas Perairan Indonesia,dan Jumlah Pulau di Indonesia) disajikan dalam visualisasi dimana angka langsung divisualisasikan tanpa perantara grafik atau tabel.
![image](https://user-images.githubusercontent.com/107903297/174720063-4ac70f2c-322c-4fd1-8e65-3f36f91e33a9.png)

Tabel berikutnya yaitu Indeks Kualitas Lingkungan Hidup divisualisasikan dengan peta persebaran. Hal ini dilakukan dengan mempertimbangkan aspek spasial dari data yaitu atribut Provinsi, dimana jika dimanfaatkan dengan baik aspek spasial tersebut akan semakin memudahkan pengguna/pembaca dalam memahami informasi yang disajikan.
 ![image](https://user-images.githubusercontent.com/107903297/174720090-70ed0c44-a23d-4b69-bf3d-26658a225053.png)

Visualisasi di atas juga dibuat agar lebih interaktif dengan menambahkan opsi tahun pada bagian yang ditandai dengan kotak merah. Dengan opsi tersebut pengguna akan bebas memilih data pada tahun berapa yang ingin ditampilkan. Selain itu, saat cursor di-hover ke wilayah dalam peta, akan muncul label yang menjelaskan nama provinsi dan IKLH dari provinsi tersebut. Besaran nilai indeks juga dapat dilihat dari kepekatan warna wilayah, semakin pekat semakin tinggi nilai indeksnya. Pengguna juga dapat memperbesar dan memperkecil tampilan peta, serta melakukan pencarian wilayah di dalam peta.
Data IKLH juga dapat dilihat perkembangannya dari tahun ke tahun menggunakan visualisasi line chart. Visualisasi ini akan menunjukkan tren atau kemajuan dari waktu ke waktu dan dapat digunakan untuk menampilkan berbagai kategori data yang kontinu. Tren atau perkembangan ini tidak mengalami gejolak yang signifikan, malah cenderung melandai dengan pola kenaikan sedikit demi sedikit pada tahun-tahun terakhir.
![image](https://user-images.githubusercontent.com/107903297/174720116-8664cd09-919d-48fe-a6f0-d7a16d36ce6e.png)

Pada visualisasi selanjutnya, terdapat 2 data yang disajikan dalam stacked bar chart. Visualisasi ini akan membandingkan banyak item yang berbeda dan menunjukkan komposisi setiap item yang dibandingkan.
![image](https://user-images.githubusercontent.com/107903297/174720618-1a7c4fd8-2ed8-4383-9c33-6f146a5eb138.png)

Visualisasi terakhir akan menyajikan data Luas Ekosistem & Kawasan Konservasi Terumbu Karang, Mangrove, dan Padang Lamun. Untuk mempermudah pemahaman informasi disajikan 5 pulau dengan ekosistem dan kawasan konservasi terluas. Jenis visualisasi yang tepat untuk informasi ini adalah bubble chart. Bubble chart akan merepresentasikan data dengan gelembung dan dimensi tambahan dari data yang dipresentasikan pula dalam ukuran gelembung dimana semakin besar gelembung maka semakin luas pula ekosistem dan kawasan konservasi di pulau tersebut.
![image](https://user-images.githubusercontent.com/107903297/174720685-82a21e04-279a-461d-be2e-458e243af797.png)

Agar layout atau penempatan visualisasi lebih efektif, ketiga data divisualisasikan dengan jenis yang sama. Lalu untuk mengubah tampilan sesuai jenis konservasi yang diinginkan, pengguna hanya perlu memilih pada opsi yang telah disediakan dan ditandai oleh kotak merah di atas.
Setelah semua data selesai divisualisasikan, langkah berikutnya adalah menggabungkannya ke dalam dashboard dengan terlebih dahulu menata layout dan menambah interpretasi data agar mudah dipahami. 

Berikut dilampirkan dashboard yang telah siap dipublikasikan:
![image](https://user-images.githubusercontent.com/107903297/174720779-612a364f-d32f-4648-b02a-d86a0320f88d.png)
