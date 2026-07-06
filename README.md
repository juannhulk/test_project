# Assignment 30 - Portofolio 
## Project ini bertujuan untuk membuat analisis tentang Tube Station di London pada tahun 2016 dan 2017.
### Pada dataset ini terdapat jumlah entry/exit pada weekday dan weekend di London Underground system. 
#### Jumlah entry/exit yang tertera dihitung harian. 

File bisa diakses di [London Underground Stations & Usage Kaggle](https://www.kaggle.com/datasets/jonbown/london-tube-station-usage?resource=download&select=2017_Entry_Exit.csv)
#### Data yang diambil hanya dari tahun 2016 dan 2017 saja (for assignment purpose) 
Step-by-step:
- Menggabungkan kedua data csv 2016 dan 2017
- Mencari 5 Borough teratas dengan volume penumpang tertinggi dalam 2 periode tersebut
- Analisis Perilaku Penumpang: Komuter vs Rekreasi pada weekday vs weekend
- Analisis Aliran Massa Entry vs Exit untuk melihat apakah volume orang yang masuk sama dengan jumlah yang keluar

### 📊 Top 5 Borough dengan Volume Penumpang Tertinggi
<img width="1189" height="590" alt="image" src="https://github.com/user-attachments/assets/a390ea21-091c-438d-8104-14912b23c760" />

| Borough | Total Volume (Juta) | Rata-Rata (Juta) | Nilai Tengah (Juta) | Jumlah Stasiun |
| :--- | :--- | :--- | :--- | :--- |
| **City of Westminster** | 81,524.32 | 1,314.91 | 196.08 | 62 |
| **Camden** | 37,726.79 | 1,178.96 | 350.98 | 32 |
| **City of London** | 25,505.13 | 1,275.25 | 353.08 | 20 |
| **Lambeth** | 23,514.42 | 1,469.65 | 279.12 | 16 |
| **Kensington and Chelsea**| 19,181.83 | 799.24 | 155.06 | 24 |

*Insight: Westminster memiliki total volume tertinggi, namun selisih yang ekstrem antara rata-rata (1.314) dan nilai tengah (196) menunjukkan bahwa volume tersebut didorong oleh segelintir stasiun transit raksasa, bukan kepadatan yang merata di 62 stasiunnya.*

### 🚇 Analisis Perilaku Penumpang: Komuter vs Rekreasi

Analisis ini bertujuan untuk memetakan fungsi utama setiap stasiun London Tube dengan membandingkan rasio volume penumpang di akhir pekan terhadap hari kerja. Pendekatan ini mengungkap dua karakteristik stasiun yang saling bertolak belakang.

---
#### 1. Beban Utama Jaringan: Stasiun Karakteristik Komuter
Sebagian besar stasiun dengan volume hari kerja tertinggi mengalami penurunan penumpang yang sangat drastis pada hari Sabtu dan Minggu (Rasio < 0.5).

#### 🏢 Top 10 Stasiun Dominan Komuter (Trafik Hari Kerja Sangat Sibuk)

| Station | Borough | Total Hari Kerja | Total Akhir Pekan | Rasio Rekreasi |
| :--- | :--- | :--- | :--- | :--- |
| **Moorgate** | City of London | 46,698 | 9,784 | 0.21 |
| **Moorgate** | City of London | 48,408 | 10,663 | 0.22 |
| **Farringdon** | Islington | 31,421 | 10,505 | 0.33 |
| **Farringdon** | Islington | 36,844 | 12,618 | 0.34 |
| **Chancery Lane** | City of London | 31,085 | 12,137 | 0.39 |
| **Chancery Lane** | City of London | 32,922 | 13,075 | 0.40 |
| **Cannon Street** | City of London | 18,732 | 7,477 | 0.40 |
| **Mansion House** | City of London | 11,584 | 4,812 | 0.42 |
| **Bank & Monument** | City of London | 112,547 | 47,320 | 0.42 |
| **Cannon Street** | City of London | 17,881 | 8,058 | 0.45 |


<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/b8433dc3-6a89-40ca-983e-124e7634378f" />

*Insight: Hampir seluruh stasiun komuter terpadat berlokasi di distrik finansial dan perkantoran utama (City of London dan sekitarnya). Volume penumpang anjlok hingga 80% pada hari Sabtu dan Minggu.*


### 📊 Top 10 Stasiun Dominan Rekreasi (Akhir Pekan Tinggi)

Analisis ini mengklasifikasikan stasiun berdasarkan rasio penumpang akhir pekan dibandingkan hari kerja. Berkebalikan dengan tren komuter, terdapat kelompok stasiun minoritas yang justru menampung beban tertingginya saat mayoritas stasiun lain sedang sepi (Rasio > 1.0).

* **Rasio > 1.0**: Stasiun didominasi aktivitas akhir pekan (Karakteristik Rekreasi/Turis/Transit Khusus).
* **Rasio < 0.5**: Stasiun didominasi aktivitas hari kerja (Karakteristik Komuter/Perkantoran).

<img width="1389" height="690" alt="image" src="https://github.com/user-attachments/assets/dc9aca12-cb1b-4eae-9925-75d123b9f3ce" />

#### 🌳 Top 10 Stasiun Dominan Rekreasi (Trafik Akhir Pekan Tinggi)

| Station | Borough | Total Hari Kerja | Total Akhir Pekan | Rasio Rekreasi |
| :--- | :--- | :--- | :--- | :--- |
| **Kensington (Olympia)** | Kensington and Chelsea | 1,645 | 11,337 | 6.89 |
| **Kensington (Olympia)** | Kensington and Chelsea | 1,640 | 11,122 | 6.78 |
| **Mornington Crescent** | Camden | 7,736 | 18,603 | 2.40 |
| **Heathrow Terminal 4** | Hillingdon | 3,200 | 7,566 | 2.36 |
| **Leicester Square** | City of Westminster | 51,298 | 118,996 | 2.32 |
| **Leicester Square** | City of Westminster | 49,948 | 113,019 | 2.26 |
| **Heathrow Terminals 123**| Hillingdon | 11,046 | 24,635 | 2.23 |
| **Heathrow Terminals 123**| Hillingdon | 11,347 | 24,886 | 2.19 |
| **Heathrow Terminal 5** | Hillingdon | 6,482 | 14,163 | 2.18 |
| **Heathrow Terminal 4** | Hillingdon | 3,253 | 6,913 | 2.13 |

*Insight: Stasiun Kensington (Olympia) memiliki anomali rasio tertinggi (hampir 7x lipat di akhir pekan), yang sejalan dengan fungsinya sebagai pusat ekshibisi. Dominasi stasiun Heathrow juga menunjukkan karakteristik penumpang pesawat/turis.*



**Insight Analitik:**
Kensington (Olympia) menampilkan anomali rasio tertinggi (hampir 7x lipat lebih padat di akhir pekan), yang sangat selaras dengan fungsinya sebagai pusat pameran dan acara. Selain itu, kehadiran stasiun-stasiun Heathrow di daftar ini menunjukkan karakteristik lalu lintas turis dan pelancong udara yang jadwalnya tidak terikat pada hari kerja standar.
