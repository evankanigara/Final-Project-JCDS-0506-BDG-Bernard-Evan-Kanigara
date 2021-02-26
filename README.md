# Final-Project-JCDS-0506-BDG-Bernard-Evan-Kanigara
Memprediksi pekerja yang akan melakukan 'attrition' (pengunduran diri) pada sebuah perusahaan

## Latar Belakang
Employee Attrition merupakan sebuah kondisi di mana perusahaan kehilangan pekerjanya. Hal tersebut dapat terjadi karena berbagai macam alasan, sebut saja alasan personal, rendahnya kepuasan di kantor, gaji yang kurang, dan lingkungan kerja yang buruk. Perusahaan yang kehilangan pekerjanya dapat merugi karena perusahaan telah menginvestasikan dana dan waktu untuk merekrut dan melatih pekerjanya. Memprediksi pekerja yang akan melakukan attrition dapat digunakan untuk mencegah pekerja resign. Perusahaan dapat melaukan pendekatan ke pekerja yang bersangkutan agar kecenderungan pekerja untuk pergi menjadi menurun. Selain itu, prediksi dapat digunakan sebagai tolak ukur evaluasi terhadap lingkungan kerja itu sendiri.  

## Tujuan
Memprediksi pekerja yang akan melakukan attrition berdasarkan data dari rekam jejak kerjanya selama di perusahaan. 

## Data 
Data terdiri dari 1470 baris dan 35 kolom. Fitur-fiturnya terdiri dari:
- Age: Umur
- BusinessTravel: Frekuensi perjalanan kantor
- DailyRate: Upah Harian
- Department: Departemen 
- DistanceFromHome: Jarak rumah dari kantor
- Education: Tingkatan pendidikan (ordinal)
- EducationField: Bidang studi pendidikan
- EnvironmentStatisfaction: Tingkat kepuasan pekerja terhadap lingkungan kerjanya
- Gender: Gender
- Hourlyrate: Upah perjam
- JobInvolvement: Jumlah proyek perusahaan yang pernah digeluti
- JobLevel: Tingakatan jabatan
- JobRole: Subdivisi dalam perusahaan
- JobStatisfaction: Tingkat kepuasaan pekerja terhadap tugas kerjanya
- MaritalStatus: Hubungan dengan pasangan
- MonthlyIncome: Gaji bulanan
- MonthlyRate: Upah bulanan
- NumCompaniesWorked: Jumlah perusahaan yang pernah ditempati
- OverTime: Status lembur
- PercentSalaryHike: Jumlah persentase kenaikan gaji
- PerformanceRating: Tingkat performa kerja
- RelationshipSatisfaction: Tingkat kebahagiaan dalam hubungan 
- StockOptionLevel: Jumlah opsi saham yang dimiliki
- TotalWorkingYears: Lamanya bekerja dalam tahun
- TrainingTimesLastYear: Lamanya bekerja tahun lalu
- WorkLifeBalance: Kualitas work life balance
- YearsAtCompany: Lama kerja di perusahaan saat ini
- YearsInCurrentRole: Lama kerja di divisi saat ini
- YearsSinceLastPromotion: Lama tahun sejak promosi terakhir
- YearsWithCurrManager: Lama tahun dengan manajer saat ini

## Visualisasi Data
### Pekerja yang lembur cenderung untuk resign
<img src='/static/visual1.png'>
### Semakin lama pekerja berada pada perusahaan maka cenderung untuk tidak melakukan resign
<img src='/static/visual2.png'>


## Pre-processing Data
<img src='/static/drawio.jpg'>
Proses pembersihan dan transformasi dilakukan dalam sebuah pipeline. Dalam pipeline dilakukan imputasi untuk meng-handle missing values. Lalu setelah itu dilakukan standarisasi. Untuk data categorical dilakukan encode berupa one hot encoder. PCA juga dilakukan pada fitur yang memiliki korelasi yang cukup tinggi. Setelah proses cleaning dan transformasi maka akan dilakukan feature selection menggunakan RFE. Jumlah data yang tidak berimbang akan diimbangi dengan oversampling SMOTE. Setelah itu data akan siap untuk dilatih dalam model yang sudah dipilih. 
