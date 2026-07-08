# Thousand Years Battle

Sebuah game **survival-shooter endless** bergaya top-down (mirip Vampire Survivors) yang dimainkan langsung di browser. Bertahanlah selama mungkin, kumpulkan koin, upgrade statistik & senjata, buka artefak unik, kalahkan boss, dan kembangkan karaktermu sekuat mungkin!

## 🎮 Cara Bermain

1. Buka file `endless.html` di browser (tidak perlu instalasi atau server, cukup double click).
2. Dari Menu Utama, kamu bisa:
   - Belanja **Statistik**, **Senjata**, **Artefak**, dan **Senjata Ultimate** menggunakan Koin/Cosmic Koin.
   - Mulai permainan dengan tombol **Start**.
3. Selama bermain, musuh akan terus berdatangan — kumpulkan Koin & Cosmic Koin dari musuh yang dikalahkan untuk di-upgrade nanti di toko.
4. Progres (koin, level senjata/artefak/statistik, highscore) otomatis tersimpan di browser (local storage), jadi bisa dilanjutkan kapan saja.

### Kontrol
| Aksi | Tombol |
|---|---|
| Bergerak | `W` `A` `S` `D` / Arrow Keys |
| Dash (klik kiri) | Klik kiri mouse |
| Dash (klik kanan) | Klik kanan mouse |
| Aktifkan Senjata Ultimate | `U` |
| Jeda permainan | `ESC` |

## 🧩 Fitur Utama

- **Statistik Dasar** — Max HP, Damage semua senjata, Movement Speed, Magnet Range, dan Idle Tycoon (penghasilan pasif walau game ditutup).
- **Puluhan Senjata** — dari Pistol dasar sampai Singularity, Earthquake, Holy Cross, Tornado, dan banyak lagi, masing-masing dengan gaya serangan unik dan jalur upgrade sendiri.
- **Artefak** — item pasif yang memberi bonus permanen seperti Crit Chance, Shield, Lifesteal, Evasion, hingga membuka **Mode Campaign**.
- **Senjata Ultimate** — skill aktif bertenaga besar (tekan `U`) dengan cooldown, mulai dari yang gratis (RAMPAGE) sampai yang paling mahal & mematikan (MaxedOut Weapon).
- **👽 Intergalactic Trader** — pedagang antar-dimensi yang muncul secara acak (peluangnya bisa ditingkatkan lewat artefak Space Trader). Bisa dipakai untuk menukar Koin ↔ Cosmic Koin, dan sesekali membawa **Senjata Mistis** langka untuk dijual.
  - Saat sedang bermain, akan muncul notifikasi kecil di pojok kiri bawah layar saat Trader datang — kamu bisa klik untuk menjeda game & langsung mengeceknya, menutup notifikasi untuk lanjut main tanpa diganggu, atau membiarkannya (namun berisiko kehabisan waktu sebelum sempat mengecek penawarannya).
- **Senjata Mistis** — 5 item paling langka & kuat di game, hanya bisa didapat lewat Intergalactic Trader.
- **Mode Campaign** — mode alternatif berdurasi 20 menit (bukan endless) dengan pembatasan senjata, cocok untuk tantangan yang berbeda.
- **Kode Redeem** — ada sejumlah kode satu-kali pakai yang bisa ditukarkan lewat panel **"Enter Code"** di pojok kiri atas menu utama untuk mendapatkan berbagai bonus permanen. Salah satu kode starter yang bisa dicoba pemain baru:

  > **`STARTER PACK`** — memberikan **1000 Koin** dan **20 Cosmic Koin** untuk membantu memulai permainan.

  Kode-kode lainnya sengaja dirahasiakan sebagai bagian dari keseruan eksplorasi game ini — selamat mencari! 🔍

## 💾 Data & Progres

- Semua progres disimpan otomatis di `localStorage` browser kamu.
- Gunakan tombol **Reset Save** di menu (jika tersedia) apabila ingin memulai dari awal — tindakan ini permanen dan tidak bisa dibatalkan.

## ⚠️ Catatan

File ini adalah game single-file (`endless.html`) yang berjalan sepenuhnya di sisi klien (client-side), tanpa memerlukan koneksi internet setelah dibuka.

Selamat bermain dan semoga bertahan hingga seribu tahun! ⚔️
