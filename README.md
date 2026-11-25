# IT Career Explorer — Ngawam Digital (v2)

Playbook interaktif gratis untuk orang yang baru penasaran dengan dunia IT. Waktu baca sekitar 10 menit. Dibuat dengan HTML, CSS, dan JavaScript biasa, tanpa framework, tanpa login, dan tanpa database.

## Isi folder

```
index.html            ← seluruh playbook
assets/logo-mark.png  ← logo kecil di header (simbol N, latar transparan)
assets/logo-ngawam.png← logo utama di halaman awal (latar transparan)
README.md
CHANGELOG.md
```

Folder `assets/` wajib ikut diunggah bersama `index.html`.

## Isi playbook

| Bagian | Isi | Waktu |
| --- | --- | --- |
| Halaman awal | Logo, judul, estimasi waktu, daftar isi | – |
| 1. Dunia IT dalam 2 menit | Siklus pembuatan aplikasi, siapa yang terlibat | 2 menit |
| 2. Kenalan dengan 6 role | Kartu QA, BA, PM, PO, UI/UX, Developer | 3 menit |
| 3. Cari role untuk dieksplorasi | 6 pertanyaan, 1–3 rekomendasi role beserta alasannya | 2 menit |
| 4. Simulasi Santap | Lingkaran kolaborasi enam role dan contoh proses yang berulang | 2 menit |
| 5. Langkah berikutnya | 3 skill dasar per role, kartu CTA, tandai selesai | 1 menit |
| Bonus (opsional) | Tantangan eksplorasi 7 hari dengan checklist | di luar 10 menit |

Bonus tidak dihitung dalam progres "x dari 5 bagian". Progres checklist bonus tetap tersimpan dan terlihat di menu "Isi".

Progres tersimpan di browser pembaca (localStorage, kunci `ngawam-it-explorer-v1`). Pembaca yang sudah memakai versi 1 tidak kehilangan progresnya. Kalau penyimpanan browser diblokir, playbook tetap bisa dipakai, hanya progresnya tidak tersimpan.

## Cara menjalankan di komputer

Buka folder, lalu klik dua kali `index.html`. Tidak perlu install apa pun.

## Bagian yang perlu diedit

Buka `index.html` dengan editor teks (VS Code atau Notepad), lalu cari kata kunci dengan Ctrl+F.

### 1. Link dan kartu CTA

Cari `var CONFIG`. Setiap kartu tertulis seperti ini:

```js
{ id: "ebook", aktif: true, utama: true,
  judul: "Ebook: Berkarier di Project Software Tanpa Latar Belakang IT",
  deskripsi: "...",
  tombol: "Lihat ebook",
  link: "" },   // GANTI: link halaman pembelian ebook
```

- `link`: isi alamatnya di antara tanda kutip. Kalau dibiarkan `""`, tombol tampil "Segera hadir" dan tidak bisa diklik.
- `aktif`: `true` untuk menampilkan, `false` untuk menyembunyikan.
- `utama`: kartu yang disorot warna gold. Cukup satu kartu.
- `hanyaUntukRole`: kartu hanya muncul kalau hasil kuis pembaca menyertakan role tersebut. BA Starter Kit memakai `"ba"`.
- Urutan kartu di halaman mengikuti urutan di daftar.

Setiap baris yang perlu diisi diberi komentar `// GANTI`.

| Kartu | Status awal |
| --- | --- |
| Ebook (kartu utama) | Tampil |
| Threads | Tampil |
| Form minat belajar | Tampil |
| Career Clinic | Disembunyikan (`aktif: false`) |
| BA Starter Kit | Disembunyikan; kalau diaktifkan, hanya tampil untuk hasil yang menyertakan BA |

### 2. Logo

Ganti file di folder `assets/` dengan nama yang sama:

- `assets/logo-mark.png`: simbol saja, latar transparan, tinggi minimal 52 px.
- `assets/logo-ngawam.png`: logo lengkap, latar transparan. Tampil di atas latar navy, jadi pakai versi yang terbaca di latar gelap.

Tidak perlu mengubah kode. Kalau file logo tidak ditemukan, playbook otomatis menampilkan teks cadangan ("N" di header dan "Ngawam Digital" di halaman awal).

Untuk memakai nama file lain, cari `LOGO KECIL` atau `LOGO UTAMA` di `index.html`, lalu ganti bagian `src="..."`.

### 3. Lainnya

| Yang ingin diganti | Cari kata kunci |
| --- | --- |
| Nama brand di header dan footer | `brandName:` |
| Warna brand | `WARNA BRAND NGAWAM DIGITAL` (`--navy`, `--gold`, `--teal`). Warna mode gelap ada tepat di bawahnya. |
| Isi role, kuis, simulasi, skill, tantangan | `var ROLES`, `var QUESTIONS`, `var SIM`, `var SKILLS`, `var DAYS` |

Catatan kuis: setiap jawaban di `QUESTIONS` diberi kode role (`qa`, `ba`, `pm`, `po`, `ux`, `dev`), dan setiap role muncul 4 kali dari 6 pertanyaan supaya hasilnya seimbang. Kalau mengubah pilihan, jaga keseimbangan ini. Setelah mengubah kuis secara besar, ganti `var KEY = "ngawam-it-explorer-v1"` menjadi `-v2` supaya progres lama pembaca tidak bentrok.

## Deploy gratis

### Pilihan A: Netlify Drop

1. Buka app.netlify.com/drop dan login.
2. Seret **seluruh folder** (berisi `index.html` dan folder `assets`) ke halaman tersebut.
3. Netlify memberi alamat seperti `nama-acak.netlify.app`. Ganti namanya di **Site configuration → Change site name**.
4. Untuk update, buka tab **Deploys**, lalu seret folder versi baru.

### Pilihan B: GitHub Pages

1. Buat repository **Public** baru, misalnya `it-career-explorer`.
2. Klik **Add file → Upload files**, lalu seret `index.html` dan folder `assets` sekaligus. Klik **Commit changes**.
3. Buka **Settings → Pages**. Pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu beberapa menit. Alamatnya akan berbentuk `namaakun.github.io/it-career-explorer`.

Setelah deploy, buka alamatnya dan pastikan logo tampil. Kalau yang muncul teks "N", berarti folder `assets` belum ikut terunggah.

## Checklist uji ulang

Uji di satu browser desktop (Chrome atau Edge) dan satu HP.

**Logo dan tampilan**
- [ ] Logo simbol tampil di header; logo lengkap tampil di halaman awal.
- [ ] Di HP, logo halaman awal ada di atas judul dan tidak ada bagian yang perlu digeser ke samping.
- [ ] Teks terbaca jelas di mode terang dan mode gelap.

**Navigasi**
- [ ] "Mulai Eksplorasi" membuka Bagian 1.
- [ ] "Lanjut" dan "Kembali" di setiap bagian berpindah ke bagian yang benar.
- [ ] Menu "Isi" membuka setiap bagian, termasuk "Bonus: tantangan 7 hari", lalu menu tertutup.
- [ ] Klik logo kembali ke halaman awal. Tombol back browser kembali ke bagian sebelumnya.

**Bagian 2 dan 3**
- [ ] Keenam kartu role bisa dibuka dan ditutup.
- [ ] Catatan "Ini bukan tes" tampil di atas pertanyaan.
- [ ] Tombol "Lihat hasil" baru aktif setelah 6 pertanyaan dijawab.
- [ ] Hasil berjudul "Rekomendasi role untuk kamu eksplorasi", menampilkan 1–3 role beserta jawabannya, dan catatan "bukan tes psikologi atau penentu karier".
- [ ] "Baca lagi kartu …" membuka kartu yang benar. "Ulangi pertanyaan" mengosongkan jawaban.

**Bagian 4 dan 5**
- [ ] Keenam role di lingkaran bisa diklik (dan dipilih dengan Tab + Enter); panel berganti isi.
- [ ] "Role sebelumnya/berikutnya" berfungsi; hitungan "x dari 6 role dilihat" bertambah.
- [ ] Tab skill berganti isi; tab awal sesuai role teratas dari kuis.
- [ ] Kartu "Bonus opsional" membuka halaman tantangan 7 hari.
- [ ] Tombol CTA yang punya link membuka tab baru; yang belum tampil "Segera hadir".
- [ ] "Tandai selesai" membuat progres menjadi 5 dari 5.

**Bonus**
- [ ] Centang hari mengubah teks, bar progres, dan angka di menu "Isi".
- [ ] Progres bagian (x dari 5) tidak berubah saat mencentang bonus.

**Penyimpanan dan reset**
- [ ] Setelah refresh, progres, jawaban kuis, role yang dilihat, dan centang bonus masih ada.
- [ ] Halaman awal menampilkan "Lanjutkan" setelah ada progres.
- [ ] "Reset progres" di footer meminta konfirmasi, lalu menghapus semua progres.

**Sebelum dibagikan**
- [ ] Semua link `// GANTI` di `CONFIG` sudah diisi dan dicoba.
- [ ] Klaim di kartu ebook masih sesuai isi ebook versi terbaru.
