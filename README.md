# 🧬 BioKimIndra

> **Belajar biokimia sistem indra tanpa bikin kepala ikut berputar.**  
> Platform belajar interaktif untuk memahami mekanisme transduksi sinyal pada sistem indra melalui visualisasi 2D, animasi bertahap, dan kuis evaluasi otomatis.

<p align="center">
  <strong>👁️ Optik · 🌡️ Integumen · 👃 Olfaktori · 👅 Gustatori · ⚖️ Vestibular · 🎧 Koklear</strong>
</p>

---

## ✨ Tentang Proyek

**BioKimIndra** adalah platform pembelajaran biokimia sistem indra yang membantu mahasiswa memahami bagaimana rangsangan diterjemahkan menjadi sinyal saraf. Materi disajikan sebagai kaskade mekanisme yang dapat dijelajahi langkah demi langkah, dilengkapi visualisasi animasi dan kuis dengan umpan balik langsung.

Proyek ini dirancang sebagai teman belajar untuk mengulang materi, memahami urutan mekanisme molekuler, dan berlatih sebelum evaluasi akademik maupun praktikum.

## 🔬 Materi yang Tersedia

| Jalur | Fokus pembelajaran |
|---|---|
| 👁️ **Optik** | Fototransduksi pada fotoreseptor: rodopsin, transducin, PDE, cGMP, kanal CNG, dan perubahan potensial membran |
| 🌡️ **Integumen** | Transduksi rangsangan panas, kanal TRPV, aliran ion, dan pembentukan potensial aksi |
| 👃 **Olfaktori** | Transduksi bau melalui GPCR, G-protein, adenilat siklase, cAMP, dan kanal ion |
| 👅 **Gustatori** | Transduksi rasa melalui reseptor, PLCβ2, IP₃, Ca²⁺, TRPM5, dan pelepasan ATP |
| ⚖️ **Vestibular** | Mekanotransduksi pada sistem keseimbangan, pergeseran otolit, tip links, dan aktivasi sel rambut |
| 🎧 **Koklear** | Transduksi suara di koklea, organ Corti, kanal mekanosensitif, dan pelepasan neurotransmiter |

> Materi ini merupakan sarana belajar. Tetap cocokkan detail mekanisme dengan buku ajar, referensi kuliah, dan arahan dosen.

## 🚀 Fitur Utama

- **🧪 Enam jalur transduksi indra** dengan urutan mekanisme dan molekul kunci.
- **🎞️ Visualisasi 2D animatif** untuk membantu membayangkan proses yang sulit diamati secara langsung.
- **⏯️ Kontrol belajar interaktif**: putar, jeda, mulai ulang, langkah sebelumnya/berikutnya, dan pengaturan kecepatan.
- **🧭 Tampilan kaskade** untuk melihat urutan tahapan dalam satu jalur.
- **📝 Kuis dengan evaluasi otomatis** dan pembahasan jawaban.
- **🎯 Ujian campuran** berisi 12 soal yang dipilih secara acak.
- **📈 Pelacakan progres belajar** dan rekor skor yang disimpan di browser.
- **📱 Antarmuka responsif** untuk desktop maupun perangkat seluler.

## 🖥️ Teknologi

Proyek ini dibangun menggunakan:

- [Next.js](https://nextjs.org/) 16
- [React](https://react.dev/) 19 dan [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/) 4
- [Bun](https://bun.sh/) sebagai package manager/runtime yang digunakan dalam skrip proyek
- [Zustand](https://zustand.docs.pmnd.rs/) untuk penyimpanan state dan progres lokal
- [Framer Motion](https://motion.dev/) untuk animasi antarmuka
- SVG dan animasi SMIL untuk visualisasi mekanisme

## ⚙️ Menjalankan Secara Lokal

### Prasyarat

- [Bun](https://bun.sh/) terpasang
- Git terpasang

### Instalasi

1. Clone repositori:

   ```bash
   git clone https://github.com/kazadarojat/biokimindra.git
   cd biokimindra
   ```

2. Pasang dependensi:

   ```bash
   bun install
   ```

3. Jalankan server pengembangan:

   ```bash
   bun run dev
   ```

4. Buka [http://localhost:3000](http://localhost:3000) di browser.

### Perintah yang tersedia

| Perintah | Fungsi |
|---|---|
| `bun run dev` | Menjalankan server pengembangan pada port 3000 |
| `bun run build` | Membuat build produksi |
| `bun run start` | Menjalankan server produksi dari hasil build |
| `bun run lint` | Memeriksa kode menggunakan ESLint |
| `bun run db:generate` | Menghasilkan Prisma Client |
| `bun run db:push` | Menyinkronkan skema Prisma ke database |
| `bun run db:migrate` | Menjalankan migrasi pengembangan Prisma |
| `bun run db:reset` | Mereset database pengembangan |

> **Catatan:** perintah database hanya diperlukan jika bagian aplikasi yang menggunakan Prisma memang dikonfigurasi. Perintah build/start pada `package.json` menggunakan utilitas shell seperti `cp` dan `tee`; pada Windows, jalankan melalui shell yang mendukung perintah tersebut atau sesuaikan skripnya.

## 🧑‍🎓 Cara Menggunakan

1. Buka tab **Jalur Indra** dan pilih sistem indra yang ingin dipelajari.
2. Ikuti visualisasi dari satu tahap ke tahap berikutnya.
3. Gunakan kontrol playback untuk mengulang atau memperlambat proses.
4. Perhatikan molekul, ion, dan perubahan sinyal pada setiap fase.
5. Kerjakan kuis untuk menguji pemahaman dan baca pembahasan setelah menjawab.
6. Pantau progres dan rekor skor dari sesi belajar berikutnya pada browser yang sama.

## 🗂️ Struktur Proyek

Gambaran berkas utama:

```text
src/
├── app/                 # Halaman, layout, dan styling global
├── components/
│   ├── platform/        # Komponen antarmuka pembelajaran dan kuis
│   └── scenes/          # Visualisasi animasi jalur transduksi
├── data/
│   ├── pathways.ts      # Data tahapan jalur transduksi
│   └── quiz.ts          # Bank soal dan logika set ujian
└── lib/
    └── progress-store.ts # Penyimpanan progres belajar lokal
```

## 🧠 Tujuan Pembelajaran

Setelah menggunakan BioKimIndra, pengguna diharapkan dapat:

- Menjelaskan urutan dasar transduksi rangsangan pada berbagai sistem indra.
- Mengidentifikasi reseptor, molekul perantara, kanal ion, dan neurotransmiter yang terlibat.
- Menghubungkan perubahan molekuler dengan perubahan aktivitas listrik sel.
- Menguji dan mengevaluasi pemahaman melalui latihan soal.

## 🤝 Kontribusi

Ide, koreksi materi, pelaporan bug, dan usulan fitur sangat terbuka.

1. Fork repositori ini.
2. Buat branch baru untuk perubahan.
3. Jelaskan perubahan yang dibuat dan sertakan referensi ilmiah untuk koreksi materi.
4. Ajukan Pull Request dengan deskripsi yang jelas.

Untuk koreksi konten biokimia, utamakan buku ajar atau sumber ilmiah tepercaya agar materi tetap akurat.

## ⚠️ Disclaimer

BioKimIndra merupakan proyek edukasi dan bukan pengganti buku ajar, praktikum, konsultasi dosen, atau sumber pembelajaran resmi. Materi dapat terus dikembangkan dan perlu ditinjau secara berkala berdasarkan referensi ilmiah terbaru.

## 📄 Lisensi

Belum ada lisensi yang dinyatakan pada README ini. Sampai lisensi ditambahkan ke repositori, jangan mengasumsikan bahwa kode atau aset bebas digunakan, dimodifikasi, maupun didistribusikan.

---

<p align="center">
  Dibuat untuk belajar memahami mekanisme indra, satu kaskade pada satu waktu. 🧬✨
</p>
