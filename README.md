
# Bot Daily Report Abhinaya

**Bot Daily Report Abhinaya** adalah bot Telegram yang dirancang untuk mencatat dan mengelola laporan harian. Bot ini menyediakan fitur input data barang keluar dan ekspor laporan dalam format Excel.

## Fitur
- **Input Data Barang Keluar**
  - Pilih sesi waktu (Breakfast, Coffee Time, Lunch, Dinner, Supper).
  - Tentukan nama barang, jumlah (qty), dan lokasi penyimpanan.
  - Data otomatis tersimpan dalam database SQLite.
- **Ekspor Laporan**
  - Ekspor data barang keluar ke file Excel.
  - Format laporan rapi Dan dapat Di baca (centered).
    
## Teknologi yang Digunakan
- **Python 3**
- **Telegram Bot API** (dengan `python-telegram-bot` library)
- **SQLite** (dengan SQLAlchemy untuk ORM)
- **Pandas** (untuk manipulasi data dan ekspor Excel)
- **OpenPyXL** (untuk format file Excel)

## Instalasi

### Prasyarat
1. Python 3.8 atau lebih baru
2. Telegram bot token (buat bot di [BotFather](https://t.me/BotFather))

### Langkah-langkah Instalasi
1. **Clone Repository**
   ```bash
   git clone https://github.com/dendve8/Daily-Report.git
   cd Daily-Report
   ```

2. **Buat Virtual Environment**
   ```bash
   python3 -m venv env
   source env/bin/activate  # Untuk Linux/Mac
   env\Scripts\activate     # Untuk Windows
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Atur Token Bot**
   - Ganti `YOUR_BOT_TOKEN` pada file `main.py` dengan token bot Telegram Anda.

5. **Jalankan Bot**
   ```bash
   python main.py
   ```

## Cara Penggunaan
1. **Memulai Bot**
   - Kirim `/start` ke bot di Telegram untuk melihat menu utama.

2. **Input Data**
   - Klik tombol **📥 Input Data** untuk memulai input barang keluar.
   - Ikuti instruksi bot untuk memilih sesi waktu, nama barang, jumlah, dan lokasi.

3. **Ekspor Laporan**
   - Klik tombol **📤 Export Data** untuk mengekspor laporan ke file Excel.
   - Bot akan mengirimkan file Excel berisi data barang keluar.

## Struktur Database
Database SQLite (`barang_keluar.db`) memiliki tabel `barang_keluar` dengan struktur berikut:
- **id**: ID unik untuk setiap entri.
- **nama_barang**: Nama barang.
- **qty**: Jumlah barang.
- **sesi**: Sesi waktu (Breakfast, Lunch, dll.).
- **lokasi**: Lokasi penyimpanan (MINI-CAMP, BASE-CAMP).
- **time**: Waktu input, termasuk nama hari.

## File Excel
File Excel berisi kolom berikut:
- No
- Nama Barang
- Qty
- Sesi
- Lokasi
- Time (format: `Hari, YYYY-MM-DD HH:MM:SS`)

## Contoh Tampilan
**Input Data:**
- Pilih sesi waktu.
- Masukkan nama barang dan jumlah.
- Pilih lokasi.

**Ekspor Laporan:**
- Klik tombol untuk menghasilkan file Excel.

**Contoh Laporan Excel:**

| No  | Nama Barang | Qty | Sesi      | Lokasi      | Time                       |
| --- | ----------- | --- | --------- | ----------- | -------------------------- |
| 1   | Galon Aqua  | 10  | BREAKFAST | BASECAMP    | Senin, 2024-12-10 08:00:00 |

## Kontribusi
Kontribusi sangat diterima! Jika Anda menemukan bug atau memiliki ide fitur baru:
1. Fork repository ini.
2. Buat branch baru untuk fitur/bug Anda.
3. Lakukan pull request ke branch `main`.

## Lisensi
Proyek ini dilisensikan di bawah lisensi MIT. Lihat [LICENSE](LICENSE) untuk informasi lebih lanjut.

## Kontak
Jika ada pertanyaan atau masukan, silakan hubungi saya melalui [Telegram](https://t.me/dendve8)).

---
![image](https://github.com/user-attachments/assets/b0b39b20-5ea7-4ba7-a5a8-1a83bded147f)

**Selamat menggunakan Bot Daily Report Abhinaya!**
