# x-creator — SOP Akun Quotes X

Repositori ini berisi **dokumentasi SOP (Standar Operasional Prosedur)** untuk pengelolaan sebuah **akun Kata Kutipan (Quotes) bernilai moral di Platform X**, beserta **spec** (requirements, design, tasks) yang menurunkannya. Tujuan project: menjalankan akun secara konsisten dan beretika sambil memenuhi syarat serta mengoptimalkan **Program Sharing Revenue** Platform X.

> Ini adalah proyek **dokumentasi**, bukan perangkat lunak. Seluruh keluaran berupa berkas Markdown.

## Ikhtisar Isi Repositori

```
x-creator/
├─ README.md            # dokumen ini — ringkasan & indeks seluruh repo
├─ sop/                 # DELIVERABLE: dokumen SOP final (3 domain)
└─ .kiro/               # spec & otomasi (requirements, design, tasks, hooks)
```

## 1. Deliverable SOP — `sop/`

Dokumen SOP dikelompokkan menjadi **tiga domain sejajar** dengan satu indeks utama. Lihat indeks lengkap di [`sop/README.md`](sop/README.md).

### a. Operasional Konten — [`sop/operasional-konten/`](sop/operasional-konten/README.md)
Pedoman operasional harian konten & akun.
- [`SOP-Akun-Quotes-X.md`](sop/operasional-konten/SOP-Akun-Quotes-X.md) — dokumen master, Bagian 0–11 (kontrol dokumen, tujuan/peran, kriteria konten, verifikasi & atribusi, styleguide, following, komentar & interaksi, moderasi, eskalasi krisis, jadwal & kalender, metrik & kelayakan, keamanan akun).
- [`lampiran-template.md`](sop/operasional-konten/lampiran-template.md) — template postingan, klarifikasi krisis, log pembelajaran.
- [`lampiran-checklist.md`](sop/operasional-konten/lampiran-checklist.md) — checklist pra-posting, moderasi, keamanan.
- [`lampiran-contoh.md`](sop/operasional-konten/lampiran-contoh.md) — contoh format postingan, thread, & balasan.
- [`lampiran-monetisasi-x.md`](sop/operasional-konten/lampiran-monetisasi-x.md) — peraturan boleh & tidak boleh monetisasi (acuan Content Monetization Standards X).
- [`panduan-brand-identitas.md`](sop/operasional-konten/panduan-brand-identitas.md) — identitas verbal & visual, bio, konsistensi brand.

### b. Operasional Bisnis — [`sop/operasional-bisnis/`](sop/operasional-bisnis/README.md)
Kesepakatan bisnis/finansial antara Founder dan Co-Founder.
- [`modal-dan-bagi-hasil.md`](sop/operasional-bisnis/modal-dan-bagi-hasil.md) — modal awal (6× Premium+), dana cadangan langganan (target 12×), sistem bagi hasil waterfall.
- [`ketentuan-bisnis.md`](sop/operasional-bisnis/ketentuan-bisnis.md) — kepemilikan (70:30), peran, pengeluaran, pencatatan keuangan, tata kelola & sengketa.

### c. Legal & Kepatuhan — [`sop/legal-kepatuhan/`](sop/legal-kepatuhan/README.md)
Kebijakan hukum & kepatuhan lintas-operasional.
- [`kebijakan-hak-cipta-privasi.md`](sop/legal-kepatuhan/kebijakan-hak-cipta-privasi.md) — hak cipta & fair use, klaim/takedown, perlindungan data pribadi (UU PDP), disclosure iklan, disclaimer.
- [`kebijakan-penggunaan-ai.md`](sop/legal-kepatuhan/kebijakan-penggunaan-ai.md) — ruang lingkup & batasan AI, verifikasi wajib, keaslian, privasi data.

## 2. Spec — `.kiro/specs/sop-akun-quotes-x/`

Spec yang menjadi sumber kebenaran di balik deliverable SOP.
- [`requirements.md`](.kiro/specs/sop-akun-quotes-x/requirements.md) — 15 requirement dalam format EARS + glosarium.
- [`design.md`](.kiro/specs/sop-akun-quotes-x/design.md) — struktur, pemetaan requirement, model data, alur kerja, 28 correctness properties, testing strategy.
- [`tasks.md`](.kiro/specs/sop-akun-quotes-x/tasks.md) — rencana implementasi & keterlacakan tugas.

## 3. Otomasi & Aturan Kerja — `.kiro/hooks/` & `.kiro/steering/`

- [`sync-sop-to-spec.kiro.hook`](.kiro/hooks/sync-sop-to-spec.kiro.hook) — hook yang otomatis menyinkronkan spec (requirements/design/tasks) setiap kali berkas SOP di [`sop/`](sop/README.md) diubah.
- [`documentation-links.md`](.kiro/steering/documentation-links.md) — aturan steering: setiap rujukan ke berkas lain wajib berupa tautan Markdown relatif yang dapat diklik, dan tautan diperbarui saat berkas dibuat/dipindahkan/dihapus.

## Konvensi Dokumen

- **ID aturan** stabil per domain: `SOP-N.x` (konten), `SOP-M.x` (monetisasi), `SOP-BR.x` (brand), `SOP-B.x` (bisnis), `SOP-L.x` (legal), `SOP-AI.x` (AI).
- **Keterlacakan**: setiap aturan beranotasi `(Requirement R{n}.{m})` ke `requirements.md`.
- **Penanda ketidaklengkapan**: bagian yang belum final ditandai `> [TODO: ...]`.
- **Kontrol dokumen & versi** diatur pada Bagian 0 dokumen master.

## Cara Memakai

1. Onboarding: baca [`sop/operasional-konten/SOP-Akun-Quotes-X.md`](sop/operasional-konten/SOP-Akun-Quotes-X.md) sebagai pedoman utama.
2. Harian: gunakan checklist pada [`lampiran-checklist.md`](sop/operasional-konten/lampiran-checklist.md) dan template pada [`lampiran-template.md`](sop/operasional-konten/lampiran-template.md).
3. Bisnis & legal: sepakati dan tanda tangani ketentuan pada folder [`operasional-bisnis/`](sop/operasional-bisnis/README.md) dan [`legal-kepatuhan/`](sop/legal-kepatuhan/README.md).
4. Perubahan: edit berkas SOP terkait; hook sinkronisasi akan memicu pembaruan spec agar keterlacakan tetap konsisten.

## Status & Catatan

- Beberapa butir menandai `> [TODO]` yang membutuhkan konfirmasi (mis. harga Premium+, batas fair use, kewajiban UU PDP, prosedur takedown resmi X, nilai palet warna brand). Tinjau butir hukum bersama penasihat hukum sebelum diberlakukan.
- Dokumen legal bukan nasihat hukum.

> Catatan lokasi: spec (`design.md`/`tasks.md`) mencatat root output SOP sebagai `.kiro/specs/sop-akun-quotes-x/sop/`, sedangkan berkas nyata berada di `sop/` pada root repositori. Selaraskan bila diperlukan.
