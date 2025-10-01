# 📘 README – Guided Deep Learning Notebook

## 📌 Deskripsi
Notebook **`GUIDED_DL_2_12298.ipynb`** berisi latihan pembelajaran mendalam (Deep Learning) menggunakan **TensorFlow/Keras**. Proyek ini dirancang sebagai **guided project** untuk memahami:
- Preprocessing data teks (lagu/lirik berbasis notasi ABC atau teks lain).
- Pembuatan kamus karakter (`char2idx`, `idx2char`).
- Pembangunan model Recurrent Neural Network (RNN).
- Pelatihan model untuk memprediksi token/karakter berikutnya.
- Evaluasi loss dan generasi teks/lagu baru.

---

## 🛠️ Persyaratan
Sebelum menjalankan notebook, pastikan environment Python sudah terpasang library berikut:

```txt
tensorflow
numpy
matplotlib
```

Jika ingin menambahkan dependensi lain (misalnya `tqdm`, `music21`, atau modul tambahan dari `magenta`/`tensorflow_datasets`), bisa sesuaikan sesuai error saat run.

Instalasi cepat:

```bash
pip install tensorflow numpy matplotlib
```

---

## 🚀 Cara Menjalankan
1. Clone / simpan repository / file notebook with ssh.
   ```bash
   git clone git@github.com:Yntzie/Guided-Deep-Learning-With-Ternsorflow-Keras.git
   ```
2. Buka notebook:
   ```bash
   jupyter notebook GUIDED_DL_2_12298.ipynb
   ```
3. Jalankan cell secara berurutan:
   - **Load Dataset:** Ganti variabel `songs` dengan dataset teks/lagu kamu.
   - **Preprocessing:** Jalankan cell untuk membuat `vocab`, `char2idx`, dan `idx2char`.
   - **Build Model:** Menyusun arsitektur RNN/GRU/LSTM.
   - **Training:** Lakukan pelatihan dan simpan model.
   - **Generate Text:** Coba hasil prediksi model untuk membuat lagu/teks baru.

---

## ✍️ Cara Mengganti Dataset Lagu
Jika ingin menggunakan lagu/lirik baru:
1. Siapkan file teks berisi lirik atau notasi ABC.
2. Ganti bagian kode:
   ```python
   with open("lagu_baru.txt", "r", encoding="utf-8") as f:
       text = f.read()
   songs = [text]
   ```
3. Jalankan ulang preprocessing → training → generate.

> ⚠️ Jika bukan notasi ABC, bagian **playback audio** akan error. Abaikan cell yang memanggil `play_song`.

---

## 📊 Output
- **Training Loss:** menunjukkan seberapa baik model belajar.
- **Generated Text:** model akan menulis teks/lagu baru berdasarkan pola dataset.
- (Opsional) **Audio Playback:** jika dataset berupa notasi musik ABC.

---

## 👨‍🎓 Catatan
Notebook ini cocok sebagai bahan pembelajaran:
- Dasar pemodelan sequence (RNN).
- Cara kerja embedding dan one-hot vector.
- Training sederhana dengan dataset teks.
