# Ant Colony Optimization (Rute Terpendek Antar Ibu Kota Provinsi di Pulau Jawa)

Repositori ini berisi proyek akhir mata kuliah **Manajemen Sains / Riset Operasi** yang menerapkan metode **Ant Colony Optimization (ACO)** untuk mencari rute terpendek antar ibu kota provinsi di Pulau Jawa. Metode ini mengadaptasi perilaku koloni semut dalam menemukan jalur tercepat menuju sumber makanan melalui mekanisme jejak feromon.

## 🎯 Tujuan Proyek
Menentukan rute perjalanan paling efisien dengan total jarak minimum yang mengunjungi seluruh ibu kota provinsi di Pulau Jawa.

## 🗺️ Wilayah yang dianalisis
Provinsi yang menjadi node pada peta:

| Kode | Ibu Kota     | Provinsi                |
|------|--------------|------------------------|
| 0    | Serang       | Banten                 |
| 1    | Jakarta      | DKI Jakarta            |
| 2    | Bandung      | Jawa Barat             |
| 3    | Semarang     | Jawa Tengah            |
| 4    | Yogyakarta   | DI Yogyakarta          |
| 5    | Surabaya     | Jawa Timur             |

## 🧠 Metode: Ant Colony Optimization
Konsep inti yang digunakan:

- Reprensentasi kota dalam bentuk **graf berarah berbobot** (matriks jarak)
- Semut membentuk kandidat solusi (rute perjalanan)
- Pembaruan **pheromone trail** untuk memperkuat rute yang lebih baik
- Parameter utama:
  - `n_ants` : jumlah semut
  - `n_best` : jumlah rute terbaik yang memperbarui feromon
  - `alpha`  : pengaruh pheromone
  - `beta`   : pengaruh jarak (heuristik)
  - `decay`  : tingkat penguapan pheromone
  - `n_iterations` : jumlah iterasi optimasi

## 🧩 Struktur Notebook
Notebook memuat:

1. Import library yang diperlukan
2. Definisi kelas **AntColonyOptimizer**
3. Matriks jarak antar kota di Pulau Jawa
4. Proses eksekusi algoritma ACO
5. Visualisasi rute terbaik dan jaraknya
