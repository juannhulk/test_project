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

Analisis ini mengklasifikasikan stasiun berdasarkan rasio penumpang akhir pekan dibandingkan hari kerja. 
* **Rasio > 1.0**: Stasiun didominasi aktivitas akhir pekan (Karakteristik Rekreasi/Turis/Transit Khusus).
* **Rasio < 0.5**: Stasiun didominasi aktivitas hari kerja (Karakteristik Komuter/Perkantoran).


### 🚇 Top 10 Stasiun Komuter (Volume Hari Kerja Tertinggi & Rasio Akhir Pekan Rendah)

| Station | Borough | Total Hari Kerja | Total Akhir Pekan | Rasio Rekreasi |
| :--- | :--- | :--- | :--- | :--- |
| **Bank & Monument** | City of London | 230,187 | 101,544 | 0.44 |
| **Moorgate** | City of London | 95,106 | 20,447 | 0.21 |
| **Farringdon** | Islington | 68,265 | 23,123 | 0.34 |
| **Chancery Lane** | City of London | 64,007 | 25,212 | 0.39 |
| **St. James's Park** | City of Westminster | 52,605 | 27,432 | 0.52 |
| **Cannon Street** | City of London | 36,613 | 15,535 | 0.42 |
| **Aldgate** | City of London | 29,292 | 14,818 | 0.51 |
| **Mansion House** | City of London | 22,880 | 9,928 | 0.43 |
| **Upminster Bridge** | Havering | 4,177 | 2,209 | 0.53 |
| **Chigwell** | Epping Forest | 2,116 | 1,116 | 0.53 |

<img width="1389" height="690" alt="image" src="https://github.com/user-attachments/assets/9a812a65-477d-4c37-ae6e-a3112b31bbec" />


---

### 🎡 Top 10 Stasiun Rekreasi (Rasio Lonjakan Akhir Pekan Tertinggi)

| Station | Borough | Total Hari Kerja | Total Akhir Pekan | Rasio Rekreasi |
| :--- | :--- | :--- | :--- | :--- |
| **Kensington (Olympia)** | Kensington and Chelsea | 3,285 | 22,459 | 6.84 |
| **Leicester Square** | City of Westminster | 101,246 | 232,015 | 2.29 |
| **Heathrow Terminal 4** | Hillingdon | 6,453 | 14,479 | 2.24 |
| **Mornington Crescent** | Camden | 15,604 | 34,953 | 2.24 |
| **Heathrow Terminals 123**| Hillingdon | 22,393 | 49,521 | 2.21 |
| **Heathrow Terminal 5** | Hillingdon | 13,141 | 28,289 | 2.15 |
| **Covent Garden** | City of Westminster | 44,654 | 91,217 | 2.04 |
| **Knightsbridge** | Kensington and Chelsea | 52,451 | 102,603 | 1.96 |
| **Hyde Park Corner** | City of Westminster | 16,206 | 31,324 | 1.93 |
| **Piccadilly Circus** | City of Westminster | 116,891 | 225,334 | 1.93 |

<img width="1389" height="690" alt="image" src="https://github.com/user-attachments/assets/5d113241-3c06-45c4-8149-8c40b3dae3e7" />

### Mobilitas penumpang London Tube tidak terdistribusi secara merata secara geografis, melainkan sangat terpusat pada distrik komersial dan wisata utama.
## City of Westminster menanggung beban mobilitas tahunan tertinggi. Situasi ini mengindikasikan perlunya prioritas alokasi dana pemeliharaan pada wilayah-wilayah "timpang" tersebut.
## Mobilitas Internasional: Kehadiran stasiun-stasiun Heathrow Terminal dalam daftar ini membuktikan bahwa titik transit bandara memiliki beban lalu lintas yang stabil di akhir pekan, terlepas dari siklus Senin-Jumat standar.
