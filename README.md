# 🏆 UCL 2025/26 — AI Champion Predictor v2

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

Proyek analisis data berbasis Python ini menyimulasikan dan memprediksi Juara **UEFA Champions League (UCL) musim 2025/2026**. Menggunakan pemodelan prediktif dan **Simulasi Monte Carlo (15.000 iterasi)**, proyek ini mengkalkulasi probabilitas kemenangan berdasarkan metrik performa terkini dari berbagai liga top Eropa.

---

## 📋 Table of Contents
- [✨ Fitur Utama](#-fitur-utama)
- [🛠 Tech Stack](#-tech-stack)
- [📊 Metodologi Prediksi](#-metodologi-prediksi)
- [📈 Visualisasi Data](#-visualisasi-data)
- [🚀 Instalasi & Penggunaan](#-instalasi--penggunaan)
- [📁 Struktur File](#-struktur-file)

---

## ✨ Fitur Utama
* **🔥 Analisis Form Dinamis:** Menghitung *Weighted Form Rating* (skala 0-10) dari 7 laga terakhir, di mana pertandingan terbaru memiliki bobot lebih tinggi untuk akurasi tren terkini.
* **🤖 Enhanced Prediction Model:** Algoritma probabilitas yang mengintegrasikan:
    * *Form Rating* & Selisih Gol.
    * Kedalaman Skuad & Kualitas Pelatih.
    * Pengalaman Historis di UCL.
    * Status Cedera Pemain Kunci.
* **🎲 Monte Carlo Simulation:** Menjalankan 15.000 simulasi turnamen acak dari Babak 16 Besar hingga Final untuk menghasilkan persentase peluang juara yang stabil secara statistik.
* **📊 Dashboard Visualisasi:** *Heatmap* performa tim dan *dashboard* prediksi komprehensif menggunakan Matplotlib.
* **❤️ Mode Jagoan v2:** Fitur *deep-dive* statistik untuk menganalisis status tim favorit (misal: Arsenal) apakah mereka masuk kategori *Front-runner*, *Dark Horse*, atau *Underdog*.

---

## 🛠 Tech Stack
Proyek ini memanfaatkan ekosistem *data science* Python:
* **Bahasa:** Python 3.10+
* **Manipulasi Data:** Pandas, NumPy
* **Visualisasi:** Matplotlib, Seaborn
* **Preprocessing:** Scikit-learn (`MinMaxScaler`)
* **Environment:** Jupyter Notebook / Google Colab

---

## 📊 Metodologi Prediksi
Model ini menggunakan normalisasi data untuk memastikan perbandingan antar liga (Premier League vs Bundesliga, dll) tetap adil. Formula probabilitas dihitung menggunakan:

$$P(win) = \frac{\sum (Form \times w_1) + (Squad \times w_2) + (Exp \times w_3)}{\text{Total Weight}}$$

---

## 📈 Visualisasi Data
> *Catatan: Pastikan gambar output telah di-generate dan tersimpan di folder root.*

### 1. Heatmap Form 7 Pertandingan Terakhir
Visualisasi intensitas performa tim berdasarkan hasil pertandingan domestik terbaru.
![Heatmap Form](ucl_form_heatmap.png)

### 2. Dashboard Prediksi Lengkap
Ringkasan probabilitas juara berdasarkan hasil simulasi 15.000 iterasi.
![Dashboard Prediksi](ucl_dashboard_v2.png)

---

## 🚀 Instalasi & Penggunaan

1.  **Clone Repositori:**
    ```bash
    git clone [https://github.com/username-kamu/ucl-2026-predictor.git](https://github.com/username-kamu/ucl-2026-predictor.git)
    cd ucl-2026-predictor
    ```

2.  **Instal Library:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```

3.  **Jalankan Notebook:**
    Buka `UCL_2026_Predictor_v2.ipynb` di Jupyter atau Google Colab dan jalankan semua cell.

4.  **Kustomisasi Tim Favorit:**
    Ubah variabel `MY_TEAM` di bagian "Mode Jagoan v2":
    ```python
    MY_TEAM = 'Arsenal'  # Masukkan nama tim pilihanmu
    ```

---

## 📁 Struktur File
```plaintext
📦 ucl-2026-predictor
 ┣ 📜 UCL_2026_Predictor_v2.ipynb  # Notebook Utama
 ┣ 📜 ucl_2026_detailed.csv        # Dataset Input (Cut-off: 27 Feb 2026)
 ┣ 📜 ucl_2026_results_v2.csv      # Output Kalkulasi Probabilitas
 ┣ 📜 ucl_form_heatmap.png         # Asset Visualisasi Heatmap
 ┣ 📜 ucl_dashboard_v2.png         # Asset Visualisasi Dashboard
 ┗ 📜 README.md                    # Dokumentasi

Sumber Data: Statistik diolah dari UEFA.com dan data liga domestik (Premier League, La Liga, dsb).
Dibuat untuk keperluan eksperimen simulasi data dan visualisasi probabilitas. 🏆
