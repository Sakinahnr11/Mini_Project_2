# Investigate Business Hotel using Data Visualization

## **Latar belakang**

Sangat penting bagi suatu perusahaan untuk selalu menganalisa performa bisnisnya. Pada kesempatan kali ini, kita akan lebih mendalami bisnis dalam bidang perhotelan. Fokus yang kita tuju adalah untuk mengetahui bagaimana perilaku pelanggan kita dalam melakukan pemesanan hotel, dan hubungannya terhadap tingkat pembatalan pemesanan hotel. Hasil dari insight yang kita temukan akan kita sajikan dalam bentuk data visualisasi agar lebih mudah dipahami dan bersifat lebih persuasif

## Alat

Saya telah menggunakan berbagai alat pada proyek ini. Saya menggunakan jupyter sebagai notebook, python sebagai bahasa pemrograman, kombinasi matplotlib dan perpustakaan seaborn untuk menghasilkan visualisasi data.

## Isi

## Data Preprocessing
**1. Handling Duplicated Data :** Saya menggunakan fungsi drop_duplicates() untuk menghapus baris duplikat dari dataframe.

**2. Handling Missing Values :** Kolom data yang hilang sangat tinggi seperti "company" dan "agent" tidak akan memberikan informasi yang signifikan, sehingga saya memutuskan untuk menghapus kolom tersebut dengan mengisi nilai kosongnya dengan 0. Saya juga mengisi nilai kosong di kolom "children" dengan 0, karena kemungkinan sebagian besar customer benar-benar tidak mempunyai anak. Sedangkan, nilai kosong di kolom "city" saya isi dengan label "unknown", karena kota mungkin tidak tersedia atau tidak terdeteksi.

**3. Handling Incorrect Value :** Saya menggantinya label kategori menjadi "No Meal" yang lebih deskriptif. Saya juga melakukan perubahan tipe data pada kolom “children”, “agent”, dan “company”. Hal ini dilakukan karena kolom-kolom tersebut mewakili angka diskrit dan harus memiliki tipe data integer untuk melakukan analisis lebih lanjut.

**4. Drop Unnecessary Data :** Saya perlu memastikan jumlah total customer pada setiap pesanan. Selanjutnya, baris-baris yang tidak relevan dengan jumlah pelanggan atau durasi menginap yang tidak valid telah saya hapus. Hal ini memastikan data yang diproses memiliki nilai yang valid dan relevan untuk analisis lebih lanjut.

## Analisis Data

### Monthly Hotel Booking Analysis Based on Hotel Type
Grafik ini memberikan wawasan tentang bagaimana jumlah rata-rata total pemesanan berubah sepanjang tahun untuk kedua jenis hotel. Baik City Hotel maupun Resort Hotel menunjukkan fluktuasi bulanan dalam jumlah pemesanan, dengan beberapa bulan mencatat pemesanan yang lebih tinggi daripada bulan lainnya. Perubahan tren ini dapat dipengaruhi oleh berbagai faktor seperti musim, liburan, acara khusus, dan kebijakan pemasaran hotel. Analisis lebih lanjut dapat membantu hotel-hotel ini dalam perencanaan dan strategi pemasaran mereka untuk meningkatkan jumlah pemesanan secara keseluruhan.

### Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates

 - City Hotel memiliki rasio pembatalan yang lebih tinggi daripada Resort Hotel untuk durasi menginap yang lebih lama (2 minggu, 3 minggu, dan 4 minggu).
 - Resort Hotel cenderung memiliki rasio pembatalan yang lebih rendah untuk semua durasi menginap, dengan rasio pembatalan terendah terjadi untuk durasi menginap 1 minggu.
 - Durasi menginap 1 minggu memiliki rasio pembatalan terendah di kedua jenis hotel.
 - Informasi ini dapat membantu manajemen hotel untuk memahami pola pembatalan pesanan dan mengidentifikasi durasi menginap yang berisiko tinggi untuk pembatalan. Dengan demikian, mereka dapat mengambil langkah-langkah untuk mengurangi pembatalan, meningkatkan kepuasan pelanggan, dan meningkatkan efisiensi operasional.
 
### Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate
- Diagram tersebut menggambarkan bahwa City Hotel memiliki rasio pembatalan yang lebih tinggi dibandingkan dengan Resort Hotel untuk semua grup lead time.
- Resort Hotel cenderung memiliki rasio pembatalan yang lebih rendah, terutama untuk pemesanan dengan lead time yang lebih pendek.
- Pemesanan dengan lead time yang sangat lama, yaitu 11-12 bulan dan lebih dari 12 bulan, memiliki risiko pembatalan yang tinggi, terutama di City Hotel.
- Informasi ini dapat membantu manajemen hotel dalam merencanakan strategi pemasaran dan kebijakan pembatalan yang lebih efektif. Dengan memahami pola pembatalan berdasarkan lead time, hotel dapat mengambil langkah-langkah untuk mengurangi tingkat pembatalan dan meningkatkan tingkat konversi pemesanan, sehingga meningkatkan efisiensi operasional dan kepuasan pelanggan.
