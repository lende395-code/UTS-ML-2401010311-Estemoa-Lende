# UTS Machine Learning: Prediksi Produksi Padi per Provinsi (Jalur B, Regresi)

## Identitas
- **NIM:** 2401010311
- **Nama:** Estemoa Lende
- **Kelas:** XX
- **Random state (SEED):** 311 

## Ringkasan proyek
Proyek ini memperkirakan produksi padi (ton) per provinsi dan tahun dari luas panen dan kondisi iklim (curah hujan, kelembaban, suhu). Alur mengikuti CRISP-DM. Model yang dibandingkan dengan 5-fold cross-validation pada data latih: `DummyRegressor` (baseline), regresi linear sederhana (1 fitur paling berkorelasi), dan regresi linear berganda. Satu model tambahan (berganda + one-hot provinsi) dipakai untuk menguji keputusan encoding.

## Sumber data dan lisensi
- **Dataset:** Data_Tanaman_Padi_Indonesia_2018-2023
- **Penulis:** Erlin, E. (2024). IEEE DataPort. https://dx.doi.org/10.21227/xqkt-z292
- **Tautan:** https://ieee-dataport.org/documents/datatanamanpadiindonesia2018-2023
- **Sumber asli:** BPS (luas panen dan produksi) dan BMKG (curah hujan, kelembaban, suhu), sebagaimana tertulis di halaman dataset.
- **Lisensi:** CC BY 4.0
- **Tanggal akses:** 24 November 2026
- **Ukuran:** 204 baris (34 provinsi x 6 tahun), 7 kolom
- **Catatan:** data Desember 2023 merupakan estimasi prediktif lembaga sumber, bukan data final.
- **Data pribadi:** tidak ada. Data berupa agregat provinsi-tahun, sehingga anonimisasi menurut UU No. 27 Tahun 2022 tidak diperlukan.

## Struktur repository
```
UTS-ML-2401010311-Estemoa Lende/
├── README.md
├── notebook/UTS_ML_2401010311_Estemoa Lende.ipynb
├── data/Data_Tanaman_Padi_Indonesia_2018-2023_Erlin_New.csv
```

## Cara menjalankan
1. Buka notebook di Google Colab.
2. Jalankan **Runtime -> Run all**. 
3. Seluruh output (grafik dan tabel) tampil di notebook.

## Pernyataan Penggunaan AI
- **Alat yang dipakai:** Claude (Anthropic).
- **Untuk bagian apa:** memeriksa kesesuaian dataset dengan ketentuan UTS, menyusun kerangka notebook enam tahap CRISP-DM, menulis draf kode (pembacaan data, grafik, pipeline, cross-validation, evaluasi) dan draf teks "Keputusan saya", serta draf README ini.
- **Bagaimana hasilnya saya periksa:** saya menjalankan seluruh sel di Google Colab (Run all) dan memastikan tidak ada error, membaca setiap bagian kode sampai saya dapat menjelaskan dan mengubahnya (misalnya mengganti jumlah fold atau menambah metrik), mencocokkan setiap kalimat interpretasi dengan grafik dan angka yang benar-benar keluar, serta memeriksa jumlah baris, jumlah fitur, dan nilai yang hilang secara langsung pada berkas CSV yang saya unduh.

## Keterbatasan singkat
Satu provinsi muncul enam kali sehingga baris tidak sepenuhnya independen (skor CV dapat terlalu optimis); kelembaban dan suhu hanya bilangan bulat; data Desember 2023 adalah estimasi. Rincian lengkap ada di Tahap 6 notebook.
