<img width="1983" height="793" alt="image" src="https://github.com/user-attachments/assets/13e54f5f-9b1b-4fe6-8e82-d7a181473fb3" />

# BioKimIndra (｡•̀ᴗ-)✧

> Belajar biokimia sistem indra tanpa bikin kepala ikut berputar! (ง ื▿ ื)ว

## Tentang Proyek (｡･ω･｡)

BioKimIndra adalah platform belajar biokimia sistem indra dengan visualisasi interaktif, animasi bertahap, dan kuis otomatis. Pelan-pelan saja, yang penting paham alurnya. (๑˃ᴗ˂)ﻭ

## Materi ( •̀ ω •́ )✧

- **Optik:** fototransduksi, rodopsin, transducin, PDE, cGMP, kanal CNG.
- **Integumen:** rangsangan panas, kanal TRPV, aliran ion, potensial aksi.
- **Olfaktori:** GPCR, G-protein, adenilat siklase, cAMP, kanal ion.
- **Gustatori:** reseptor rasa, PLCβ2, IP₃, Ca²⁺, TRPM5, ATP.
- **Vestibular:** otolit, tip links, mekanotransduksi sel rambut.
- **Koklear:** koklea, organ Corti, kanal mekanosensitif, neurotransmiter.

## Fitur (ﾉ´ヮ`)ﾉ*:･ﾟ

- Enam jalur transduksi indra.
- Visualisasi 2D animatif dan kaskade mekanisme.
- Kontrol putar, jeda, mulai ulang, langkah sebelumnya/berikutnya, dan kecepatan.
- Kuis otomatis dengan pembahasan.
- Ujian campuran 12 soal acak.
- Progres dan rekor skor tersimpan di browser.
- Antarmuka responsif untuk desktop dan perangkat seluler.

## Teknologi ( •̀ᴗ•́ )و

- [Next.js](https://nextjs.org/) 16
- [React](https://react.dev/) 19 dan [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/) 4
- [Bun](https://bun.sh/)
- [Zustand](https://zustand.docs.pmnd.rs/)
- [Framer Motion](https://motion.dev/)

## Menjalankan Lokal (ง •̀_•́)ง

1. Clone repo: `git clone https://github.com/kazadarojat/biokimindra.git`
2. Masuk folder: `cd biokimindra`
3. Instal dependensi: `bun install`
4. Jalankan: `bun run dev`
5. Buka http://localhost:3000

Perintah lain: `bun run build`, `bun run start`, `bun run lint`. Perintah database Prisma hanya diperlukan jika fitur database dikonfigurasi. Skrip build/start memakai utilitas shell seperti cp dan tee; di Windows mungkin perlu shell yang kompatibel atau penyesuaian skrip. (｡•́︿•̀｡)

## Struktur Proyek (・・ ) ?

~~~text
src/
├── app/
├── components/
│   ├── platform/
│   └── scenes/
├── data/
│   ├── pathways.ts
│   └── quiz.ts
└── lib/
    └── progress-store.ts
~~~

## Tujuan Pembelajaran (๑•̀ㅂ•́)و

- Menjelaskan urutan dasar transduksi rangsangan pada berbagai sistem indra.
- Mengidentifikasi reseptor, molekul perantara, kanal ion, dan neurotransmiter.
- Menghubungkan perubahan molekuler dengan aktivitas listrik sel.
- Mengevaluasi pemahaman melalui latihan soal.

## Kontribusi (づ｡◕‿‿◕｡)づ

Ide, koreksi materi, laporan bug, dan usulan fitur sangat terbuka. Fork repo, buat branch, sertakan referensi ilmiah untuk koreksi materi, lalu ajukan Pull Request. Terima kasih sudah ikut membuat proyek ini lebih baik! (づ￣ ³￣)づ

## Disclaimer (._.)

BioKimIndra adalah proyek edukasi, bukan pengganti buku ajar, praktikum, konsultasi dosen, atau sumber pembelajaran resmi. Cocokkan materi dengan referensi ilmiah terbaru.

## Lisensi

Belum ada lisensi yang dinyatakan. Jangan mengasumsikan kode atau aset bebas digunakan, dimodifikasi, atau didistribusikan sampai lisensi ditambahkan.

---

<p align="center"><strong>Belajar memahami mekanisme indra, satu kaskade pada satu waktu.</strong><br>(ﾉ≧∀≦)ﾉ ✧ Semangat belajarnya! ✧</p>
