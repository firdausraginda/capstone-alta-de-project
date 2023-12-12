# Project Brief Template Data Engineering

## 💻 Technical Brief

## Contraints

- Data terpisah berasal dari multiple source seperti db, excel, dan data source yg lain.
- Constraint setiap problem akan spesifik ditentukan pada bagian project description.

### Requirements

- Melakukan pengambilan data, include orchestration, transformation. i.e., ETL) (Mandatory)
- Melakukan pengambilan data agregasi dari db + excel (Mandatory)
- Melakukan penerapan replication & sharding (Poin plus)
- Mengambil data secara real time (Poin plus)
- Membuat visualisasi (Poin plus)

### Project Description and Expected Delivereble

#### Background

Github adalah sebuah platform berbasis cloud yang digunakan oleh developer untuk menyimpan, mengelola dan mengontrol perubahan dari sebuah codebase, serta memfasilitasi developer untuk melakukan perubahan code secara kolaboratif. Terhitung lebih dari 100 juta developer di seluruh dunia menggunakan Github untuk mendukung pekerjaan mereka setiap harinya. Tidak heran jika Github memiliki ukuran total dataset yang sangat besar, hingga 3TB. 

Kita akan mengimplementasikan proses ELT (Extraction, Loading dan Transformation) pada dataset github di link [gharchives](https://www.gharchive.org/), alih-alih menggunakan dataset github yang sudah tersedia di [github BigQuery public dataset](https://console.cloud.google.com/marketplace/product/github/github-repos). Mengingat dataset github ini memiliki ukuran sangat besar, siswa hanya perlu memproses data selama setidaknya 2-5 hari (bebas dimulai sejak tanggal berapa).

Ada 2 hal yang dapat dipelajari oleh siswa, pertama dari sisi data engineering. Pada sisi Data Engineering, proses ELT pada dataset Github ini cukup menantang karena potensi ukuran data yang diproses > 1 GB setiap jamnya! Dengan ukuran data yang besar, seorang Data Engineer harus menentukan solusi yang lebih efisien pada tiap fase ELT. 

Kedua, dari sisi Data Analysis. Dengan melakukan analisis dan eksplorasi lebih dalam pada dataset github, siswa bisa memahami bagaimana melakukan query yang cost-efisien pada data besar. 


#### Expected Deliverable

Di akhir project, diharapkan siswa dapat membuat sebuah scheduled batch data pipeline (ELT), analisis dan visualisasi pada dashboard yang memiliki metrics antara lain: 
1. 10 top programming languages
2. Geographic distribution (country) of developers and their behaviors 
3. The distribution of specific events
4. 10 top developers who gave more stars
5. 10 most active organizations (count by number of PR submitted)

#### Success Criteria

Kriteria sukses/tidak project ini adalah, ketika hasil akhir memiliki: 
- Implementasi airflow/google cloud composer untuk workflow management: ingest data, transform data dengan airflow
- Implementasi PostgreSQL/BigQuery sebagai datawarehouse
- Implementasi dbt untuk proses transformasi data (implementasi data model sederhana)
- Implementasi metabase/google looker sebagai media visualisasi
- Step by step penjelasan tentang bagaimana cara me-replikasi project tersebut

Nice to have: 
- Implementasi CI/CD
- Test and data validation

#### Documentation

- [trend dan insight Github Events di tahun 2022](https://ossinsight.io/blog/trends-and-insights-from-github-2022/)

#### Assest

- [github events dataset](https://www.gharchive.org/)

## 📆 Schedule Meeting and Format Mentoring

### Schedule Mentoring

- Mentoring dilakukan 3x dalam sepekan dengan alokasi 60 menit mentoring tiap sesi.
- Jadwal Mentoring dapat menyesuaikan jadwal mentor dan disepakati bersama dengan team, jika ada perubahan mentor dan tim terkait bisa langsung mengkomunikasikan.
- Mentoring bisa dilakukan hari senin-jumat atau sabtu-minggu sesuai availability mentor dan team.

### Mentoring Alocation

| Mentoring | Allocation Time | Agenda                                                      |
| --------- | --------------- | ----------------------------------------------------------- |
| Part 1    | 15 minutes      | Update Team in General                                      |
|           |                 | Update Every Member of The Team                             |
|           |                 | Showing Progress Based On Project Management Tools (Trello) |
| Part 2    | 45 minutes      | Discussion topics according to the problem at hand          |

## ⚠️ General Rules

### Hal-hal yang harus dilakukan oleh Mentees dan Team

- Setiap individu wajib berkontribusi & aktif berkomunikasi dalam team (yang tidak berkontribusi maka tidak mendapatkan nilai, nilai diberikan kenapa yang berkontribusi aktif).
- Setiap team wajib memiliki group komunikasi (membuat group telegram).
- Setiap team wajib menggunakan trello untuk management task & membagi task dg proporsional setiap member.
- Setiap team wajib mengadakan daily meeting setiap hari untuk berkoordinasi.

### Tindakan yang dianggap sebagai pelanggaran bagi Mentees dan Team

- Individu yang tidak aktif atau slow response dalam berkomunikasi dg tim (tidak membalas komunikasi team lebih dari 2 jam saat jam aktif: 9 am - 9 pm).
- Individu tidak ikut berkontribusi dalam mengerjakan task.
- Tim yang tidak membuat group komunikasi.
- Tim tidak menggunakan trello.
- Tim tidak melakukan pembagian tugas.
- Tim yang tidak mengadakan daily meeting.
