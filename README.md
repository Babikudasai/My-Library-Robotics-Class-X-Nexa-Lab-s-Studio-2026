# 🤖 My Library Robotics - Class X
### 🏢 Nexa Lab's Studio © 2026

[![Platform: ESP32](https://shields.io)](https://espressif.com)
[![Framework: Arduino](https://shields.io)](https://arduino.cc)
[![Lab Status: Active](https://shields.io)]()

Selamat datang di repositori perpustakaan kode, skema, dan dokumentasi resmi untuk siswa **Kelas X Kurikulum Robotika & IoT**. Repositori ini dirancang sebagai pustaka modular untuk mempermudah pembelajaran arsitektur mikrokontroler, pengendali motor, dan integrasi berbagai sensor cerdas.

---

## 🗺️ Peta Navigasi Repositori (Klik untuk Membuka)

Silakan klik tautan di bawah ini untuk langsung menuju dokumentasi teknis dan contoh kode program spesifik:

### 🧠 1. Modul Mikrokontroler (Controllers)
Bagian utama yang berfungsi sebagai otak atau unit pemroses robot:
*   [**ESP32 Classic (DevKit v1)**](./controllers/esp32-classic/) — Panduan dasar GPIO, Wi-Fi, dan instalasi driver CP210x.
*   [**ESP32-C3 (RISC-V)**](./controllers/esp32-c3/) — Dokumentasi arsitektur core tunggal RISC-V dan limitasi pin.
*   [**ESP32-S3 (AI Dual-Core)**](./controllers/esp32-s3/) — Konfigurasi tingkat lanjut untuk akselerasi vektor dan USB-OTG.

### ⚙️ 2. Sistem Penggerak (Drivers Motor)
Modul antarmuka aktuator daya untuk mengendalikan pergerakan motor:
*   [**TB6612FNG (MOSFET)**](./drivers-motor/tb6612fng/) — Driver motor hemat daya efisiensi tinggi, *truth table*, dan pin STBY.
*   [**L298N (H-Bridge BJT)**](./drivers-motor/l298n/) — Analisis driver klasik, masalah disipasi panas, dan drop tegangan.
*   [**DRV8825 (Stepper Driver)**](./drivers-motor/drv8825/) — Panduan motor stepper presisi derajat dan kalibrasi Vref.

### 📡 3. Sistem Indra (Sensors)
Modul input untuk membaca kondisi lingkungan fisik di sekitar robot:
*   [**Ultrasonic HC-SR04**](./sensors/ultrasonic-hcsr04/) — Rumus konversi durasi pulsa suara menjadi satuan centimeter.
*   [**IMU MPU6050**](./sensors/imu-mpu6050/) — Pembacaan data Gyroscope & Accelerometer lewat bus I2C.
*   [**IR Line Follower**](./sensors/ir-line-follower/) — Teknik kalibrasi sensitivitas sensor pembaca garis lintasan.

### 🚀 4. Proyek Integrasi Praktikum (Projects)
Kumpulan cetak biru proyek utuh hasil gabungan pengontrol, driver, dan sensor:
*   [**Nexa Line Follower Robot**](./projects/nexa-line-follower/) — Robot pelacak garis menggunakan algoritma kontrol arah.
*   [**Nexa Obstacle Avoidance Bot**](./projects/nexa-obstacle-bot/) — Robot otonom penghindar rintangan berbasis ultrasonik.

---

## 📋 Panduan Awal Menggunakan Repositori

1.  **Gunakan `.gitignore`:** Pastikan file `.gitignore` di root sudah aktif agar folder `.pio/` atau `.build/` dari komputer Anda tidak ikut terunggah saat melakukan *push*.
2.  **Aturan Kontribusi:** Bagi siswa Kelas X, sebelum mengunggah kode proyek baru ke folder `projects/`, silakan baca terlebih dahulu [Panduan Kontribusi Lab](./.github/PANDUAN_KONTRIBUSI.md).
3.  **Level Tegangan:** Selalu perhatikan bahwa keluarga ESP32 bekerja pada tegangan logika **3.3V**. Jangan menghubungkan sensor beroutput 5V langsung tanpa pembagi tegangan (*voltage divider*)!

---
*Diproduksi oleh **Nexa Lab's Studio 2026**. Hak Cipta Dilindungi Undang-Undang.*
