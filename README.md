<p align="center"> 
  <img src="img/img_1.jpeg" alt="Data Ranger Logo" width="250px" height="200px">
</p>
<h1 align="center"> Data Ranger </h1>

<h4 align="center">A data scientist team constitutes of 8 hailed accross various expertises</h4>

![-----------------------------------------------------](img/img_2.png)

## ⚡ Overview

<p align="justify"> 
  To summarize this world of project, a financial industry wishes to lift their sales of deposit by increasing the conversion rate that was about only 11% into 15%, the number of new customers captured divided by the size of population exposed, by running a campaign of business team. We are as a data scientist team assigned to figure out this case and offering several business recommendation
</p>

![-----------------------------------------------------](img/img_2.png)

## 💡 Insights and Business Recommendations

<p align="center"> 
  <img src="img/img_3.png" alt="Age Feature Insight" width="650px" height="250px">
</p>

<h3>⭐️ Insight</h3>

<p align="justify">
  Nasabah dewasa awal dengan umur dibawah 30 tahun memiliki nilai conversion rate yang tertinggi disusul dengan nasabah era silver age dengan umur diatas 50 tahun. Nasabah silver segment ini cenderung untuk memilih deposito dengan fixed rate sebagai low risk investment mereka sekaligus menjadi passive income pada usia menjelang masa retirement/pensiun.
</p>

<h3>📝 Business Strategy</h3>

<p align="justify"> 
  Mengerucutkan target marketing pada nasabah dewasa awal yang telah memiliki wawasan akan pentingnya investasi deposito dan nasabah diatas 50 tahun yang membutuhkan produk deposito dimana sesuai dengan produk yang sedang dilakukan campaign oleh tim marketing
</p>

![-----------------------------------------------------](img/img_2.png)

<p align="center"> 
  <img src="img/img_4.png" alt="Job Feature Insight" width="600px" height="300px">
</p>

<h3>⭐️ Insight</h3>

<p align="justify">
  Nasabah dengan occupation student dan retired menunjukkan nilai conversion rate tertinggi, hal ini sejalan dengan insight yang telah diidentifikasi berdasarkan fitur age
</p>

<h3>📝 Business Strategy</h3>

<p align="justify"> 
  Selain menargetkan kedua segment tersebut, dirasa perlu untuk memberikan perhatian pada occupation management dan blue-collar dimana kelompok tersebut memiliki karir dan golongan terpelajar sehingga perlu diberikan pengarahan akan esensi dari produk deposito
</p>

![-----------------------------------------------------](img/img_2.png)

<p align="center"> 
  <img src="img/img_5.png" alt="Duration Feature Insight" width="650px" height="250px">
</p>

<h3>⭐️ Insight</h3>

<p align="justify">
  Durasi telephone diatas 10 menit menyumbang nilai conversion rate yang paling tinggi, namun hal tersebut akan membuat pengeluaran program campaign semakin melambung seiring dengan meningkatnya durasi penawaran melalui telephone
</p>

<h3>📝 Business Strategy</h3>

<p align="justify"> 
  Untuk mengoptimalkan campaign dari berbagai dimensi, pertimbangan yang kami berikan adalah memaksimalkan waktu 5 menit untuk memberikan penawaran pada nasabah yang memiliki kapasitas untuk meningkatkan potensi konversi
</p>

![-----------------------------------------------------](img/img_2.png)

<p align="center"> 
  <img src="img/img_6.png" alt="Education Feature Insight" width="350px" height="300px">
</p>

<h3>⭐️ Insight</h3>

<p align="justify">
  Nasabah dengan tingkat education tertiary memiliki nilai conversion rate paling tinggi, sedangkan pendidikan primary dan secondary membentuk lebih dari 65% nasabah
</p>

<h3>📝 Business Strategy</h3>

<p align="justify"> 
  Memberikan persepsi kepada nasabah dengan tingkat pendidikan dan pengetahuan finansial lebih rendah akan substansi dan benefit dari produk investasi deposito untuk hari tua nantinya
</p>

![-----------------------------------------------------](img/img_2.png)

<p align="center"> 
  <img src="img/img_7.png" alt="Campaign Feature Insight" width="650px" height="250px">
</p>

<h3>⭐️ Insight</h3>

<p align="justify">
  Hubungan antar tiap segment fitur campaign dan kelas/target menunjukkan bahwa nasabah yang menerima contact dalam campaign sebanyak 1 - 2 kali memiliki nilai conversion rate yang paling tinggi. Semakin banyak penawaran yang diterima nasabah kecenderungan konversi semakin rendah.
</p>

<h3>📝 Business Strategy</h3>

<p align="justify"> 
  Identifikasi nasabah dari sekitar 66% target menjadi lebih spesifik karena hanya sekitar 13% yang memutuskan untuk konversi
</p>

![-----------------------------------------------------](img/img_2.png)

<h3>📝 Data Preparation</h3>

<h3>⭐️ Handling Null Values dan Data Duplikat</h3>
<p align="justify"> 
  Dari data yang diperoleh, tidak terdapat data null dan data duplikat.
</p>

<h3>⭐️ Handling Outliers</h3>
<p align="justify"> 
  Untuk pengolahan Outlier dilakukan dengan zscore. Terdapat 2.038 data outlier yang di remove. Kami mempertimbangkan untuk penanganan outliers menggunakan Z-score untuk menentukan seberapa jauh suatu data berada dari rata-rata, dengan Z-score tinggi dianggap sebagai outlier atau nilai ekstrem , kami mempertimbangkan dengan memilih z-score dikarenakan kami tidak ingin kehilangan banyak data. Dikarenakan data nya tidak berdistribusi normal maka kami melakukan log transformasi terlebih dahulu.
</p>

<h3>⭐️ Normalisasi</h3>
<p align="justify"> 
Sebelum dilakukan scalling dengan normalization, data perlu di split terlebih dahulu, menjadi train dan test. Normalization dipilih menjadi metode transformation karena merupakan metode yang paling umum digunakan.
</p>

<h3>⭐️ Feature Encoding</h3>
<p align="justify"> 
Fitur-fitur kategorikal perlu di-encode menjadi representasi numerik agar dapat digunakan dalam model. dengan label encoding pada kolom married,education, default, housing, loan dan month.
</p>
<p align="justify"> 
untuk kolom month di jadikan 4 kuartal menjadi 'month quarter' dan one hot encoding untuk kolom job, contact dan month quarter
</p>

<h3>⭐️ Class Imbalance</h3>
<p align="justify"> 
Dikarenakan fitur target 'y' itu memiliki data imbalance maka kami mempertimbangkan untuk handling class imbalance dengan SMOTE
</p>

<h3>⭐️ Feature Selection and Engineering</h3>
<p align="center"> 
  <img src="img/img_8.png" alt="Data Ranger Logo" width="250px" height="200px">
</p>
<p align="justify"> 
Berdasarkan hasil validasi model menggunakan filter method yang mengukur mean recall scoring parameter pada beberapa persentase fitur yang terlibat dalam proses pembentukan model diperoleh kondisi optimal dengan memanfaatkan percentile 60 dari fitur atau sekitar 11 fitur dari eksperimen yang berjumlah 19 fitur. Daftar fitur yang menjadi bahan pertimbangan adalah age, balance, is_married, education_mapped, is_default, is_housing, job, is_poutcome_success, duration, campaign, pdays.
</p>

<p align="center"> 
  <img src="img/img_9.png" alt="Data Ranger Logo" width="250px" height="200px">
</p>
<p align="justify"> 
Metode Recursive Feature Elimination berperan dalam menentukan jumlah fitur penyusun model melalui penghapusan/eliminasi fitur yang memiliki nilai koefisien terendah secara iteratif untuk seluruh kombinasi fitur yang tersedia guna memperoleh nilai mean test recall yang paling optimal. Mengacu pada grafik, kondisi ideal mampu mengakomodasi sekitar 8 fitur yaitu age, balance, is_married, education_mapped, is_default, is_housing, is_loan dan job.
</p>

<p align="justify"> 
Merujuk pada kedua metode yang mampu merekomendasikan fitur pembentuk model, maka ditentukan fitur yang berkontribusi terhadap predictor yaitu age, balance, is_married, education_mapped, is_default, is_housing, is_loan dan job.
</p>


![-----------------------------------------------------](img/img_2.png)

### 💙 Our Contributors

<p align="left"> 
  🐼 <b>Hunayn Risatayn<b><br>
  🐼 <b>Indah Kusuma Wardani<b><br>
  🐼 <b>Nindy Salsabila Hanin Zahra<b><br>
  🐼 <b>Athira Syifa Puti Salim<b><br>
  🐼 <b>Zery Triputra<b><br>
  🐼 <b>M. Khairul Ardi<b><br>
  🐼 <b>Muhamad Amar Nadhif<b><br>
  🐼 <b>Andriansyah Firdimas<b>
</p>
