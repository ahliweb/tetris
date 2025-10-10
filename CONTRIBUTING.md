# 🤝 Panduan Kontribusi (CONTRIBUTING.md)

**Project:** 🎮 Tetris Statis (Basic Edition)  
**Organization:** [PT Ahli Web Internasional](https://ahliweb.co.id)  
**Author:** Unggul Cahya Saputra  
**Program:** Ekskul Coding & AI Terpadu  
**Lisensi:** MIT License  

---

## 💬 Pendahuluan
Terima kasih telah tertarik berkontribusi pada proyek **Tetris Statis**!  
Proyek ini bertujuan sebagai sarana belajar logika pemrograman dasar menggunakan **HTML, CSS, dan JavaScript**, serta akan dikembangkan ke versi lanjutan dengan **Dart + Serverpod + Jaspr + Flutter Web**.

Kami menyambut kontribusi dalam bentuk:
- 💡 Ide & saran perbaikan.
- 🧱 Perbaikan bug dan optimalisasi kode.
- 🎨 Penyempurnaan tampilan (UI/UX).
- 📚 Dokumentasi dan tutorial tambahan.

---

## ⚙️ Persiapan Awal
1. Pastikan kamu sudah memiliki akun GitHub.  
2. *Fork* repositori ini: [https://github.com/ahliweb/tetris](https://github.com/ahliweb/tetris)  
3. *Clone* hasil fork ke komputer lokal:
   ```bash
   git clone https://github.com/<username>/tetris.git
   cd tetris/statis
````

4. Pastikan struktur awal sesuai:

   ```
   tetris/
   └── statis/
       ├── tetris.html
       └── README.md
   ```
5. Gunakan editor yang nyaman (disarankan: **VS Code** atau **Cursor IDE**).

---

## 🧩 Cara Kontribusi

### 1. Buat Branch Baru

Gunakan format penamaan yang jelas:

```bash
git checkout -b fitur/nama-fitur
# contoh:
# git checkout -b fitur/tambah-skor-tinggi
```

### 2. Lakukan Perubahan

* Tulis kode dengan rapi dan konsisten.
* Gunakan komentar (`//`) untuk menjelaskan logika penting.
* Uji fungsionalitas sebelum commit.

### 3. Commit Perubahan

Gunakan format pesan commit yang deskriptif:

```bash
git add .
git commit -m "feat: tambah sistem skor dan reset game"
```

### 4. Push & Pull Request

```bash
git push origin fitur/nama-fitur
```

Kemudian buka halaman repositori fork-mu di GitHub, dan klik:

> **Compare & Pull Request**

Berikan deskripsi singkat tentang apa yang kamu ubah dan alasannya.

---

## 📜 Gaya Penulisan Kode

* Gunakan **indentasi 2 spasi**.
* Gunakan **nama variabel deskriptif** (hindari `x1`, `tmp`, dll).
* Gunakan gaya konsisten:

  ```js
  const playerScore = 0;
  function updateScore() { ... }
  ```
* Jangan ubah struktur utama file kecuali disetujui melalui *issue discussion*.

---

## 💡 Saran Pengembangan

Kami mendorong kontribusi ke arah:

* Menambahkan **level & kecepatan dinamis**.
* Menyimpan skor tertinggi di **localStorage**.
* Menambah efek suara atau animasi.
* Membuat mode “Dark / Light Theme”.
* Porting ke versi **Dart + Serverpod + Jaspr + Flutter Web**.

---

## 🛡️ Etika Kontributor

* Patuhi [Code of Conduct](./CODE_OF_CONDUCT.md).
* Gunakan bahasa sopan, profesional, dan saling menghormati.
* Tidak ada spam, iklan, atau plagiarisme.
* Semua kontribusi di bawah lisensi **MIT**.

---

## 📬 Hubungi Kami

Jika ingin berdiskusi sebelum berkontribusi, kamu bisa menghubungi:

* 💌 **[team@ahliweb.co.id](mailto:team@ahliweb.co.id)**
* 🧠 **[sec@satpamsiber.com](mailto:sec@satpamsiber.com)** (untuk keamanan & bug report)

---

## 🌟 Ucapan Terima Kasih

Kami menghargai setiap kontribusi, sekecil apa pun.
Bersama kita bangun komunitas pembelajar yang **cerdas, beradab, dan berilmu**.

> 🧩 *Bagian dari ekosistem edukasi digital AhliWeb.co.id – “Berkarya dengan Ilmu, Amanah, dan Akhlak Mulia.”*

```

---

📦 **Langkah upload ke repo GitHub:**
1. Masuk ke repository `ahliweb/tetris`
2. Klik **Add file → Create new file**
3. Beri nama: `CONTRIBUTING.md`
4. Salin isi di atas → klik **Commit new file**

---
