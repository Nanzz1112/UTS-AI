# Klasifikasi Tingkat Stres Mahasiswa dengan Logistic Regression

**Tugas Proyek UTS Mata Kuliah AI**

## Disusun oleh

- Dhananjaya (2501010023)
- Kadek Angga Putra Artawan (2501010030)
- I Gede Anggara Suryantara (2501010013)



---

## Pendahuluan

Tekanan yang dihadapi mahasiswa ada beragam, salah satunya ya dari akademik atau mungkin hal-hal lainnya. Hal ini sering memicu stres yang berdampak buruk pada kesehatan mental dan kemampuan mahasiswa dalam pembelajaran maupun kegiatannya sehari hari. Sering kali kita tidak sadar bahwa sedang mengalami stres, oleh karena itu kelompok kami memilih topik ini.

Dalam proyek ini dibuat sebuah model Machine Learning (ML) untuk mengklasifikasikan tingkat stres pada mahasiswa berdasarkan beberapa faktor yang dapat memengaruhi tingkat stres. Di sini kami menggunakan model/algoritma Logistic Regression, diharapkan model ini sesuai dan mampu menghasilkan hasil yang memuaskan.

## Data set dan jumlah data

Di sini kami menggunakan dataset kumpulan data tingkat stres yang kami cari di web data publik Kaggle. Dataset ini berbentuk tabel yang terdiri dari 21 kolom (berisi faktor yang memengaruhi dan target) dan 1.100 baris (responden). Dataset ini sudah diperiksa dan tidak ditemukan data kosong maupun duplikat sehingga dataset ini sudah bersih.

Menurut apa yang kita baca dan dapatkan, dataset ini berisi 20 faktor yang berpengaruh terhadap level stres. Dijelaskan bahwa faktor-faktor ini dipilih secara ilmiah dengan mempertimbangkan 5 faktor utama beberapa di antaranya yaitu:

- **Faktor psikologis** = tingkat kecemasan, harga diri, riwayat kesehatan mental, depresi.
- **Faktor fisiologis** = sakit kepala, tekanan darah, kualitas tidur, masalah pernapasan.
- **Faktor lingkungan** = tingkat kebisingan, kondisi tempat tinggal, keamanan, kebutuhan dasar.
- **Faktor akademik** = kinerja akademik, beban belajar, hubungan guru siswa, kekhawatiran karier masa depan.
- **Faktor sosial** = dukungan sosial, tekanan teman sebaya, aktivitas ekstrakurikuler, perundungan.

Semua faktor di atas akan menjadi bahan prediksi, dimana setiap faktor akan mempengaruhi penilaian terhadap level stres. Dihasilkan output berupa prediksi level stres yang terdiri dari 3 level (0 = stres rendah, 1 = stres sedang, 2 = stres tinggi).

## Model yang digunakan

Dalam tugas ini, untuk memprediksi tingkat stres mahasiswa diselesaikan menggunakan pendekatan supervised learning dengan tugas klasifikasi. Model/algoritma yang digunakan untuk menjalankannya adalah Logistic Regression.

Logistic Regression adalah salah satu algoritma di Supervised Machine Learning yang digunakan untuk tugas klasifikasi, dimana ia memprediksi probabilitas/peluang.

Awalnya kelompok kami menggunakan algoritma Random Forest, tapi hasil yang didapatkan tidak memuaskan.

Hasil output di latihan adalah 100% dan saat diuji/tes hasilnya 88%, dapat dilihat dari hasilnya sangat berbeda (terdapat jarak sekitar “12%”). Jadi saya melihatnya sebagai overfitting (kondisi ketika ML terlalu menghafal data latihan) dari saat melihat hasil latihannya 100%. Membuat kami berpikir untuk menggunakan model algoritma yang lain. Jadi digunakanlah model Logistic Regression yang hasil data latihannya 90% dan hasil tesnya 88% (terdapat jarak 2%) dimana hasilnya tergolong baik dan layak digunakan.

## Tahapan pengerjaan

1. **Pengumpulan data**

   Mencari dataset publik yang berkaitan dengan apa yang dibuat kelompok kami (level stres) dengan syarat ada 1000+ data yang dapat digunakan. Ditemukan dataset Tingkat stres mahasiswa di web Kaggle.

2. **Pemeriksaan data**

   Memeriksa dataset yang telah ditemukan apakah sudah bersih/lengkap (tidak ada nilai kosong dan data duplikat) dan sesuai untuk digunakan.

3. **Pembagian data**

   Dataset dibagi dengan rasio 80:20 (880 data latih dan 220 data uji). Supaya model memiliki data yang cukup besar untuk belajar, sekaligus menyisakan sejumlah data untuk diuji.

4. **Pelatihan model**

   Model dilatih menggunakan algoritma Logistic Regression (model utama) dan Random Forest (model pembanding). Awalnya Random Forest digunakan sebagai model utama tapi karena hasilnya overfitting sehingga membuat Logistic Regression dipertimbangkan sebagai model utama.

5. **Evaluasi/uji model**

   - **Logistic Regression**, memiliki akurasi data latih sekitar 90% dan data uji sekitar 88%.
   - **Random Forest**, memiliki akurasi data latih 100% dan data uji sekitar 88%.

6. **Menyimpulkan**

   Hasil data latih dan data uji dari kedua model (Logistic Regression dan Random Forest) membuat kami akhirnya memilih model Logistic Regression karena performa pada data latihan dan data uji yang paling memuaskan kami.

## Kesimpulan

Berdasarkan apa yang telah kami kerjakan, model untuk klasifikasi tingkat stres mahasiswa adalah algoritma Logistic Regression. Dimana menggunakan dataset publik yang kami temukan di Kaggle (memiliki 1000+ data) yang sudah cukup untuk memulai proyek ini.

Hasil pengujian menunjukkan bahwa model Logistic Regression mampu menghasilkan akurasi data latihan sekitar 90% dan akurasi data uji sekitar 88%. Dimana ini sudah bisa dinilai stabil dan mampu menghasilkan akurasi data yang baik dibandingkan model Random Forest sebagai model pembanding yang mengalami overfitting (akurasi data latih 100% dan data uji 88%).
