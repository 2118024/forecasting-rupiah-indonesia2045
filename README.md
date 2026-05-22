# 📉 Indonesia Emas 2045 vs Indonesia Cemas: Analisis Prediktif & Proyeksi Titik Balik Nilai Tukar Rupiah (USD/IDR)

Proyek analisis data dan *machine learning* ini dibangun untuk membedah diskursus publik mengenai optimisme target **"Indonesia Emas 2045"** dan tantangan realita ekonomi **"Indonesia Cemas"** secara empiris. Riset difokuskan pada volatilitas nilai tukar Rupiah terhadap Dolar AS (USD/IDR) menggunakan pendekatan statistik multivariat dan permodelan *time-series forecasting*.

---

## 🛠️ Alur Metodologi & Fitur Data
Proyek ini mengintegrasikan data deret waktu (*time-series*) harian berskala makroekonomi selama 10 tahun terakhir dengan memanfaatkan integrasi API langsung ke sumber data publik tanpa unduhan manual:
1. **Target Variable (Y):** Kurs harian USD/IDR via API `yfinance` (Yahoo Finance).
2. **Predictor Features (X):** - **Indeks Dolar AS (DXY):** Mengukur kekuatan relatif USD di pasar global (Sumber: FRED St. Louis Fed).
   - **Suku Bunga Efektif AS (Fed Funds Rate):** Mengukur arah kebijakan moneter Amerika Serikat (Sumber: FRED St. Louis Fed).
   - **BI-Rate:** Sebagai jangkar intervensi kebijakan moneter domestik dari Bank Indonesia.

---

## 📈 Rekapitulasi Hasil Analisis (Key Insights)

* **Analisis Korelasi Multivariat (Seaborn Heatmap):** Berdasarkan matriks korelasi Pearson, ditemukan korelasi positif yang sangat kuat (+0.80 ke atas) antara variabel `Kurs_USD_IDR` dengan `Indeks_Dolar_DXY`. Secara statistik, ini membuktikan bahwa faktor tekanan eksternal (*global dollar strengthening*) memegang peranan dominan terhadap pelemahan nilai tukar domestik pada kondisi riil saat ini (Kuartal II-2026).
* **Dekomposisi Pola Musiman (Seasonal Pattern):** Melalui algoritma **Meta Prophet**, model berhasil mengisolasi fluktuasi musiman tahunan. Rupiah secara siklikal mengalami tekanan psikologis terberat di akhir Kuartal II (April–Juni) akibat faktor musiman korporasi (repatriasi dividen ke luar negeri), namun secara historis menunjukkan peluang *rebound* penguatan yang konsisten pada paruh kedua tahun (**Kuartal III & IV**).
* **Proyeksi Titik Balik (Forecasting):** Tren jangka panjang model memproyeksikan nilai tukar USD/IDR akan memasuki fase stabilisasi dan berpotensi mulai melandai (Rupiah kembali menguat) seiring dengan proyeksi pelonggaran kebijakan suku bunga global serta bertahannya efektivitas jangkar moneter BI-Rate di level 5.25%.

---

## 💻 Tech Stack & Library Python yang Digunakan
- **Environment:** Jupyter Notebook / Google Colab (`.ipynb`)
- **Data Gathering:** `yfinance`, `pandas_datareader`
- **Data Cleansing & Analytics:** `pandas`, `numpy`
- **Data Visualization:** `matplotlib`, `seaborn`
- **Predictive Modeling:** `prophet` (by Meta)

---

## 🚀 Cara Menjalankan Proyek Ini Secara Lokal

1. Clone repositori ini:
   ```bash
   git clone [https://github.com/USERNAME-KAMU/forecasting-rupiah-indonesia2045.git](https://github.com/USERNAME-KAMU/forecasting-rupiah-indonesia2045.git)
