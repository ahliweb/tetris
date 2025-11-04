# 🎮 Game Tetris by AhliWeb - Tetris Statis (Basic Edition)

Versi dasar **Game Tetris klasik** menggunakan **HTML, CSS, dan JavaScript** tanpa framework.
Dikembangkan oleh **PT Ahli Web Internasional** untuk program **Ekskul Coding & AI Terpadu**.

---

## 💡 Tujuan Proyek

Proyek ini bertujuan untuk:

1. Mengenalkan logika dasar pemrograman melalui permainan interaktif.
2. Melatih pemahaman **DOM**, **loop**, dan **event listener**.
3. Menjadi dasar sebelum masuk ke versi **advance (Dart + Serverpod + Jaspr)**.

---

## 🗂️ Struktur Folder

```
tetris/
├── statis/
│   └── tetris.html
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
└── readme.md
```

---

## 📚 Deskripsi Proyek

Game Tetris **Improved Edition** berbasis **HTML, CSS, dan JavaScript**.
Dikembangkan sebagai materi latihan ekskul coding untuk memahami logika pemrograman dasar, manipulasi DOM, dan animasi web interaktif. 🚀

### ✨ Fitur Utama (v2.0):

#### Gameplay
* ✅ Tampilan grid 10x20 klasik
* ✅ **Hold Piece** - Simpan piece untuk digunakan nanti (tekan C)
* ✅ **Ghost Piece** - Bayangan menunjukkan dimana piece akan jatuh
* ✅ **Wall Kick** - Rotasi otomatis saat dekat dinding (SRS system)
* ✅ Sistem skor otomatis dengan combo
* ✅ Level dan kecepatan meningkat progresif

#### UI/UX
* ✅ Welcome screen dengan instruksi lengkap
* ✅ **Touch Controls** untuk mobile/tablet
* ✅ **Settings Panel** (on/off: sound, ghost piece, grid lines)
* ✅ **Game Statistics** (waktu bermain, total pieces, pieces per minute)
* ✅ Desain responsif 3-kolom (desktop) dan adaptive (mobile)
* ✅ Animasi smooth dan visual feedback
* ✅ Tombol UI interaktif dengan hover effects

#### Keamanan & Kode
* ✅ Validasi localStorage dengan sanitization
* ✅ Error handling untuk audio context
* ✅ Komentar lengkap untuk maintainability
* ✅ Code organization dengan sections
* ✅ Data-testid attributes untuk automated testing
* ✅ 100% **Vanilla JavaScript** (tanpa library eksternal)

---

## 🛠️ Cara Menjalankan

1. Clone repositori ini:

   ```bash
   git clone https://github.com/ahliweb/tetris.git
   ```
2. Buka folder proyek:

   ```bash
   cd tetris/statis
   ```
3. Jalankan file `tetris.html` di browser favoritmu (cukup klik dua kali file tersebut).

---

## 🎮 Cara Bermain

### Kontrol Keyboard
- `←` `→` : Geser kiri/kanan
- `↑` : Rotasi piece
- `↓` : Soft drop (turun cepat)
- `Space` : Hard drop (langsung jatuh)
- `C` : Hold piece (simpan untuk nanti)
- `P` : Pause/Resume

### Kontrol UI
- Gunakan tombol pada panel samping
- Touch controls tersedia di mobile

### Tips
- Gunakan ghost piece untuk melihat landing position
- Hold piece strategi untuk kombo lebih baik
- Perhatikan next piece untuk planning

---

## 📚 Dokumentasi

Dokumentasi lengkap tersedia:

- **[📖 DOCS_INDEX.md](./DOCS_INDEX.md)** - Navigasi semua dokumentasi
- **[📋 CHANGELOG.md](./CHANGELOG.md)** - Version history & roadmap
- **[🔒 SECURITY.md](./SECURITY.md)** - Security practices
- **[💻 TECHNICAL_DOCS.md](./TECHNICAL_DOCS.md)** - Deep technical dive (16KB!)
- **[📊 IMPROVEMENTS_SUMMARY.md](./IMPROVEMENTS_SUMMARY.md)** - Complete improvement list

**Total Documentation:** 48KB+ comprehensive docs!

---

## 🔧 Rencana Pengembangan Lanjutan

Tahap berikutnya akan mencakup:

* Porting ke **Dart + Serverpod + Jaspr + Flutter Web**.
* Penambahan sistem login & leaderboard.
* Mode multiplayer.
* UI/UX modern dengan animasi halus.

---

## 👨‍💻 Author

**Unggul Cahya Saputra**
Direktur Operasional — [PT Ahli Web Internasional](https://ahliweb.co.id)

---

## 📝 Lisensi

MIT License © 2025 [AhliWeb.co.id](https://ahliweb.co.id)

---

## 🛡️ Code of Conduct

Proyek ini mengikuti pedoman etika terbuka dan profesional sesuai dokumen:
[🛡️ CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)

---

## 🛠️ Panduan Kontribusi

Panduan lengkap kontribusi tersedia di:
[👨‍💻 CONTRIBUTING.md](./CONTRIBUTING.md)

---

> 🥉 *Bagian dari ekosistem edukasi digital AhliWeb.co.id — “Berkarya dengan Ilmu, Amanah, dan Akhlak Mulia.”*
