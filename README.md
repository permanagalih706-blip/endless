# 🌌 Thousand Years Battle

**Thousand Years Battle** adalah sebuah game *action roguelite survival* berbasis web (HTML5 Canvas) yang terinspirasi dari mekanik populer genre *bullet heaven / vampire survivors*. Pemain dituntut untuk bertahan hidup dari gempuran ribuan musuh yang kekuatannya terus meningkat seiring berjalannya waktu, mengumpulkan koin serta material kosmikal, dan berevolusi menjadi petarung tak terkalahkan.

---

## 🔥 Apa yang Baru di Update 2.0?

### **Added (Fitur Baru)**
* **One-Time Code System**: Kolom penukaran kode baru di pojok kiri atas menu utama lengkap dengan efek visual dan popup hadiah yang interaktif.
* **Redeemable Reward Codes**:
  * `STARTER PACK`: Mendapatkan bonus instan +1000 Koin dan +100 Cosmic Coin.
  * `EXTRA BULLET`: Pistol dasar mendapatkan tambahan +1 peluru permanen (bisa mencapai hingga 11 peluru sekaligus jika di-upgrade maksimal).
  * `FASTER START`: Memulai permainan langsung di menit ke-1 secara permanen tanpa perlu mengaktifkan cheat skip.
  * `COOL DASH`: Menambahkan efek gelombang dorongan (*knockback area*) kecil untuk mementalkan musuh setiap kali dash berakhir.
* **Exact Time Skip**: Hack `SKIP` kini melompati waktu langsung ke detik spesifik sesuai dengan rekor highscore terakhir Anda, lengkap dengan pre-kalkulasi boss interval dan difficulty scaling yang presisi.

### **Revamped (Peningkatan)**
* **Memory & Performance Optimizations (Low-RAM Friendly)**:
  * Restrukturisasi game loop utama dengan mengubah penyaringan array entitas aktif (`projectiles`, `enemies`, `particles`, `damageTexts`) menjadi sistem **in-place**. Menghilangkan proses alokasi array baru setiap frame sehingga meringankan beban RAM dan CPU secara signifikan (mengurangi *micro-stuttering* akibat Garbage Collection).
  * Batasan jumlah maksimal partikel, proyektil, dan teks damage dikurangi sedikit untuk mencegah overheat pada laptop spek rendah.
  * Pembersihan memori total (`entities` di-reset ke kosong, referensi player dan kamera di-null-kan) dan pengosongan canvas secara bersih saat Anda kembali ke main menu.
* **Game Navigation & State Control**:
  * Pengendalian state game diatur dengan ketat melalui penetapan `gameState = 'menu'` saat di menu utama, mencegah tombol pause (`Escape`) aktif di area menu utama maupun toko.
  * Memperbaiki bug di mana menekan kombinasi tombol `Tab` + `Enter` di toko memicu game berjalan di latar belakang secara tidak sengaja.
* **Hack Speed Values**:
  * Pengali kecepatan dasar untuk cheat `SPEED` ditingkatkan menjadi **3x lipat** (sebelumnya 2x).
  * Efek kombinasi cheat `SPEED` + `BRUTE` disesuaikan menjadi **5x lipat** (sebelumnya 10x).

### **Removed (Dihapus/Diperbaiki)**
* **Memory Leaks**: Menghapus sisa-sisa entitas dan loop aktif di latar belakang saat game dalam kondisi keluar/kembali ke menu utama.
* **Unwanted GC Churn**: Menyingkirkan fungsi `.filter()` konvensional berulang pada update loop utama yang membebani alokasi memori laptop.

---

## 🚀 Fitur Utama

- **Gameplay Tanpa Henti (Endless Survival):** Bertahan sejauh mungkin melawan ratusan musuh sekaligus di layar tanpa adanya *lag* berkat optimasi rendering partikel.
- **Sistem Peningkatan Permanen (Toko Upgrade Evolusi):** Kumpulkan Koin (🪙) dan Kristal Cosmic (🔮) selama pertempuran untuk membuka peningkatan permanen yang terbagi dalam 4 kategori:
  1. 📊 **Statistik Utama:** Upgrade Max HP, Damage, Speed, dan Jangkauan Magnet dasar.
  2. ⚔️ **Permanen Senjata:** Buka senjata baru atau naikkan level awal senjata aktif secara permanen sebelum pertempuran dimulai.
  3. 👑 **Inventaris Artefak:** Pasang artefak magis untuk memicu efek pasif unik seperti perisai (*shield*) atau penggandaan koin.
  4. 🌌 **Toko Ultimate:** Kuasai salah satu dari 9 senjata pamungkas semesta dengan efek visual dan damage luar biasa.
- **Sistem Level-Up Dinamis:** Pilih peningkatan acak setiap kali naik level di tengah pertempuran, lengkap dengan fitur *Reroll* pilihan.
- **Mekanik Tingkat Kesulitan Progresif (Scaling Difficulty):** Darah (*HP*) musuh meningkat sebesar 30% setiap menit. Kemunculan Bos juga memiliki interval dinamis yang akan semakin cepat setiap kali Bos berhasil dikalahkan.

---

## 🎮 Cara Bermain & Kontrol

Jalankan game langsung dengan membuka file `endless.html` di browser modern pilihan Anda.

### Kontrol Karakter
| Tombol | Aksi |
| :--- | :--- |
| <kbd>W</kbd> / <kbd>A</kbd> / <kbd>S</kbd> / <kbd>D</kbd> atau Panah | Menggerakkan Karakter |
| <kbd>Klik kiri</kbd> / <kbd>J</kbd> | Melakukan *Dash* (kiri) (Menghindar Cepat) |
| <kbd>Klik kanan</kbd> / <kbd>K</kbd> | Melakukan *Dash* (kanan) (Menghindar Cepat) |
| <kbd>U</kbd> | Memicu Kemampuan **Ultimate** (Saat indikator penuh) |
| <kbd>Tab</kbd> | Membuka *Hack Terminal* (Cheat) |
| <kbd>ESC</kbd> | Jeda / *Pause* Game |

### Navigasi Pintasan Toko (Menu)
Saat berada di Toko Upgrade Evolusi, Anda dapat menggunakan pintasan keyboard berikut:
- <kbd>1</kbd> : Buka Sub-Toko Statistik Utama
- <kbd>2</kbd> : Buka Sub-Toko Senjata Permanen
- <kbd>3</kbd> : Buka Sub-Toko Inventaris Artefak
- <kbd>4</kbd> : Buka Sub-Toko Ultimate

---

## ⚔️ Daftar Senjata & Kemampuan Unik

Game ini menyediakan berbagai persenjataan unik dengan gaya bertarung yang bervariasi:
- **Boomerang:** Menembakkan senjata tajam menembus musuh hingga ke 8 arah mata angin pada level maksimal.
- **Missile & Meteor:** Serangan berdaya ledak tinggi (AOE) yang mampu melumat gerombolan musuh sekaligus.
- **Chain Lightning & Tesla Coil:** Mengalirkan listrik berantai otomatis yang melompat antar musuh terdekat.
- **Blue Lapse & Reversal Red:** Teknik kutukan spesial jarak dekat dan jauh yang dipicu secara taktis bersamaan dengan manuver *dash*.
- **Singularity (Black Hole):** Menciptakan pusaran gravitasi mini yang menghisap seluruh musuh ke satu titik tengah.

---

## 📦 Komponen Drop Item

Hancurkan musuh dan Bos untuk mendapatkan barang-barang berikut di arena:
- 🔹 **Exp Gems:** Berwarna biru untuk meningkatkan level karakter di tengah permainan.
- 🪙 **Koin Emas:** Digunakan untuk membeli upgrade statistik dasar dan level senjata di menu utama.
- 🔮 **Cosmic Crystals:** Kristal langka yang berfungsi untuk menebus Artefak magis dan Senjata Ultimate.
- 🧲 **Magnet & Super Magnet:** Menarik semua *drop item* yang bertebaran di peta secara instan ke arah pemain.

---

## 🛠️ Teknologi yang Digunakan

- **HTML5 Canvas:** Menggunakan API rendering 2D murni untuk performa grafis berkecepatan tinggi.
- **Vanilla JavaScript (ES6+):** Logika game, manajemen entitas, sistem partikel, kecerdasan buatan musuh (AI pathfinding), dan kalkulasi matematika dihitung secara *native* tanpa pustaka pihak ketiga.
- **CSS Glassmorphism UI:** Antarmuka modern minimalis dengan efek blur latar belakang (`backdrop-filter`) menggunakan tema warna elegan dari palet *Tailwind CSS Slate/Zinc*.
- **Google Fonts:** Menggunakan *font family* `Plus Jakarta Sans` untuk teks HUD yang bersih dan tajam.
- **Web LocalStorage API:** Seluruh progres permainan, skor tertinggi (*highscore*), koin, kristal, serta item yang sudah dibeli tersimpan otomatis di browser pemain.
