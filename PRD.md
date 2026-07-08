# Product Requirements Document (PRD)
## Nama Projek: Kubus Matematik Ajaib 3D (Tahun 1) - Versi 2.0

### 1. Pengenalan
Permainan web 3D interaktif yang direka khusus untuk murid Tahun 1 bagi mempraktikkan asas matematik (operasi tambah dan tolak dalam lingkungan 10). Versi 2.0 ini menggabungkan elemen visual 3D yang menarik dengan sistem maklum balas audio sintetik untuk meningkatkan daya tumpuan, kefahaman, dan keterlibatan murid.

### 2. Objektif
* Menyediakan platform pembelajaran interaktif yang menyeronokkan untuk matematik Tahun 1.
* Meningkatkan kecekapan murid dalam operasi tambah dan tolak asas (0 hingga 10).
* Memberikan rangsangan pelbagai deria (visual dan audio) untuk proses peneguhan (reinforcement) pembelajaran.

### 3. Kumpulan Sasaran
* Kanak-kanak berumur 6 hingga 7 tahun (Tahun 1).
* Guru sekolah rendah dan ibu bapa sebagai pemudah cara.

### 4. Ciri-ciri Utama (Core Features)

* **Enjin Grafik 3D (Three.js):** 
  * Memaparkan 3 buah kubus (blok) 3D dengan warna berbeza yang terapung dan berputar.
* **Penjanaan Soalan Rawak (Campuran):** 
  * Sistem akan memilih operasi Tambah (+) atau Tolak (-) secara rawak.
  * *Peraturan Operasi Tambah:* Hasil tambah maksimum ialah 10.
  * *Peraturan Operasi Tolak:* Nombor pertama sentiasa lebih besar atau sama dengan nombor kedua (a ≥ b) untuk mengelakkan jawapan bernilai negatif, selaras dengan silibus Tahun 1.
* **Sistem Pilihan Pelbagai:** 
  * 3 pilihan jawapan dijana secara rawak (1 betul, 2 salah) dan dipaparkan secara langsung pada tekstur permukaan kubus 3D.
* **Maklum Balas Audio (Web Audio API):**
  * *Jawapan Betul:* Bunyi "Ting!" / Loceng (nada tinggi dan ceria).
  * *Jawapan Salah:* Bunyi "Buzzer" (nada rendah).
* **Maklum Balas Visual & Skor:** 
  * *Jawapan Betul:* Skor bertambah 10 mata, mesej pujian berwarna hijau dipaparkan, kubus membesar (scale up), dan soalan baharu dijana selepas sela masa 1 saat.
  * *Jawapan Salah:* Skor ditolak 5 mata (jika skor lebih dari 0), mesej galakan berwarna merah dipaparkan, dan kubus mengecil (scale down).
* **Mekanisme Anti-Spam:**
  * Fungsi klik dinyahaktifkan seketika (1 saat) apabila jawapan betul dipilih bagi mengelakkan pemain menekan kubus berkali-kali dan merosakkan logik penjanaan soalan.

### 5. Keperluan Teknikal (Tech Stack)
* **Frontend:** HTML5, CSS3, JavaScript (ES6).
* **Grafik:** Pustaka Three.js (dihubungkan melalui CDN).
* **Audio:** Web Audio API (Penjanaan bunyi sintetik terbina dalam pelayar, tiada fail MP3 luaran diperlukan).
* **Platform:** Pelayar web moden (Chrome, Safari, Firefox, Edge). Responsif dan menyokong input tetikus (PC) serta skrin sentuh (Tablet/Telefon Pintar).

### 6. Aliran Pengguna (User Flow)
1. Pemain membuka halaman web.
2. Skrin memaparkan skor "0", teks arahan "Klik mana-mana kubus untuk mulakan bunyi!", dan soalan "Bersedia?".
3. Pemain melakukan klik pertama pada skrin untuk membenarkan pengaktifan Web Audio API.
4. Tiga kubus 3D berputar di skrin, masing-masing memaparkan pilihan jawapan. Soalan pertama dijana (contoh: "8 - 3 = ?").
5. Pemain menyentuh/mengklik kubus yang mempunyai jawapan yang betul.
6. Sistem menyemak jawapan dan memainkan kesan bunyi (Ting/Buzzer) serta animasi pembesaran/pengecilan kubus.
7. Selepas jawapan yang betul diberikan, soalan campuran baharu dijana secara automatik.