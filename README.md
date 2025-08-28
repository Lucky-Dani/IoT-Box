IoT-Box Dashboard 
IoT-Box adalah sistem monitoring mesin produksi berbasis IoT yang memanfaatkan ESP32, MQTT, dan Firebase untuk mengawasi kondisi mesin, sensor, serta runtime secara real-time melalui dashboard web interaktif.

Fitur Utama :
- Deteksi Kebakaran dengan flame sensor + indikator LED
- Monitoring Air menggunakan sensor kelembaban / water sensor
- Komunikasi MQTTX
- Integrasi Firebase Realtime Database untuk penyimpanan & sinkronisasi data

📊 Dashboard Web yang menampilkan:
- Status mesin (ON / OFF) dengan runtime otomatis
- Data sensor (api, suhu, gerakan, getaran) real-time
- Riwayat runtime mesin
- Timeout otomatis: mesin dianggap OFF jika tidak ada data sensor dalam periode tertentu

🛠️ Tech stack yang Digunakan :
- Hardware: ESP32-WROOM, Flame Sensor, Water Sensor
- Software / Cloud:
   - Arduino IDE (C++)
   - Paho-MQTT (Python)
   - Firebase Realtime Database
   - MQTTX
   - HTML, CSS, JavaScript (Frontend Dashboard)

📂 Struktur Project
📦 IoT-Box
 ┣ 📜 ESP32-WROOM.ino            # Kode untuk ESP32
 ┣ 📜 connection.py              # MQTT client → push ke Firebase
 ┣ 📜 index.php                  # Dashboard web
 ┣ 📜 style.css                  # Styling dashboard
 ┣ 📜 logo.png                   # logo
 ┗ 📜 README.md                  # Dokumentasi

Cara Menjalankan :
1️⃣ Setup ESP32
- Buka esp32_flame_water.ino di Arduino IDE
- Ganti SSID dan PASS dengan WiFi kamu
- Upload ke ESP32

2️⃣ Setup Python Bridge :
Install dependency : pip install paho-mqtt firebase-admin 
- Jalankan script: connection.py

3️⃣ Dashboard Web :
- Buka index.php di browser
- Dashboard akan otomatis menampilkan data real-time dari Firebase

📸 Tampilan Dashboard
https://github.com/user-attachments/assets/94790bdd-c02b-4e4a-83b4-70d41889932a

Tujuan Project :
Proyek ini dikembangkan untuk mendukung Industry 4.0 dengan menyediakan sistem monitoring mesin otomatis yang real-time, scalable, dan dapat diakses via cloud.
