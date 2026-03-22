# PsychoMetric — Platform Tes Psikologi Profesional

> Dibuat oleh **Alfi Syahr Nur Widenky**

Platform tes psikologi berbasis web yang interaktif, estetik, dan berbasis sains. Dirancang untuk membantu pengguna memahami kepribadian, kecerdasan emosi, dan potensi karir secara mendalam — lengkap dengan laporan PDF yang bisa diunduh.

---

## Tampilan

- Desain **earth tone aesthetic** dengan palet krem, rust, sage, dan gold
- Tipografi premium: **Fraunces** (display) + **DM Sans** (body)
- Animasi smooth, progress bar, dan transisi antar soal yang responsif
- Fully responsive — bekerja di desktop maupun mobile

---

## Fitur Utama

- **5 jenis tes psikologi** yang berbeda dalam satu platform
- **Form data diri** sebelum memulai tes (nama, usia, gender, pendidikan, pekerjaan)
- **Auto-advance** setelah memilih jawaban untuk pengalaman yang lebih smooth
- **Hasil konsisten** — jawaban yang sama selalu menghasilkan profil yang sama (berbasis algoritma deterministik)
- **Download PDF** laporan resmi 2 halaman (cover + analisis detail)
- Identitas pembuat ditampilkan di navbar, landing page, footer, dan di dalam PDF

---

## Jenis Tes yang Tersedia

| Tes | Dimensi | Jumlah Soal | Tipe Soal |
|-----|---------|-------------|-----------|
| 🎯 **DISC** | Dominance, Influence, Steadiness, Conscientiousness | 10 soal | Pilihan ganda 4 opsi |
| 🧠 **MBTI** | 16 tipe kepribadian (E/I, S/N, T/F, J/P) | 12 soal | Pilihan ganda 2 opsi |
| 🌱 **RIASEC** | Realistic, Investigative, Artistic, Social, Enterprising, Conventional | 24 soal | Skala Likert 1–5 |
| 💛 **EQ** | Kesadaran Diri, Regulasi Emosi, Empati, Motivasi, Keterampilan Sosial | 30 soal | Skala Likert 1–5 |
| ⭐ **Big Five** | Openness, Conscientiousness, Extraversion, Agreeableness, Neuroticism | 30 soal | Skala Likert 1–5 |

---

## Alur Penggunaan

```
1. Landing Page
   └── Lihat pilihan tes yang tersedia

2. Form Data Diri
   └── Isi nama, usia, gender, pendidikan, pekerjaan
   └── Pilih jenis tes yang diinginkan

3. Sesi Tes
   └── Jawab pertanyaan satu per satu
   └── Progress bar menampilkan kemajuan
   └── Bisa navigasi maju/mundur

4. Halaman Hasil
   └── Tipe/profil kepribadian
   └── Skor per dimensi (visualisasi bar)
   └── Kekuatan utama
   └── Area pengembangan
   └── Rekomendasi karir

5. Download PDF
   └── Laporan resmi 2 halaman
   └── Berisi data peserta + analisis lengkap
```

---

## Struktur File

```
psikologi-tes.html    ← Seluruh aplikasi dalam satu file HTML
README.md             ← Dokumentasi ini
```

Aplikasi ini adalah **single-file HTML** — tidak membutuhkan server, framework, atau instalasi apapun.

---

## Cara Menjalankan

Cukup buka file `psikologi-tes.html` di browser modern manapun:

```bash
# Opsi 1: Klik dua kali file HTML di file explorer

# Opsi 2: Via terminal
open psikologi-tes.html        # macOS
start psikologi-tes.html       # Windows
xdg-open psikologi-tes.html    # Linux
```

Tidak perlu koneksi internet khusus — hanya Google Fonts dan jsPDF yang di-load dari CDN.

---

## Dependensi Eksternal

| Library | Versi | Fungsi |
|---------|-------|--------|
| [Google Fonts](https://fonts.google.com) | — | Tipografi (Fraunces + DM Sans) |
| [jsPDF](https://github.com/parallax/jsPDF) | 2.5.1 | Generate laporan PDF |

---

## Detail Teknis

### Sistem Scoring

- **DISC** — Menghitung frekuensi pilihan per dimensi (D/I/S/C), dimensi terbanyak menjadi tipe dominan
- **MBTI** — Membandingkan skor berpasangan (E vs I, S vs N, T vs F, J vs P), menghasilkan 4-huruf kode dari 16 kemungkinan
- **RIASEC** — Rata-rata skor Likert per dimensi, 3 dimensi tertinggi menjadi kode Holland, dicocokkan ke peta karir
- **EQ** — Rata-rata per subdimensi (SE, ER, EM, MT, RS) dikonversi ke skala 0–100, level ditentukan dari total rata-rata
- **Big Five** — Rata-rata per dimensi OCEAN dikonversi ke persentase, profil dideskripsikan berdasarkan threshold tinggi/sedang/rendah

### Konsistensi Hasil

Semua hasil bersifat **deterministik** — tidak ada elemen acak. Jawaban yang sama akan selalu menghasilkan tipe dan skor yang identik, sehingga cocok untuk keperluan assessment formal.

### PDF Output

- Format A4 portrait, 2 halaman
- Halaman 1: Cover dengan data peserta, tipe hasil, dan info tes
- Halaman 2: Analisis detail — deskripsi, bar chart skor, kekuatan, pengembangan, rekomendasi karir
- Nama file: `PsychoMetric_[Nama]_[Tes]_[Tanggal].pdf`

---

## Browser yang Didukung

| Browser | Status |
|---------|--------|
| Chrome 90+ | ✅ Didukung penuh |
| Firefox 88+ | ✅ Didukung penuh |
| Safari 14+ | ✅ Didukung penuh |
| Edge 90+ | ✅ Didukung penuh |
| IE 11 | ❌ Tidak didukung |

---

## Pengembangan Lebih Lanjut

Beberapa ide fitur yang bisa ditambahkan:

- [ ] Simpan riwayat hasil tes ke `localStorage`
- [ ] Halaman perbandingan dua peserta
- [ ] Mode admin untuk melihat semua hasil tes
- [ ] Integrasi backend untuk penyimpanan database
- [ ] Tambahan tes: Wartegg, Grafologi, IST (Inteligensi)
- [ ] Versi multi-bahasa (EN/ID)
- [ ] Sharing hasil via link atau media sosial

---

## Lisensi

Proyek ini dibuat untuk keperluan pribadi dan edukasi.  
Dilarang mendistribusikan ulang tanpa izin dari pembuat.

---

<div align="center">

**PsychoMetric**  
*Platform Tes Psikologi Profesional*

Dibuat dengan ❤️ oleh **Alfi Syahr Nur Widenky**

</div>
