# Kubus Matematik Ajaib 3D (Tahun 1) - Versi 2.0

**Kubus Matematik Ajaib 3D** adalah sebuah permainan web 3D interaktif yang direka khas untuk membantu murid-murid Tahun 1 mempraktikkan asas matematik, khususnya operasi tambah dan tolak dalam lingkungan 10. Permainan ini menggabungkan grafik 3D menggunakan Three.js dan sistem maklum balas audio sintetik menggunakan Web Audio API bagi mewujudkan pengalaman pembelajaran yang menyeronokkan dan berkesan.

---

## 🚀 Ciri-ciri Utama

* **Enjin Grafik 3D (Three.js):** Memaparkan tiga buah kubus 3D berwarna-warni yang terapung dan berputar secara dinamik pada skrin.
* **Penjanaan Soalan Rawak & Pintar:**
  * Soalan dijana secara rawak merangkumi operasi Tambah (+) dan Tolak (-).
  * **Tambah:** Hasil tambah maksimum dihadkan kepada 10.
  * **Tolak:** Sistem memastikan nombor pertama sentiasa lebih besar atau sama dengan nombor kedua ($a \ge b$) bagi mengelakkan hasil negatif, selaras dengan silibus matematik Tahun 1.
* **Sistem Pilihan Jawapan 3D:** Jawapan dipaparkan secara langsung pada tekstur permukaan kubus 3D (1 jawapan betul dan 2 jawapan salah).
* **Maklum Balas Audio Dinamik (Web Audio API):** Bunyi dihasilkan secara sintetik oleh pelayar tanpa memerlukan fail audio luaran:
  * **Betul:** Bunyi loceng/"Ting!" yang ceria dan bernada tinggi.
  * **Salah:** Bunyi *buzzer* bernada rendah.
* **Sistem Skor & Animasi Visual:**
  * **Betul:** +10 mata, mesej pujian berwarna hijau, kubus membesar (*scale up*), dan soalan baru dijana selepas 1 saat.
  * **Salah:** -5 mata (jika skor melebihi 0), mesej galakan berwarna merah, dan kubus mengecil (*scale down*).
* **Mekanisme Anti-Spam:** Klik pada kubus dinyahaktifkan seketika selama 1 saat selepas jawapan yang betul dipilih bagi mengelakkan isu logik klik bertindih.

---

## 🛠️ Keperluan Teknikal

* **Bahasa & Struktur:** HTML5, CSS3, JavaScript (ES6).
* **Pustaka Grafik:** [Three.js](https://threejs.org/) (dihubungkan melalui CDN).
* **Pustaka Audio:** Web Audio API (Terbina dalam pelayar).
* **Keserasian:** Responsif sepenuhnya pada pelayar web moden (Chrome, Safari, Firefox, Edge). Menyokong input tetikus (PC) dan skrin sentuh (Tablet/Telefon Pintar).

---

## 🎮 Cara Bermain / Aliran Pengguna

1. **Mulakan Permainan:** Buka permainan pada pelayar web. Skrin akan memaparkan skor `0` dan arahan: *"Klik mana-mana kubus untuk mulakan bunyi!"*.
2. **Aktifkan Audio:** Klik pertama pada skrin diperlukan untuk mengaktifkan fungsi audio Web Audio API mengikut polisi keselamatan pelayar moden.
3. **Selesaikan Soalan:** Tiga kubus akan berputar dan memaparkan pilihan jawapan untuk soalan matematik yang ditunjukkan (cth: `8 - 3 = ?`).
4. **Pilih Jawapan:** Klik atau sentuh kubus dengan jawapan yang betul.
5. **Teruskan Belajar:** Dapatkan maklum balas visual serta audio segera dan skor akan dikemas kini sebelum soalan seterusnya dijana secara automatik.

---

## 📂 Struktur Projek

* [PRD.md](file:///c:/Users/Demo%20Unit/Downloads/Github/game/mathgame/PRD.md) - Dokumen Keperluan Produk (Product Requirements Document).
* [README.md](file:///c:/Users/Demo%20Unit/Downloads/Github/game/mathgame/README.md) - Dokumen penerangan projek ini.

---

## 🧑‍💻 Pembangunan & Cara Menjalankan Projek

1. Klon repositori ini ke komputer anda:
   ```bash
   git clone https://github.com/hairuln694/mathgame.git
   ```
2. Buka folder projek:
   ```bash
   cd mathgame
   ```
3. Buka fail `index.html` terus di mana-mana pelayar web moden pilihan anda.
