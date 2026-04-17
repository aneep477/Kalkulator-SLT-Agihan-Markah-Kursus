# 📊 Kalkulator Maklumat Kursus (MK) - Backend Engine

Sistem ini adalah enjin pengiraan belakang (backend) yang dibina menggunakan **Google Apps Script** untuk membantu pemaju kurikulum mengira Jam Pembelajaran Pelajar (SLT) dan agihan markah HPK secara automatik berdasarkan fail MQA Table 4 (XLSX).

## 🚀 Ciri-Ciri Utama
- **Auto-Extract**: Mengekstrak data terus dari fail Excel (.xlsx) Table 4.
- **Pengiraan SLT**: Mengikut formula standard (Kredit × 40 jam).
- **Validasi Pintar**: Menyemak ketepatan agihan jam PdP bagi setiap HPK.
- **Integrasi GitHub**: Kod backend disimpan dan diuruskan melalui GitHub.

## 🛠️ Formula Yang Digunakan
Sistem ini menggunakan logik pengiraan rasmi seperti berikut:
1. **Jumlah SLT Keseluruhan** = Nilai Kredit × 40 jam.
2. **Jumlah Jam SLT PdP (Kuliah)** = Digenapkan daripada `(Total SLT / 17 minggu) × 14 minggu`.
3. **Pemberatan HPK** = `(Jam HPK / Jumlah Jam PdP) × 100`.

## 📖 Panduan Penggunaan

### 1. Penyediaan Awal
1. Buka Google Sheets anda.
2. Pergi ke `Extensions` > `Apps Script`.
3. Pastikan **Drive API** telah diaktifkan di bahagian *Services*.
4. Jalankan fungsi `onOpen` untuk memaparkan menu **⚙️ Sistem MK**.

### 2. Membina Struktur
- Klik menu **⚙️ Sistem MK** > **1. Sediakan Header & Struktur**.
- Sistem akan membina helaian bernama `Kalkulator_SLT` dengan tajuk kolum yang betul.

### 3. Memproses Fail Excel (MK)
- Klik menu **⚙️ Sistem MK** > **2. 📂 Muat Naik & Ekstrak Fail MK**.
- Pilih fail `.xlsx` (Table 4) dari komputer anda.
- Sistem akan mengekstrak Kod Kursus, Kredit, dan Jam PdP secara automatik.

### 4. Semakan Keputusan
- Lihat kolum **Status Validasi**.
- ✅ **TEPAT**: Agihan jam anda memenuhi syarat SLT.
- ❌ **RALAT**: Jumlah jam yang dimasukkan tidak sama dengan pengiraan standard. Sila buat pelarasan pada fail MK anda.

## 💻 Pemasangan Backend (GitHub)
Untuk menghubungkan kod ini dengan GitHub anda:
1. Pasang extension **Google Apps Script GitHub Assistant**.
2. Sambungkan akaun GitHub menggunakan *Personal Access Token*.
3. Tolak (*Push*) kod dari Apps Script ke repositori ini.

---
**Dibangunkan oleh:** [Nama Anda / Unit Akademik]  
**Versi:** 1.0.0
