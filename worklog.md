# Worklog

---
Task ID: 1
Agent: main (Z.ai)
Task: Membangun Platform Belajar Mekanisme Biokimia Sistem Indra interaktif (visualisasi 2D jalur sinyal saraf + kuis evaluasi otomatis)

Work Log:
- Klasifikasi tugas: Type 3 (Interactive Web Development) → memuat skill fullstack-dev, jalankan init script (Next.js 16 + Tailwind 4 + shadcn/ui + zustand + framer-motion).
- Membuat data materi `src/data/pathways.ts`: 6 jalur (Optik 10 langkah, Integumen 6, Olfaktori 11, Gustatori 11, Vestibular 10, Koklear 13 = 61 langkah) sesuai urutan kaskade dari materi user, lengkap dengan fase scene, molekul kunci, dan fakta.
- Membuat bank soal `src/data/quiz.ts`: 37 soal (5-6 per jalur + 6 soal integratif campuran) dengan pembahasan; fungsi buildExamSet (12 soal acak) dan shuffle.
- Store progres `src/lib/progress-store.ts` (zustand persist localStorage): progres langkah per jalur, jalur selesai, rekor skor kuis, reset.
- Kit scene `src/components/scenes/scene-kit.tsx` (SceneFrame, P phase-dim, Lbl, Ion, IonFlow SMIL, ZoomBox) + keyframes SVG di globals.css.
- 6 scene SVG animasi 2D: OptikScene (mata+rodopsin→all-trans, transducin/PDE/cGMP, kanal CNG tertutup, grafik hiperpolarisasi, vesikel glutamat), IntegumenScene (termometer 40°, gelombang panas, TRPV, ion Na/Ca, gauge potensial, AP berjalan), OlfaktoriScene (hidung, odorant, GPCR→Gα-GTP→ACIII→cAMP, CNG, Cl⁻ keluar, AP ke bulbus), GustatoriScene (lidah, T1R2+T1R3, PLCβ2, IP₃→ER→Ca²⁺, TRPM5, CALHM1/3→ATP→P2X), VestibularScene (lift naik beranimasi, otolith bergeser, striola, tip links tegang, MET, K⁺, VGCC, eksositosis), KoklearScene (gelombang suara, timpani bergetar, stapes, spiral koklea + gelombang perilimfe, organ Corti, MET, VGCC, glutamat).
- Komponen platform: FlowCascade (metro line 61 node auto-scroll), PathwayView (scene + caption fase + kontrol play/pause/restart/prev/next/kecepatan 0.5-2x + detail langkah + CTA selesai), PathwayGrid (kartu progres), HomeView (hero, statistik, cara pakai), QuizView (pilih mode, sesi soal dengan feedback instan + pembahasan, layar hasil + tinjauan + rekor skor).
- page.tsx: shell navigasi tab (Beranda/Jalur Indra/Kuis), AnimatePresence, footer sticky; layout.tsx metadata Indonesia + lang="id".
- Perbaikan lint: menghilangkan setState-in-effect (interval pakai idxRef, kuis auto-start via prop initialQuizId + remount nonce).
- **Bug kritis ditemukan & diperbaiki via Agent Browser**: `answered = selected !== null` membuat tombol "Periksa Jawaban" tergantikan begitu opsi dipilih → jawaban tak pernah terekam (skor selalu 0). Fix: pisahkan state `checked`; verified 5/5 = 100% di browser.
- Verifikasi Agent Browser end-to-end: beranda, kartu jalur, playback otomatis kaskade (langkah maju, fase berganti), CTA tuntas, kuis per jalur (skor benar), ujian campuran 12 soal, progres persist (2/6), responsif mobile 390px, footer sticky, tanpa error konsol.
- Aksesibilitas: aria-label pada tab ikon mobile, role/aria pada kaskade & kuis.
- Lint final: 0 error, 0 warning. dev.log bersih (200 OK).

Stage Summary:
- Aplikasi web berjalan di port 3000 (route `/`), semua fitur inti terverifikasi via browser.
- Artefak: src/data/{pathways,quiz}.ts, src/lib/progress-store.ts, src/components/scenes/* (7 file), src/components/platform/* (7 file), src/app/{page,layout,globals.css}.
- Keputusan penting: tema gelap ilmiah dengan aksen per jalur (violet/oranye/hijau/pink/teal/amber), ion berkode warna konsisten antar scene, animasi partikel SMIL + dim per fase.
