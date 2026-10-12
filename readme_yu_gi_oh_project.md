# Prediksi Harga Pasar Kartu Yu-Gi-Oh! Menggunakan Machine Learning

Proyek ini adalah tugas praktikum Machine Learning yang bertujuan untuk memprediksi harga pasar kartu Yu-Gi-Oh! (`tcgplayer_price`) berdasarkan spesifikasi fisik kartu monster tersebut.

## Deskripsi Proyek

Dalam permainan Yu-Gi-Oh!, setiap kartu monster memiliki atribut *Level*, *Attack* (ATK), dan *Defense* (DEF). Proyek ini menggunakan algoritma **Regresi** untuk menganalisis apakah ketiga atribut tersebut memiliki pengaruh yang signifikan terhadap harga jual sebuah kartu di pasaran.

## Dataset

Dataset yang digunakan adalah `yugioh_cards.csv` yang berisi ribuan data kartu Yu-Gi-Oh!.
Dalam tahap *preprocessing*, data dibersihkan dengan memfilter khusus **Kartu Monster** saja (membuang kartu *Spell* dan *Trap* yang tidak memiliki ATK/DEF/Level).

* **Fitur (X):** `level`, `atk`, `def`

* **Target (y):** `tcgplayer_price` (Harga dalam Dolar)

## Algoritma & Library

* **Algoritma:** Random Forest Regressor

* **Evaluasi:** Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), dan R-Squared ($R^2$)

* **Library:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

## Tahapan Pemrosesan

1. **Data Loading:** Memuat dataset menggunakan Pandas.

2. **Exploratory Data Analysis (EDA) & Preprocessing:** Membersihkan *missing values* dan melihat distribusi data harga.

3. **Data Splitting:** Membagi data menjadi 80% *Training Set* dan 20% *Testing Set*.

4. **Modeling:** Melatih model regresi menggunakan algoritma Random Forest.

5. **Evaluasi & Visualisasi:** Mengukur tingkat *error* prediksi model, membuat grafik perbandingan harga asli vs tebakan model, serta melihat *Feature Importance*.

## Cara Menjalankan Proyek

1. Clone atau unduh repositori ini ke komputer lokal Anda:

   ```
   git clone https://github.com/deadlysins002-bit/Tugas-Machine-Learning.git
   
   ```

2. Masuk ke direktori proyek:

   ```
   cd Tugas-Machine-Learning
   
   ```

3. Pastikan file dataset `yugioh_cards.csv` berada di direktori yang sama dengan file notebook.

4. Buka Jupyter Notebook atau JupyterLab:

   ```
   jupyter notebook main.ipynb
   
   ```

5. Jalankan sel (*cells*) secara berurutan dari atas ke bawah.