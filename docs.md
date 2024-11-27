# Laporan Proyek Machine Learning

## Anggota:
- Naufal Arsapradhana (225150701111028)
- Ahmad Faiz Agustianto (225150707111068)
- Kevin Joasua Situmorang (225150707111057)

## Domain Proyek

> **"Pendidikan adalah kunci menuju kemajuan bangsa."**  
Namun, berdasarkan laporan **Programme for International Student Assessment (PISA) 2022** dari **OECD** menunjukkan bahwa kualitas pendidikan Indonesia mengalami penurunan signifikan. Berikut adalah hasil skor rata-rata siswa Indonesia dibandingkan rata-rata OECD

| **Bidang**      | **Skor Indonesia (2022)** | **Rata-rata OECD (2022)** |
|------------------|--------------------------|---------------------------|
| **Matematika**   | 366                      | 472                       |
| **Membaca**      | 359                      | 476                       |
| **Sains**        | 383                      | 485                       |

Hanya **18% siswa** Indonesia yang mencapai tingkat kemahiran minimal (Level 2) dalam matematika, jauh di bawah rata-rata OECD sebesar **69%**. Lebih memprihatinkan, hampir **tidak ada siswa** Indonesia yang masuk kategori berprestasi tinggi (Level 5 atau 6).

Kondisi ini dipengaruhi oleh berbagai faktor internal dan eksternal. Misalnya, faktor eksternal seperti **kualitas fasilitas belajar** dan **tingkat pendapatan orang tua**, serta faktor internal seperti **motivasi siswa** dan **kebiasaan belajar**. Selain itu, dampak pandemi COVID-19 yang memaksa penutupan sekolah hingga lebih dari tiga bulan turut memberikan pengaruh negatif pada hasil belajar siswa.


![Sokr PSA Indonesia](https://github.com/user-attachments/assets/057878bb-8435-4c95-9f64-7a2a8d114c1d)
<br />
<sup>Sumber: [Data Kualitas Pendidikan Siswa Indonesia](https://dataindonesia.id/pendidikan/detail/data-kualitas-pendidik)</sup>

Selain itu, sesuai dengan data pada diagram di atas, ditinjau dari skor literasi atau membaca, Indonesia memiliki nilai rata-rata sebesar 359 pada 2022. Angka tersebut menurun 12 poin dibandingkan periode 2018 dengan skor 371. Kemudian, skor numerasi atau perhitungan matematika Indonesia sebesar 366 poin. Nilainya juga turun 13 poin dibandingkan tahun 2018 dengan nilai 379 poin. Selain itu, penilaian sains yang dimiliki Indonesia sebesar 383 poin. Angkanya juga menurun dari 2018 yang sebesar 396 poin.

Untuk mengatasi tantangan ini, pendekatan berbasis data dapat memberikan wawasan yang lebih dalam untuk mendesain intervensi pendidikan yang sesuai. Analisis berbasis data memungkinkan prediksi performa akademik yang lebih akurat dan membantu menciptakan strategi pembelajaran yang disesuaikan dengan kebutuhan individu siswa. Hal ini penting untuk meningkatkan kualitas pendidikan guna mendukung visi Indonesia Emas 2045. 

Pendekatan inovatif ini sejalan dengan rekomendasi OECD untuk mengatasi kesenjangan pendidikan melalui pembelajaran yang lebih adaptif dan terfokus pada kebutuhan siswa, terutama mereka yang berasal dari kelompok kurang beruntung.

Referensi:
- [OECD. (2023). PISA 2022 Results (Volume I and II) - Country Notes](https://www.oecd.org/en/publications/pisa-2022-results-volume-i-and-ii-country-notes_ed6fbcc5-en/indonesia_c2e1ae0e-en.html)
- [OECD Education GPS. (2023). Indonesia - Student Performance (PISA 2022)](https://gpseducation.oecd.org/CountryProfile?primaryCountry=IDN&treshold=10&topic=PI)
- [Data Indonesia. (2023). Data Kualitas Pendidikan Siswa di Indonesia Berdasarkan Hasil PISA 2022](https://dataindonesia.id/pendidikan/detail/data-kualitas-pendidikan-siswa-di-indonesia-berdasarkan-hasil-pisa-2022)


## Business Understanding

Pada bagian ini, terdapat proses klarifikasi masalah yang terdiri dari pernyataan masalah yang melatar belakangi proyek ini dan tujuan proyek dalam menjawab permasalahan yang ada.

### Problem Statements
1. Mengapa kualitas pendidikan di Indonesia mengalami penurunan berdasarkan hasil PISA 2022?
2. Bagaimana keberagaman cara belajar, kebiasaan, dan latar belakang siswa mempengaruhi performa akademik mereka?
3. Mengapa intervensi pendidikan yang diberikan belum sesuai dengan kebutuhan siswa?
4. Apa saja faktor eksternal yang mempengaruhi performa akademik siswa, seperti fasilitas belajar, aktivitas ekstrakurikuler, dan pendapatan orang tua?
5. Bagaimana faktor internal seperti jam tidur, tingkat motivasi, dan durasi belajar siswa mempengaruhi pencapaian akademik mereka?

### Goals
1. Menganalisis penyebab penurunan kualitas pendidikan di Indonesia berdasarkan hasil PISA 2022.
2. Mengidentifikasi pengaruh keberagaman cara belajar, kebiasaan, dan latar belakang siswa terhadap performa akademik mereka
3. Merancang pendekatan intervensi pendidikan yang lebih sesuai dengan kebutuhan siswa berdasarkan hasil analisis.
4. Mengevaluasi dampak faktor eksternal, seperti fasilitas belajar, aktivitas ekstrakurikuler, dan pendapatan orang tua, terhadap performa akademik siswa.
5. Mengukur pengaruh faktor internal, seperti jam tidur, tingkat motivasi, dan durasi belajar, terhadap pencapaian akademik siswa.

### Solution statements
Berdasarkan pernyataan masalah di atas, terdapat beberapa solusi yang dapat dikembangkan untuk menjawab permasalahan tersebut. Diperlukan adanya pendekatan berbasis data yang memungkinkan prediksi performa akademik dengan lebih akurat serta memberikan wawasan mendalam mengenai intervensi pendidikan yang dibutuhkan. Pendekatan berbasis data ini merujuk kepada pengembangan model Machine Learning yang membantu instansi dan pihak pendidikan untuk dapat memprediksi performa siswa berdasarkan faktor eksternal dan internal.

Solusi ini membandingkan 3 algoritma untuk mencari algoritma yang paling efektif dan sesuai untuk mengembangkan sistem prediksi yang sesuai dengan faktor eksternal dan internal siswa. 

 Berikut adalah algoritma yang digunakan:

| **Algoritma**                | **Deskripsi**                                                                                            |
|-------------------------------|---------------------------------------------------------------------------------------------------------|
| Support Vector Regressor  | Menggunakan hyperplane untuk memisahkan data dengan margin maksimal, efektif untuk data berukuran kecil.    |
| Random Forest Regressor   | Memanfaatkan kombinasi pohon keputusan untuk menghasilkan prediksi yang lebih stabil dan akurat.            |
| K-Neighbors Regressor     | Membandingkan data berdasarkan tetangga terdekat, cocok untuk data dengan pola hubungan sederhana.          |

Kemudian, instansi dan pihak pendidikan dapat secara efektif memberikan intervensi fasilitas pendidikan sesuai dengan kebutuhan siswa dalam meningkatkan performa akademik mereka.

## Data Understanding

Pada proyek ini, data yang digunakan bertujuan untuk menganalisis faktor-faktor yang mempengaruhi performa akademik siswa. Dataset ini dapat diakses melalui [Student Performance Factors Dataset di Kaggle](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors/data). Dataset ini mencakup informasi mengenai faktor eksternal dan internal yang dapat mempengaruhi performa akademik siswa dalam ujian matematika dan bahasa Portugis.

### Variabel-variabel pada **Student Performance Factors Dataset**:
| **Attribute**                | **Description**                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **Hours_Studied**            | Jumlah jam yang dihabiskan siswa untuk belajar per minggu.                                                      |
| **Attendance**               | Persentase kelas yang dihadiri oleh siswa.                                                                      |
| **Parental_Involvement**     | Tingkat keterlibatan orang tua dalam pendidikan siswa (``Low``, ``Medium``, ``High``).                                       |
| **Access_to_Resources**      | Ketersediaan sumber daya pendidikan (``Low``, ``Medium``, ``High``).                                                        |
| **Extracurricular_Activities**| Partisipasi dalam kegiatan ekstrakurikuler (``Yes``, ``No``).                                                           |
| **Sleep_Hours**              | Rata-rata jumlah jam tidur per malam yang dimiliki siswa.                                                       |
| **Previous_Scores**          | Nilai ujian dari ujian sebelumnya.                                                                              |
| **Motivation_Level**         | Tingkat motivasi belajar siswa (``Low``, ``Medium``, ``High``).                                                             |
| **Internet_Access**          | Ketersediaan akses internet di rumah (``Yes``, ``No``).                                                                 |
| **Tutoring_Sessions**        | Jumlah sesi les tambahan yang dihadiri per bulan.                                                               |
| **Family_Income**            | Tingkat pendapatan keluarga (``Low``, ``Medium``, ``High``).                                                                |
| **Teacher_Quality**          | Kualitas pengajaran yang diberikan oleh guru (``Low``, ``Medium``, ``High``).                                               |
| **School_Type**              | Jenis sekolah yang dihadiri (``Public``, ``Private``).                                                                  |
| **Peer_Influence**           | Pengaruh teman-teman terhadap performa akademik siswa (``Positive``, ``Neutral``, ``Negative``).                             |
| **Physical_Activity**        | Rata-rata jumlah jam kegiatan fisik yang dilakukan siswa per minggu.                                            |
| **Learning_Disabilities**    | Adanya gangguan belajar pada siswa (``Yes``, ``No``).                                                                   |
| **Parental_Education_Level** | Tingkat pendidikan orang tua (``High School``, ``College``, ``Postgraduate``).                                              |
| **Distance_from_Home**       | Jarak dari rumah ke sekolah (``Near``, ``Moderate``, ``Far``).                                                              |
| **Gender**                   | Jenis kelamin siswa (``Male``, ``Female``).                                                                             |
| **Exam_Score**               | Nilai ujian akhir siswa, yang menjadi variabel target untuk prediksi performa akademik.                         |

### Data Overview
Untuk melihat lebih dalam isi data, kita dapat menggunakan perintah

```python
# Menampilkan semua data di dalam dataset
data = pd.read_csv('/content/drive/MyDrive/StudentPerformanceFactors.csv')
data
```

| **Hours_Studied** | **Attendance** | **Parental_Involvement** | **Access_to_Resources** | **Extracurricular_Activities** | **Sleep_Hours** | **Previous_Scores** | **Motivation_Level** | **Internet_Access** | **Tutoring_Sessions** | **Family_Income** | **Teacher_Quality** | **School_Type** | **Peer_Influence** | **Physical_Activity** | **Learning_Disabilities** | **Parental_Education_Level** | **Distance_from_Home** | **Gender** | **Exam_Score** |
|--------------------|----------------|--------------------------|-------------------------|--------------------------------|-----------------|----------------------|-----------------------|---------------------|------------------------|-------------------|---------------------|-----------------|--------------------|----------------------|---------------------------|----------------------------|------------------------|------------|----------------|
| 23                 | 84             | Low                      | High                    | No                             | 7               | 73                   | Low                   | Yes                 | 0                      | Low               | Medium              | Public          | Positive           | 3                    | No                        | High School              | Near                   | Male       | 67             |
| 19                 | 64             | Low                      | Medium                  | No                             | 8               | 59                   | Low                   | Yes                 | 2                      | Medium            | Medium              | Public          | Negative           | 4                    | No                        | College                 | Moderate               | Female     | 61             |
| 24                 | 98             | Medium                   | Medium                  | Yes                            | 7               | 91                   | Medium                | Yes                 | 2                      | Medium            | Medium              | Public          | Neutral            | 4                    | No                        | Postgraduate             | Near                   | Male       | 74             |
| 29                 | 89             | Low                      | Medium                  | Yes                            | 8               | 98                   | Medium                | Yes                 | 1                      | Medium            | Medium              | Public          | Negative           | 4                    | No                        | High School              | Moderate               | Male       | 71             |
| 19                 | 92             | Medium                   | Medium                  | Yes                            | 6               | 65                   | Medium                | Yes                 | 3                      | Medium            | High                | Public          | Neutral            | 4                    | No                        | College                 | Near                   | Female     | 70             |
| ...                | ...            | ...                      | ...                     | ...                            | ...             | ...                  | ...                   | ...                 | ...                    | ...               | ...                 | ...             | ...                | ...                  | ...                       | ...                     | ...                    | ...        | ...              |

Untuk melihat informasi lebih lanjut tentang tipe data dan kolom yang ada di dataset, kita dapat menggunakan perintah

```python
data.info()
```

```plaintext
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 6607 entries, 0 to 6606
Data columns (total 20 columns):
 #   Column                      Non-Null Count  Dtype 
---  ------                      --------------  ----- 
 0   Hours_Studied               6607 non-null   int64 
 1   Attendance                  6607 non-null   int64 
 2   Parental_Involvement        6607 non-null   object
 3   Access_to_Resources         6607 non-null   object
 4   Extracurricular_Activities  6607 non-null   object
 5   Sleep_Hours                 6607 non-null   int64 
 6   Previous_Scores             6607 non-null   int64 
 7   Motivation_Level            6607 non-null   object
 8   Internet_Access             6607 non-null   object
 9   Tutoring_Sessions           6607 non-null   int64 
 10  Family_Income               6607 non-null   object
 11  Teacher_Quality             6529 non-null   object
 12  School_Type                 6607 non-null   object
 13  Peer_Influence              6607 non-null   object
 14  Physical_Activity           6607 non-null   int64 
 15  Learning_Disabilities       6607 non-null   object
 16  Parental_Education_Level    6517 non-null   object
 17  Distance_from_Home          6540 non-null   object
 18  Gender                      6607 non-null   object
 19  Exam_Score                  6607 non-null   int64 
dtypes: int64(7), object(13)
```

Untuk mengetahui jumlah baris dan kolom dalam dataset, kita dapat menggunakan perintah
```python
# Mengetahui jumlah baris dan kolom dalam dataset
data.shape
```
```plaintext
(6607, 20)
```

Berdasarkan informasi yang diperoleh dari dataset, terdapat **6607 entri** dan **20 kolom** dengan berbagai tipe data, baik numerik maupun kategorikal. Dataset ini mencakup faktor-faktor eksternal dan internal yang mempengaruhi performa akademik siswa, seperti **jam belajar**, **keterlibatan orang tua**, **akses ke sumber daya**, **kualitas guru**, serta **aktivitas ekstrakurikuler**. Data ini juga menunjukkan adanya beberapa kolom dengan nilai yang hilang, seperti **Teacher_Quality**, **Parental_Education_Level**, dan **Distance_from_Home**.

## Data Preparation
Pada bagian ini, dilakukan beberapa teknik **data preparation** untuk memastikan data yang digunakan dalam model prediksi bersih dan siap diproses lebih lanjut. Berikut adalah tahapan-tahapan yang dilakukan dalam proses persiapan data:

### Pengecekan untuk Data null
Pertama, dilakukan pengecekan terhadap kolom-kolom yang memiliki nilai null atau hilang dengan menggunakan
```python
# Melakukan pengecekan untuk data null
print(data.isnull().sum())
```
```plaintext
Hours_Studied                 0
Attendance                    0
Parental_Involvement          0
Access_to_Resources           0
Extracurricular_Activities    0
Sleep_Hours                   0
Previous_Scores               0
Motivation_Level              0
Internet_Access               0
Tutoring_Sessions             0
Family_Income                 0
Teacher_Quality               78
School_Type                   0
Peer_Influence                0
Physical_Activity             0
Learning_Disabilities         0
Parental_Education_Level      90
Distance_from_Home            67
Gender                        0
Exam_Score                    0
dtype: int64
```

Langkah ini dilakukan untuk mengidentifikasi kolom yang memiliki data hilang (null). Data yang hilang dapat mempengaruhi kualitas analisis dan pemodelan

### Visualisasi Missing Data
Untuk lebih memahami distribusi data yang hilang, dilakukan visualisasi dengan diagram batang untuk melihat jumlah nilai hilang di setiap kolom.
```python
# Memvisualisasikan kolom yang memiliki null value
missing_data = data.isnull().sum()

# Visualisasi menggunakan diagram batang
missing_data.plot(kind='bar', figsize=(8, 4))
plt.title("Missing Values Count by Column")
plt.ylabel("Number of Missing Values")
plt.show()
```
![Missing Value by Column](https://github.com/user-attachments/assets/5efe7a14-bc1f-4266-a26a-a8f657d5a6c8)


Visualisasi ini membantu untuk memberikan gambaran yang jelas dan cepat mengenai sebaran data yang hilang di setiap kolom

### Imputation
Untuk menangani nilai yang hilang, dilakukan imputasi data dengan ketentuan:
- Menggunakan nilai rata-rata (``mean``) untuk mengisi nilai yang hilang pada kolom numerik.
- Menggunakan nilai terbanyak (``most_frequent``) untuk mengisi nilai yang hilang pada kolom kategorikal.

```python
# Imputasi data numerik
num_imputer = SimpleImputer(strategy='mean')
data[numerical_cols] = num_imputer.fit_transform(data[numerical_cols])

# Imputasi data kategorikal
cat_imputer = SimpleImputer(strategy='most_frequent')
data[categorical_cols] = cat_imputer.fit_transform(data[categorical_cols])
```

Imputasi dilakukan untuk mengganti nilai yang hilang dengan nilai yang masuk akal, yaitu rata-rata untuk data numerik dan nilai terbanyak untuk data kategorikal. Tanpa imputasi, nilai yang hilang bisa menyebabkan error atau bias dalam model prediksi

Setelah imputasi, dilakukan pengecekan kembali untuk memastikan tidak ada lagi nilai null dalam dataset.

```python
# Melakukan pengecekan untuk kolom dengan null value
print(data.isnull() .sum())
```
```plaintext
Hours_Studied                 0
Attendance                    0
Parental_Involvement          0
Access_to_Resources           0
Extracurricular_Activities    0
Sleep_Hours                   0
Previous_Scores               0
Motivation_Level              0
Internet_Access               0
Tutoring_Sessions             0
Family_Income                 0
Teacher_Quality               0
School_Type                   0
Peer_Influence                0
Physical_Activity             0
Learning_Disabilities         0
Parental_Education_Level      0
Distance_from_Home            0
Gender                        0
Exam_Score                    0
dtype: int64
```

Pengecekan ini memastikan bahwa tidak ada nilai yang hilang setelah proses imputasi, yang membuat dataset siap digunakan untuk model tanpa ada kekurangan data.


Terakhir, dilakukan pengecekan untuk memastikan tidak ada data duplikat dalam dataset.

```python
# Melakukan pengecekan adanya duplikasi data
data.duplicated().sum()
```
```plaintext
0
```

Pengecekan duplikasi dilakukan untuk memastikan dataset bersih dari entri yang terulang.

### Label Encoding

Pada bagian ini, dilakukan encoding pada data kategorikal agar dapat digunakan dalam pemodelan machine learning. Algoritma machine learning biasanya memerlukan data numerik untuk dapat memproses dan melakukan prediksi. **Label Encoding** digunakan untuk mengonversi kategori dalam fitur kategorikal menjadi bentuk numerik.

#### Visualisasi Distribusi Data pada Kolom Kategorikal
Hal ini bertujuan untuk memahami frekuensi kemunculan setiap kategori dalam setiap kolom kategorikal.

```python
# Membuat visualisasi distribusi data pada kolom kategorikal
num_columns = len(data_categorical_cols.columns)
plt.figure(figsize=(15, 5 * (num_columns // 2 + num_columns % 2)))

# Membuat grafik untuk setiap kolom dan mem-plot nilai unik
for i, column in enumerate(data_categorical_cols.columns):
    plt.subplot((num_columns // 2 + num_columns % 2), 2, i + 1)  
    unique_values = data_categorical_cols[column].value_counts() 
    sns.barplot(x=unique_values.index, y=unique_values.values)
    # Memberi label pada grafik
    plt.title(f'Unique Values in {column}')
    plt.xlabel(column)
    plt.ylabel('Count')
    plt.xticks(rotation=45)

# Mengatur tata letak
plt.tight_layout()
plt.show()
```
![Distribution Bar Plot](https://github.com/user-attachments/assets/2338a54c-e5b5-4c14-ae36-6f18999bb207)


#### Proses Label Encoding
langkah selanjutnya adalah melakukan Label Encoding untuk mengonversi kategori menjadi angka. Ini dilakukan dengan menggunakan LabelEncoder dari library ``scikit-learn``.

```python
from sklearn.preprocessing import LabelEncoder

label_encoder = LabelEncoder()

# Mengaplikasikan LabelEncoder untuk setiap kolom data kategorikal
for column in categorical_cols:
    data[f'{column}_encoded'] = label_encoder.fit_transform(data[column])

# Menampilkan 5 baris pertama setelah Label Encoding
data.head()
```

| **Hours_Studied** | **Attendance** | **Parental_Involvement_encoded** | **Access_to_Resources_encoded** | **Extracurricular_Activities_encoded** | **Sleep_Hours** | **Previous_Scores** | **Motivation_Level_encoded** | **Internet_Access_encoded** | **Tutoring_Sessions** | **Family_Income_encoded** | **Teacher_Quality_encoded** | **School_Type_encoded** | **Peer_Influence_encoded** | **Physical_Activity** | **Learning_Disabilities_encoded** | **Parental_Education_Level_encoded** | **Distance_from_Home_encoded** | **Gender_encoded** | **Exam_Score** |
|-------------------|----------------|----------------------------------|---------------------------------|----------------------------------------|-----------------|----------------------|-----------------------------|-----------------------------|-----------------------|---------------------------|---------------------------|------------------------|----------------------------|-----------------------|---------------------------------|--------------------------------------|---------------------------|-----------------|--------|
| 23.0              | 84.0           | 1                                | 1                               | 0                                      | 7.0             | 73.0                 | 1                           | 1                           | 0.0                   | 1                         | 2                         | 1                        | 2                          | 0                     | 1                               | 2                                    | 1                         | 1               | 67              |
| 19.0              | 64.0           | 1                                | 0                               | 0                                      | 8.0             | 59.0                 | 1                           | 1                           | 2.0                   | 2                         | 2                         | 1                        | 0                          | 0                     | 0                               | 0                                    | 1                         | 0               | 61              |
| 24.0              | 98.0           | 2                                | 0                               | 1                                      | 7.0             | 91.0                 | 2                           | 1                           | 2.0                   | 2                         | 2                         | 1                        | 1                          | 0                     | 2                               | 2                                    | 1                         | 1               | 74              |
| 29.0              | 89.0           | 1                                | 0                               | 1                                      | 8.0             | 98.0                 | 2                           | 1                           | 1.0                   | 2                         | 2                         | 1                        | 0                          | 0                     | 1                               | 1                                    | 1                         | 1               | 71              |
| 19.0              | 92.0           | 2                                | 0                               | 1                                      | 6.0             | 65.0                 | 2                           | 1                           | 3.0                   | 2                         | 0                         | 1                        | 1                          | 0                     | 0                               | 2                                    | 0                         | 0               | 70              |

- Label Encoding bertujuan untuk mengubah data kategorikal menjadi bentuk numerik, sehingga bisa digunakan oleh algoritma machine learning.
- Setiap kategori unik dalam kolom kategorikal akan diberi label numerik.
- Distribusi ini dapat menentukan apakah perlu dilakukan tindakan seperti encoding, resampling, atau pengelompokan ulang kategori agar model dapat berfungsi lebih baik.

### Scaler
Pada bagian ini, dilakukan scaling data numerik untuk memastikan data berada dalam skala yang teratur sebelum diproses ke dalam model. 

#### StandardScaler dan MinMaxScaler
- **StandardScaler** digunakan untuk mengubah data sehingga memiliki distribusi dengan rata-rata (mean) 0 dan standar deviasi (standard deviation) 1.
  
  **Rumus Transformasi StandardScaler**:
  \[
  z = \frac{x - \mu}{\sigma}
  \]
  di mana:
  - \( x \) adalah nilai data
  - \( \mu \) adalah rata-rata dari data
  - \( \sigma \) adalah standar deviasi dari data

- **MinMaxScaler** digunakan untuk mengubah data ke dalam skala tertentu, biasanya antara 0 dan 1 (default).
  
  **Rumus Transformasi MinMaxScaler**:
  \[
  x' = \frac{x - \min(x)}{\max(x) - \min(x)}
  \]
  di mana:
  - \( x \) adalah nilai data
  - \( \min(x) \) adalah nilai minimum dari data
  - \( \max(x) \) adalah nilai maksimum dari data

#### Penerapan Scaler pada Kolom Data
```python
# Mengubah skala data pada kolom tertentu menggunakan Standard Scaler dan MinMax Scaler
from sklearn.preprocessing import StandardScaler, MinMaxScaler

# Mengaplikasikan StandardScaler pada variabel yang mempunyai distribusi normal
scaler = StandardScaler()

data[['Hours_Studied', 'Sleep_Hours', 'Physical_Activity']] = scaler.fit_transform(
    data[['Hours_Studied', 'Sleep_Hours', 'Physical_Activity']]
)

# Mengaplikasikan MinMaxScaler untuk data berskala antara 0, 1 secara default
min_max_scaler = MinMaxScaler()

data[['Attendance', 'Previous_Scores']] = min_max_scaler.fit_transform(
    data[['Attendance', 'Previous_Scores']]
)
```

Tujuan dari Scaling:

- Beberapa algoritma seperti SVM dan KNN sensitif terhadap skala data. Scaling memastikan bahwa setiap variabel memiliki pengaruh yang setara dalam model.
- Tanpa scaling, data dengan skala besar (misalnya, 1.000.000 vs. 0,1) dapat menyebabkan model memberikan bobot yang tidak proporsional terhadap variabel berskala besar.
- Scaling membantu meningkatkan akurasi dan efisiensi model dengan memastikan bahwa data memiliki skala yang seragam.

```python
data.head()
```

| **Hours_Studied** | **Attendance** | **Parental_Involvement** | **Access_to_Resources** | **Extracurricular_Activities** | **Sleep_Hours** | **Previous_Scores** | **Motivation_Level** | **Internet_Access** | **Tutoring_Sessions** | **Family_Income** | **Teacher_Quality** | **School_Type** | **Peer_Influence** | **Physical_Activity** | **Learning_Disabilities** | **Parental_Education_Level** | **Distance_from_Home** | **Gender** | **Exam_Score** |
|-------------------|----------------|--------------------------|--------------------------|-------------------------------|-----------------|----------------------|-----------------------|----------------------|-----------------------|------------------|--------------------|----------------|-------------------|------------------------|---------------------------|----------------------------|-------------------------|------------|---------------|
| 0.504942          | 0.600          | Low                      | High                     | No                            | -0.019796       | 0.46                 | Low                   | Yes                  | 0.0                   | 1                | 2                  | 1              | 2                 | 0                      | 1                         | 2                          | 1                       | 1          | 67            |
| -0.162822         | 0.100          | Low                      | Medium                   | No                            | 0.661399        | 0.18                 | Low                   | Yes                  | 2.0                   | 2                | 2                  | 1              | 0                 | 0                      | 0                         | 0                          | 1                       | 0          | 61            |
| 0.671882          | 0.950          | Medium                   | Medium                   | Yes                           | -0.019796       | 0.82                 | Medium                | Yes                  | 2.0                   | 2                | 2                  | 1              | 1                 | 0                      | 2                         | 2                          | 1                       | 1          | 74            |
| 1.506587          | 0.725          | Low                      | Medium                   | Yes                           | 0.661399        | 0.96                 | Medium                | Yes                  | 1.0                   | 2                | 2                  | 1              | 0                 | 0                      | 1                         | 1                          | 1                       | 1          | 71            |
| -0.162822         | 0.800          | Medium                   | Medium                   | Yes                           | -0.700990       | 0.30                 | Medium                | Yes                  | 3.0                   | 2                | 0                  | 1              | 1                 | 0                      | 0                         | 2                          | 0                       | 0          | 70            |

#### Tipe Data Setelah Scaling

```python
# Melihat tipe data pada data setelah di transformasi
data.dtypes
```
```plaintext
Hours_Studied 	float64
Attendance 	float64
Parental_Involvement 	object
Access_to_Resources 	object
Extracurricular_Activities 	object
Sleep_Hours 	float64
Previous_Scores 	float64
Motivation_Level 	object
Internet_Access 	object
Tutoring_Sessions 	float64
Family_Income 	object
Teacher_Quality 	object
School_Type 	object
Peer_Influence 	object
Physical_Activity 	float64
Learning_Disabilities 	object
Parental_Education_Level 	object
Distance_from_Home 	object
Gender 	object
Exam_Score 	float64
Parental_Involvement_encoded 	int64
Access_to_Resources_encoded 	int64
Extracurricular_Activities_encoded 	int64
Motivation_Level_encoded 	int64
Internet_Access_encoded 	int64
Family_Income_encoded 	int64
Teacher_Quality_encoded 	int64
School_Type_encoded 	int64
Peer_Influence_encoded 	int64
Learning_Disabilities_encoded 	int64
Parental_Education_Level_encoded 	int64
Distance_from_Home_encoded 	int64
Gender_encoded 	int64
```

- StandardScaler dan MinMaxScaler digunakan untuk memastikan data berada pada skala yang konsisten.
- Scaling penting untuk model yang sensitif terhadap skala data seperti SVM dan KNN, yang membantu meningkatkan performa dan efisiensi model.


### Feature Engineering
Pada bagian ini, dilakukan beberapa teknik **feature engineering** untuk memanipulasi dan memilih fitur yang penting dalam dataset.

#### Memilih Kolom Numerik
Langkah pertama adalah memilih kolom-kolom yang berisi data numerik dari dataset untuk analisis lebih lanjut.
```python
# Memilih kolom yang berisi data numerik
numerical_all_colslist = data.select_dtypes(include=['float64', 'int64','int32']).columns

# Membuat subset data
numerical_all_cols = data[numerical_all_colslist]

# Menampilkan lima baris pertama
numerical_all_cols.head()
```

| **Hours_Studied** | **Attendance** | **Sleep_Hours** | **Previous_Scores** | **Tutoring_Sessions** | **Physical_Activity** | **Exam_Score** | **Parental_Involvement_encoded** | **Access_to_Resources_encoded** | **Extracurricular_Activities_encoded** | **Motivation_Level_encoded** | **Internet_Access_encoded** | **Family_Income_encoded** | **Teacher_Quality_encoded** | **School_Type_encoded** | **Peer_Influence_encoded** | **Learning_Disabilities_encoded** | **Parental_Education_Level_encoded** | **Distance_from_Home_encoded** | **Gender_encoded** |
|-------------------|----------------|-----------------|---------------------|------------------------|------------------------|----------------|----------------------------------|---------------------------------|----------------------------------------|--------------------------------|-----------------------------|---------------------------|----------------------------|--------------------------|---------------------------|------------------------------------|------------------------------------|---------------------------|-----------------|
| 0.504942          | 0.600          | -0.019796       | 0.46                | 0.0                    | 0.031411               | 67.0           | 1                                | 0                               | 0                                      | 1                              | 1                           | 1                         | 2                          | 1                        | 2                         | 0                                | 1                                  | 2                          | 1               |
| -0.162822         | 0.100          | 0.661399        | 0.18                | 2.0                    | 1.001199               | 61.0           | 1                                | 2                               | 0                                      | 1                              | 1                           | 2                         | 2                          | 1                        | 0                         | 0                                | 1                                  | 0                          | 0               |
| 0.671882          | 0.950          | -0.019796       | 0.82                | 2.0                    | 1.001199               | 74.0           | 2                                | 2                               | 1                                      | 2                              | 1                           | 2                         | 2                          | 1                        | 1                         | 0                                | 2                                  | 2                          | 1               |
| 1.506587          | 0.725          | 0.661399        | 0.96                | 1.0                    | 1.001199               | 71.0           | 1                                | 2                               | 1                                      | 2                              | 1                           | 2                         | 2                          | 1                        | 0                         | 0                                | 1                                  | 1                          | 1               |
| -0.162822         | 0.800          | -0.700990       | 0.30                | 3.0                    | 1.001199               | 70.0           | 2                                | 2                               | 1                                      | 2                              | 1                           | 2                         | 0                          | 1                        | 1                         | 0                                | 0                                  | 2                          | 0               |


#### Korelasi Antar Kolom
Setelah memilih kolom numerik, dilakukan perhitungan matriks korelasi antar kolom numerik untuk mengetahui hubungan antar fitur. Korelasi ini dihitung menggunakan fungsi ``.corr()`` dan divisualisasikan menggunakan heatmap.

```python
# Menggunakan Correlation Matrix antar kolom
corr_matrix = numerical_all_cols.corr()
plt.figure(figsize=(12, 8))
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.show()
```
![Heatmap 1](https://github.com/user-attachments/assets/ac260910-e0ab-42b9-8ae2-c6a47681cbdd)

Korelasi mengukur sejauh mana dua variabel numerik berkaitan secara linear, dengan nilai antara -1 (hubungan negatif sempurna) hingga +1 (hubungan positif sempurna).

#### Menghapus Kolom dengan Korelasi Lemah
Setelah melihat korelasi antar kolom, dilakukan penghapusan kolom dengan korelasi yang lemah terhadap target.

```python
# Menghapus kolom 'Sleep_Hours' dan 'Physical_Activity' karena memiliki korelasi yang lemah pada performa ujian siswa
data_numerical_all_cols = numerical_all_cols.drop(['Sleep_Hours', 'Physical_Activity'], axis=1)
data_numerical_all_cols.head()
```
- Menghilangkan fitur yang tidak penting untuk menghindari model yang kompleks dan menjaga agar model tetap sederhana dan efisien.
- Memastikan hanya fitur yang memiliki korelasi signifikan dengan target yang digunakan untuk pelatihan model.

#### Korelasi Antar Kolum Terbaru
```python
corr_matrix = data_numerical_all_cols.corr()
plt.figure(figsize=(12, 8))
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.show()
```
![Heatmap 2](https://github.com/user-attachments/assets/fe369fc2-b9bc-4623-819e-16ba167453fa)


#### Menghapus Kolom dengan Korelasi Lemah
Pada langkah ini, dilakukan penyederhanaan dataset dengan menghapus fitur yang tidak terlalu berpengaruh atau relevan
```python
# Menghapus fitur yang kurang penting
data_numerical_all_cols_Gender = numerical_all_cols.drop(['Gender_encoded', 'Family_Income_encoded','Learning_Disabilities_encoded', 'Internet_Access_encoded'], axis=1)
data_numerical_all_cols_Gender.head()
```

#### Visualisasi Korelasi Terakhir Setelah Penghapusan Fitur
Setelah penghapusan fitur yang kurang penting, dilakukan visualisasi ulang matriks korelasi untuk memastikan hanya fitur yang signifikan yang tersisa dalam dataset.
```python
final_data = data_numerical_all_cols_Gender

# Korelasi setelah penghapusan fitur kurang penting
corr_matrix = final_data.corr()
plt.figure(figsize=(12, 8))
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.show()
```
| **Hours_Studied** | **Attendance** | **Previous_Scores** | **Tutoring_Sessions** | **Exam_Score** | **Parental_Involvement_encoded** | **Access_to_Resources_encoded** | **Extracurricular_Activities_encoded** | **Motivation_Level_encoded** | **Internet_Access_encoded** | **Family_Income_encoded** | **Teacher_Quality_encoded** | **School_Type_encoded** | **Peer_Influence_encoded** | **Parental_Education_Level_encoded** | **Distance_from_Home_encoded** |
|-------------------|----------------|---------------------|------------------------|----------------|----------------------------------|---------------------------------|----------------------------------------|--------------------------------|-----------------------------|---------------------------|----------------------------|--------------------------|---------------------------|------------------------------------|------------------------------------|
| 0.504942          | 0.600          | 0.46                | 0.0                    | 67.0           | 1                                | 0                               | 0                                      | 1                              | 1                           | 1                         | 2                          | 1                        | 2                         | 1                                | 2                                  |
| -0.162822         | 0.100          | 0.18                | 2.0                    | 61.0           | 1                                | 2                               | 0                                      | 1                              | 1                           | 2                         | 2                          | 1                        | 0                         | 0                                | 1                                  |
| 0.671882          | 0.950          | 0.82                | 2.0                    | 74.0           | 2                                | 2                               | 1                                      | 2                              | 1                           | 2                         | 2                          | 1                        | 1                         | 0                                | 2                                  |
| 1.506587          | 0.725          | 0.96                | 1.0                    | 71.0           | 1                                | 2                               | 1                                      | 2                              | 1                           | 2                         | 2                          | 1                        | 0                         | 0                                | 1                                  |
| -0.162822         | 0.800          | 0.30                | 3.0                    | 70.0           | 2                                | 2                               | 1                                      | 2                              | 1                           | 2                         | 0                          | 1                        | 1                         | 0                                | 2                                  |

- Memastikan bahwa dataset yang tersisa hanya berisi fitur-fitur yang penting dan relevan untuk analisis lebih lanjut.

Proses **data preparation** yang dilakukan mencakup pengecekan nilai yang hilang dan imputasi dengan menggunakan rata-rata untuk kolom numerik dan nilai terbanyak untuk kolom kategorikal. Setelah imputasi, data diperiksa kembali dan tidak ditemukan nilai yang hilang. Selain itu, dilakukan scaling pada beberapa kolom numerik dan label encoding pada kolom kategorikal untuk memastikan data siap digunakan dalam model machine learning. Kolom yang tidak relevan berdasarkan analisis korelasi juga dihapus untuk menyederhanakan dataset.

## Modeling
Pada tahap ini, dilakukan proses pemodelan untuk memprediksi nilai ujian akhir siswa (**Exam_Score**) berdasarkan faktor-faktor internal dan eksternal. Proses ini mencakup pembagian data, standarisasi fitur, dan pelatihan model menggunakan tiga algoritma berbeda: **Random Forest Regressor**, **Support Vector Regressor (SVR)**, dan **K-Neighbors Regressor (KNN)**. Berikut adalah tahapan yang dilakukan:

### Pembagian Dataset (Train-Test Split)
Dataset dibagi menjadi dua bagian utama:
- **Training Set (80%)**: Digunakan untuk melatih model.
- **Testing Set (20%)**: Disisihkan untuk evaluasi model di tahap berikutnya.

```python
from sklearn.model_selection import train_test_split

# Membagi data menjadi fitur (X) dan target (y)
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```
- Memastikan model memiliki data yang berbeda untuk pelatihan dan pengujian sehingga evaluasi model menjadi lebih objektif.
- Mengurangi risiko overfitting dengan menyediakan data yang tidak pernah dilihat model selama pelatihan.

### Standarisasi Fitur (Feature Scaling)
Setelah membagi data, dilakukan proses standarisasi untuk memastikan semua fitur berada pada skala yang sama. Hal ini dilakukan menggunakan ``StandardScaler`` dari scikit-learn:

```python
from sklearn.preprocessing import StandardScaler

# Standarisasi fitur
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)  
```
- Menormalkan data untuk model yang sensitif terhadap skala data, seperti Support Vector Regressor (SVR) dan K-Neighbors Regressor (KNN).
- Meningkatkan stabilitas numerik algoritma dan membantu model berperforma lebih baik.

### Pemilihan dan Inisialisasi Model
Tiga algoritma machine learning digunakan dalam proses ini untuk membangun model prediksi. Berikut adalah model yang digunakan:
- Random Forest Regressor: Model ensemble berbasis pohon keputusan.
- Support Vector Regressor (SVR): Model yang menggunakan hyperplane dan kernel untuk prediksi.
- K-Neighbors Regressor (KNN): Model berbasis instance yang memprediksi target berdasarkan tetangga terdekat.

```python
from sklearn.ensemble import RandomForestRegressor
from sklearn.svm import SVR
from sklearn.neighbors import KNeighborsRegressor

# Model Training, Cross-Validation, and Evaluation
from sklearn.model_selection import cross_val_score

from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
from sklearn.preprocessing import StandardScaler

# Inisialisasi Model
classifiers = [
    RandomForestRegressor(),
    SVR(),
    KNeighborsRegressor()
] 
```
- Memilih algoritma yang sesuai untuk memprediksi nilai ujian akhir siswa berdasarkan faktor-faktor yang tersedia.
- Menginisialisasi model dengan parameter default sebelum melanjutkan ke proses pelatihan.

### Tanpa StandardScaler
Proses pertama dilakukan tanpa menggunakan standarisasi fitur untuk mengetahui performa awal model pada data mentah. Langkah-langkahnya mencakup validasi silang (``cross-validation``) dan pelatihan model.
```python
withoutresults = {}
for model in classifiers:
  model_name = model.__class__.__name__
   print(f"\nTraining {model_name}...")

  # Melakukan validasi silang (5-fold cross-validation) untuk mengevaluasi performa model secara lebih umum menggunakan skor R
  cv_scores = cross_val_score(model, X_train, y_train, cv=5, scoring='r2')

  # Menyesuaikan model dengan training set
  model.fit(X_train, y_train)

  # Prediksi
  y_pred = model.predict(X_test)

  # Metriks evaluasi
  r2 = r2_score(y_test, y_pred)
  mae = mean_absolute_error(y_test, y_pred)
  mse = mean_squared_error(y_test, y_pred)

  # Menyimpan hasil
  withoutresults[model_name] = {
      "CV R²": np.mean(cv_scores),
      "Test R²": r2,
      "MAE": mae,
      "MSE": mse
}
```
- Melakukan validasi silang untuk mengevaluasi performa model pada data pelatihan dengan membagi data menjadi lima lipatan (folds).
- Melatih model menggunakan data pelatihan mentah untuk menghasilkan model dasar tanpa preprocessing tambahan.

### Menampilkan Hasil Tanpa StandardScaler
```python
# Menampilkan hasil
for model_name, metrics in withoutresults.items():
    print(f"\nModel: {model_name}")
    for metric_name, value in metrics.items():
        print(f"{metric_name}: {value:.4f}")
```

```plaintext
Model: RandomForestRegressor
CV R²: 0.6141
Test R²: 0.6482
MAE: 1.1597
MSE: 4.9728

Model: SVR
CV R²: 0.6808
Test R²: 0.7325
MAE: 0.7647
MSE: 3.7814

Model: KNeighborsRegressor
CV R²: 0.2701
Test R²: 0.2970
MAE: 2.2265
MSE: 9.9364
```

Hasil Pengukuran:
| Model | CV R² | Test R² | MAE | MSE |
| --- | --- | --- | --- | --- |
| RandomForestRegressor | 0.6183 | 0.6560 | 1.1392 | 4.8629 |
| SVR (Support Vector Regressor) | 0.6808 | 0.7325 | 0.7647 | 3.7814 |
| KNeighborsRegressor | 0.2701 | 0.2970 | 2.2265 | 9.9364 |

- SVR adalah model terbaik berdasarkan metrik evaluasi, karena memiliki skor R² tertinggi dan error terendah.
- Model Random Forest cukup kompetitif, tetapi tidak sebaik SVR.
- Model K-Neighbors memiliki performa terburuk yang mungkin disebabkan oleh sensitivitasnya terhadap ukuran dataset atau distribusi data.

### Dengan StandardScaler
Proses berikutnya dilakukan dengan menggunakan data yang telah di-scaling menggunakan StandardScaler. Standarisasi ini memastikan bahwa model yang sensitif terhadap skala data dapat bekerja lebih optimal.
```python
results = {}
for model in classifiers:
    model_name = model.__class__.__name__
    print(f"\nTraining {model_name}...")

    # Cross-validation (5-fold)
    cv_scores = cross_val_score(model, X_train_scaled, y_train, cv=5, scoring='r2')

    # Menyesuaikan model dengan training set
    model.fit(X_train_scaled, y_train)

    # Prediksi
    y_pred = model.predict(X_test_scaled)

    # Metriks evaluasi
    r2 = r2_score(y_test, y_pred)
    mae = mean_absolute_error(y_test, y_pred)
    mse = mean_squared_error(y_test, y_pred)

    # Menyimpan hasil
    results[model_name] = {
      "CV R²": np.mean(cv_scores),
      "Test R²": r2,
      "MAE": mae,
      "MSE": mse
}
```
- Memanfaatkan data yang telah di-scaling untuk meningkatkan performa model yang sensitif terhadap skala data, seperti SVR dan KNN.
- Membandingkan hasil validasi silang antara model dengan dan tanpa scaling untuk menentukan dampak preprocessing terhadap performa model.

### Menampilkan Hasil Dengan StandardScaler
```python
# Menampilkan hasil
for model_name, metrics in results.items():
    print(f"\nModel: {model_name}")
    for metric_name, value in metrics.items():
        print(f"{metric_name}: {value:.4f}")
```

```plaintext
Model: RandomForestRegressor
CV R²: 0.6143
Test R²: 0.6456
MAE: 1.1511
MSE: 5.0096

Model: SVR
CV R²: 0.6825
Test R²: 0.7324
MAE: 0.7682
MSE: 3.7823

Model: KNeighborsRegressor
CV R²: 0.4700
Test R²: 0.4988
MAE: 1.6828
MSE: 7.0843
```

Hasil Pengukuran:

| Model | CV R² | Test R² | MAE | MSE |
| --- | --- | --- | --- | --- |
| RandomForestRegressor | 0.6184 | 0.6510 | 1.1548 | 4.9325 |
| SVR | 0.6825 | 0.7324 | 0.7682 | 3.7823 |
| KNeighborsRegressor | 0.4700 | 0.4988 | 1.6828 | 7.0843 |

- Proses ini mengubah data ke dalam bentuk distribusi normal dengan rata-rata 0 dan standar deviasi 1. Hal ini membantu algoritma tertentu seperti SVR dan KNeighborsRegressor, yang sensitif terhadap skala fitur.
- SVR adalah model terbaik dalam eksperimen ini, terutama karena sensitif terhadap data yang diskalakan dengan StandardScaler.
- Random Forest juga memberikan hasil yang cukup baik tetapi tidak seoptimal SVR.
- KNeighborsRegressor tidak bekerja dengan baik dalam skenario ini, mungkin karena sifat dataset yang lebih cocok untuk model non-lokal atau kompleks.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

Pada bagian ini, evaluasi dilakukan untuk menilai performa model yang telah dilatih menggunakan beberapa metrik evaluasi. Metrik yang digunakan adalah sebagai berikut:

## Evaluation

### Metrik Evaluasi

Untuk mengevaluasi performa model, digunakan beberapa metrik berikut:

- **CV R² (Cross-Validation R²)**: 
    \[
    R^2 = 1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2}
    \]
  Mengukur seberapa baik model memprediksi target dibandingkan rata-rata target dalam data pelatihan. Nilai mendekati 1 menunjukkan model mampu menjelaskan variabilitas target dengan baik.

- **R² (Coefficient of Determination)**: 
  - Formula sama seperti **CV R²**, tetapi dihitung pada data uji.
  - Menilai performa model pada data uji untuk mengetahui seberapa baik model mampu melakukan generalisasi. Nilai mendekati 1 menunjukkan prediksi model akurat.

- **MAE (Mean Absolute Error)**: 
   
    \[
    MAE = \frac{1}{n} \sum |y_i - \hat{y}_i|
    \]
  Mengukur rata-rata selisih absolut antara nilai prediksi (\(\hat{y}\)) dan nilai aktual (\(y\)). MAE memberikan interpretasi langsung tentang rata-rata error dalam unit asli data.

- **MSE (Mean Squared Error)**: 
    \[
    MSE = \frac{1}{n} \sum (y_i - \hat{y}_i)^2
    \]
  Mengukur rata-rata kuadrat dari selisih antara nilai prediksi (\(\hat{y}\)) dan nilai aktual (\(y\)). Karena menggunakan kuadrat, MSE lebih sensitif terhadap error besar, sehingga cocok untuk mendeteksi outlier.

### Model Comparison

#### Visualisasi Hasil dengan Bar Plot
```python
# Mengkonversi hasil ke pandas DataFrame
results_data = pd.DataFrame(results).T

# Mengubah index agar nama model sesuai dengan kolom
results_data = results_data.reset_index().rename(columns={'index': 'Model'})

# Memplot menggunakan Seaborn
metrics = ['CV R²', 'Test R²', 'MAE', 'MSE']
for metric in metrics:
    plt.figure(figsize=(10, 6))
    sns.barplot(x='Model', y=metric, data=results_data, palette='viridis')
    plt.title(f'Model Comparison for {metric}')
    plt.xticks(rotation=45)
    plt.show()
```

![Bar Plot CVR](https://github.com/user-attachments/assets/6c03cd1f-aa4c-4089-9598-6d3358d056e2)
![Bar Plor R](https://github.com/user-attachments/assets/f4e4c9b1-f59a-497b-b674-b137182b66f6)
![Bar Plot MAE](https://github.com/user-attachments/assets/1056f2a6-148b-4c91-86a8-464480f6cc4f)
![Bar Plot MSE](https://github.com/user-attachments/assets/c9d1c992-6778-48d5-8395-9c34c3d1dcfa)

#### Visualisasi Hasil dengan Scatter Plot
```python
# Visualisasi data menggunakan ScatterPlot
for metric in metrics:
    plt.figure(figsize=(10, 6))

    # Penggunaan ScatterPlot untuk setiap metriks
    sns.scatterplot(data=results_data, x='Model', y=metric, hue='Model', palette='viridis', s=100, marker='o')

    # Mengatur label title dan axis
    plt.title(f'Model Comparison for {metric}')
    plt.xticks(rotation=45)
    plt.ylabel(metric)

    # Kustomisasi legenda dan tata letak
    plt.legend(loc='best')
    plt.grid(True)
    plt.tight_layout()

    # Menampilkan plot
    plt.show()
```

![Scatter Plot CVR](https://github.com/user-attachments/assets/cfce6be5-bd89-455c-96a9-b4b85cb5d08a)
![Scatter Plot R](https://github.com/user-attachments/assets/5c2b4674-bfb1-4c4e-92fe-5d1cc843e1e0)
![Scatter Plot MAE](https://github.com/user-attachments/assets/4ca119c4-972e-4ec7-a5ef-1530292d5879)
![Scatter Plot MSE](https://github.com/user-attachments/assets/6910dd96-ef85-4040-9fe2-60d7269c3eea)


### Feature Importance Comparison
Perbandingan fitur penting dilakukan untuk melihat fitur mana yang memiliki kontribusi paling signifikan terhadap prediksi pada setiap model.

#### Analisis dan Visualisasi Individual
```python
# Menambahkan library yang diperlukan
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.inspection import permutation_importance

# Melakukan plotting untuk fitur penting
def plot_feature_importance(importances, feature_names, model_name):
    feature_importance_data = pd.DataFrame({
        'Feature': feature_names,
        'Importance': importances
    })
    feature_importance_data = feature_importance_data.sort_values(by='Importance', ascending=False)

    plt.figure(figsize=(10, 6))
    sns.barplot(x='Importance', y='Feature', data=feature_importance_data)
    plt.title(f'{model_name} - Feature Importance')
    plt.show()

# Untuk model dengan fitur penting bawaan
def get_feature_importance_native(model, X, model_name):
    try:
        importances = model.feature_importances_
        plot_feature_importance(importances, X.columns, model_name)
    except AttributeError:
        print(f"{model_name} does not have native feature importance")

# Untuk model tanpa fitur penting bawaan
def get_permutation_importance(model, X_test, y_test, X, model_name):
    result = permutation_importance(model, X_test, y_test, n_repeats=10, random_state=42)
    importances = result.importances_mean
    plot_feature_importance(importances, X.columns, model_name)

# Analisis fitur penting untuk setiap model
for model in classifiers:
    model_name = model.__class__.__name__

    print(f"Feature Importance for {model_name}:")

    if hasattr(model, 'feature_importances_'):
        # Native feature importance (tree-based models like RandomForest)
        get_feature_importance_native(model, X_train, model_name)
    else:
        # Permutation importance for models like SVR and KNeighbors
        get_permutation_importance(model, X_test_scaled, y_test, X_train, model_name)
```

![RandomForest Feature](https://github.com/user-attachments/assets/171f86d1-8ca7-415f-885e-9a81b30ccb4c)
![SVR Feature](https://github.com/user-attachments/assets/a816c8a2-22a7-4d3c-8f7e-bcbf095ac9c8)
![KNN Feature](https://github.com/user-attachments/assets/13cf8c04-128f-4fe2-a368-4f220055ac91)

#### Perbandingan Across Models
```python
from sklearn.inspection import permutation_importance

# Normalisasi value yang penting
def normalize_importance(importances):
    return importances / np.sum(importances)

# Esktraksi fitur penting
def get_feature_importance(model, X_train, X_test, y_train, y_test, model_name):
    try:
        if hasattr(model, 'feature_importances_'):
            importances = model.feature_importances_
        else:
            # Permutasi
            result = permutation_importance(model, X_test, y_test, n_repeats=10, random_state=42)
            importances = result.importances_mean

        # Normalisasi fitur penting untuk perbandingan
        normalized_importances = normalize_importance(importances)
        return normalized_importances
    except Exception as e:
        print(f"Could not compute feature importance for {model_name}: {e}")
        return None

# Inisialisasi dictionary untuk menyimpan fitur penting dari setiap model
feature_importance_comparison = {}

# Melakukan perhitungan dan menyimpan fitur penting pada setiap model
for model in classifiers:
    model_name = model.__class__.__name__
    print(f"Extracting feature importance for {model_name}...")

    # Pelatihan model
    model.fit(X_train_scaled, y_train)

    # Mendapatkan value yang penting
    importances = get_feature_importance(model, X_train_scaled, X_test_scaled, y_train, y_test, model_name)

    if importances is not None:
        feature_importance_comparison[model_name] = importances

# Membuat DataFrame untuk perbandingan
feature_importance_data = pd.DataFrame(feature_importance_comparison, index=X_train.columns)

# Pembagian perbandingan fitur penting dari setiap model
plt.figure(figsize=(12, 8))
feature_importance_data.plot(kind='bar', figsize=(12, 8))
plt.title("Feature Importance Comparison Across Models")
plt.xlabel("Features")
plt.ylabel("Normalized Importance")
plt.xticks(rotation=90)
plt.legend(loc='best')
plt.tight_layout()
plt.show()
```

![Models Feature](https://github.com/user-attachments/assets/0fa73304-35fe-4860-b24c-c5716874e1ea)



## Kesimpulan

Berdasarkan hasil pemodelan dan evaluasi, berikut adalah beberapa kesimpulan utama:

### 1. **Super Vector Regressor (SVR) sebagai Model Terbaik**
   **SVR** menjadi model terbaik berdasarkan performa pengujian pada metrik **R²**, **MAE**, dan **MSE**.

   **Mengapa SVR menjadi model terbaik?**
   - **R² Tertinggi (0.7355)**: SVR mampu menjelaskan variansi terbesar dalam variabel target (**Exam_Score**), menunjukkan bahwa model ini paling efektif dalam memprediksi hasil secara keseluruhan.
   - **MAE Terendah (0.7440)**: SVR menghasilkan kesalahan absolut rata-rata terkecil, yang berarti prediksi model lebih dekat dengan nilai sebenarnya dibandingkan dengan model lainnya.
   - **MSE Terendah (3.7384)**: Kesalahan kuadrat rata-rata terkecil menunjukkan bahwa SVR memiliki generalisasi yang lebih baik dan tingkat kesalahan yang lebih rendah dibandingkan model lainnya.

### 2. **Fitur Terbaik**
   - **Hours_Studied** dan **Attendance** adalah dua fitur yang konsisten dianggap paling penting dalam semua model yang digunakan.
   - Kedua fitur ini memiliki **skor kepentingan yang tinggi** (berdasarkan normalisasi), yang menunjukkan bahwa keduanya memiliki **hubungan yang sangat kuat** dengan variabel target, yaitu **performa akademik siswa**.

### 3. **Fitur Terendah**
   - Fitur seperti **Sleep_Hours**, **Tutoring_Sessions**, dan **Previous_Scores** menunjukkan tingkat kepentingan yang sedang dalam model **RandomForest**. Namun, fitur-fitur ini kurang menonjol dalam model linear seperti **SVR**.
   - Fitur lainnya, seperti **Physical_Activity**, **Motivation_Level_encoded**, **Parental_Involvement_encoded**, dan **Internet_Access_encoded**, memberikan **kontribusi yang sangat kecil** dalam model. Ini menunjukkan bahwa fitur-fitur tersebut mungkin memiliki **dampak terbatas** dalam memprediksi hasil akademik siswa.

---

### **Penilaian Akhir**
- **SVR** adalah model yang paling efektif dalam memprediksi nilai ujian akhir siswa, terutama karena kemampuannya untuk menangani data yang terdistribusi secara non-linear dengan baik.
- **Fitur yang paling penting**: **Hours_Studied** dan **Attendance** menjadi indikator utama yang mempengaruhi performa akademik.
- **Fitur yang kurang penting**: Beberapa fitur seperti **Sleep_Hours** dan **Parental_Involvement** memiliki kontribusi yang lebih kecil dalam memprediksi **Exam_Score**.


