# ⚔️ Thousand Years Battle

**Thousand Years Battle** adalah game aksi *survival roguelike* 2D (Bullet Heaven) berbasis web yang dibangun menggunakan Vanilla JavaScript dan HTML5 Canvas. Bertahanlah dari gelombang musuh yang tak ada habisnya, kumpulkan *Exp*, kembangkan senjata, dan picu kombo rahasia yang mematikan!

---

## 🚀 Fitur Utama

* **Sistem Bullet Heaven DInamis:** Hadapi ratusan musuh yang kekuatannya berskala seiring berjalannya waktu.
* **Meta Progression (Toko Upgrade):** Kumpulkan Koin dan *Cosmic Coins* selama bertempur untuk membeli peningkatan stat permanen, membuka senjata baru, serta mengoleksi artefak kuno.
* **20+ Senjata & Kemampuan Efek:** Mulai dari Pistol konvensional, botol racun, hingga hujan meteor, *Frost Nova*, dan menara tesla.
* **Sistem Artefak Unik:** Modifikasi gaya bermainmu dengan artefak khusus seperti *Phoenix Feather* (hidup kembali) atau *Philosopher Stone* (pengganda koin).
* **Mekanisme Sinergi Rahasia (Gojo Mode):** Gabungkan teknik *Blue Lapse* dan *Reversal Red* untuk memicu ledakan **Hollow Purple Nuke** yang menghancurkan seluruh musuh di layar!

---

## 🎮 Cara Bermain

Game ini sepenuhnya berjalan di peramban (browser) tanpa perlu instalasi tambahan.

### Kontrol Karakter

* **Bergerak:** Gunakan tombol `W` `A` `S` `D` atau **Tombol Panah** pada papan ketik.
* **Dash Kiri (Red Flame):** **Klik Kiri Mouse** (Memicu proyektil cepat *Reversal Red* berdaya ledak tinggi jika senjatanya sudah terbuka).
* **Dash Kanan (Blue Flame):** **Klik Kanan Mouse** (Memicu pusaran *Blue Lapse* yang menghisap musuh sekitar jika senjatanya sudah terbuka).

> 💡 **Tips Pro:** Aktifkan *Blue Lapse* dan *Reversal Red* secara bersamaan. Jika kedua proyektil tersebut bertabrakan, kamu akan memicu **Hollow Purple Nuke** masif dengan radius hancur 365+ unit!

---

## 🗺️ Panduan Sinergi & Upgrade

### Mata Uang Game

1. 🪙 **Koin Emas:** Digunakan untuk meningkatkan Statistik Utama (HP, ATK, Speed, Magnet) dan membeli Artefak Unik di Toko.
2. 🔮 **Cosmic Coins:** Digunakan untuk membuka dan meningkatkan Level Mulai (*Starting Level*) senjata baru secara permanen.

### Statistik Utama yang Bisa Ditingkatkan (Max Level 25):

* **Max HP Up:** Menambah kapasitas nyawa tempur karakter.
* **All Weapon Damage:** Meningkatkan persentase kerusakan dari semua jenis senjata.
* **Movement Speed:** Membuat pergerakan karakter lebih lincah menghindari kepungan.
* **Magnet Range:** Memperluas radius penarikan otomatis untuk *Exp* dan koin yang jatuh di tanah.

---

## 🛠️ Spesifikasi Teknologi

Game ini dirancang agar sangat ringan dan memiliki performa tinggi tanpa dependensi eksternal (*Zero Dependencies*).

* **Frontend:** HTML5 & CSS3 (Menggunakan font *Plus Jakarta Sans*).
* **Game Engine:** Vanilla JavaScript dengan API `requestAnimationFrame` untuk *rendering* 60 FPS yang mulus.
* **Grafis:** Logika rendering berbasis vektor langsung pada elemen `<canvas>`.
* **Penyimpanan Data:** Menggunakan `localStorage` otomatis untuk menyimpan progres koin, senjata, dan artefak yang sudah kamu beli.

---

## 📦 Cara Menjalankan Proyek

1. Salin seluruh kode yang kamu miliki ke dalam sebuah file baru bernama `index.html`.
2. Klik dua kali (*double click*) pada file `index.html` tersebut untuk membukanya di browser modern pilihanmu (Chrome, Edge, Firefox, atau Safari).
3. Selamat bermain dan bertahanlah selama mungkin!
