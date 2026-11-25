# Changelog — IT Career Explorer

## v2 (25 November 2026)

Revisi terarah dari v1. Struktur 5 bagian, navigasi, kuis, progres, dan reset dipertahankan.

### Konten
- Total waktu baca diringkas dari ±20 menit menjadi ±10 menit (2/3/2/2/1 menit).
- Bagian 1: teks diringkas. Alur proses, catatan siklus berulang, dan peta enam role tetap ada.
- Bagian 2: enam kartu role tetap sama, pengantar dipersingkat.
- Bagian 3: catatan "Ini bukan tes" ditambahkan di atas pertanyaan. Judul hasil diubah menjadi "Rekomendasi role untuk kamu eksplorasi", dan catatan penutup menegaskan bahwa ini rekomendasi, bukan tes psikologi atau penentu karier. **Pertanyaan, pilihan jawaban, dan cara menghitung hasil tidak diubah.**
- Bagian 4: simulasi 7 langkah diganti lingkaran kolaborasi (PO → BA → UI/UX → Developer → QA → Rilis → masukan pengguna → PO, dengan PM di tengah). Setiap role bisa diklik untuk melihat perannya, contoh hasil kerja, dan dengan siapa ia sering bolak-balik. Ditambah tiga contoh proses yang berulang.
- Bagian 5: diganti nama menjadi "Langkah berikutnya". Berisi skill per role, kartu bonus, CTA, dan tombol selesai.
- Tantangan 7 hari dipindah ke halaman bonus opsional (`#tantangan-7-hari`). Tidak dihitung dalam progres 5 bagian; bisa dibuka dari Bagian 5 dan menu.

### Brand dan tampilan
- Logo asli Ngawam Digital ditambahkan (header, halaman awal, kotak selesai) dari folder `assets/`, dengan teks cadangan kalau file tidak ditemukan.
- Warna disesuaikan dengan logo: navy #062B45, gradasi teal-hijau simbol N, cyan tulisan Ngawam. Gold tetap untuk tombol utama.

### CTA
- `CONFIG` diubah menjadi daftar kartu CTA (`aktif`, `utama`, `judul`, `deskripsi`, `tombol`, `link`, `hanyaUntukRole`), dengan komentar `// GANTI` di setiap link.
- Deskripsi ebook disesuaikan dengan isi Ebook V2: 12 bab, latihan di setiap bab, simulasi proyek, roadmap 90 hari, template portfolio, dan persiapan interview.
- Deskripsi Career Clinic dan BA Starter Kit dibuat netral (tanpa janji isi) dan tetap disembunyikan secara default.

### Teknis
- Kunci localStorage tetap `ngawam-it-explorer-v1`. Progres pembaca v1 tetap terbaca; data simulasi lama otomatis disesuaikan dengan 6 role.
- Tidak ada framework atau database baru.
