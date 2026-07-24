# Implementation Plan: Penyusunan Dokumen SOP Akun Quotes X

## Overview

Rencana ini memecah penyusunan **dokumen SOP** (bukan perangkat lunak) menjadi langkah-langkah penulisan yang inkremental. Keluaran akhir adalah berkas Markdown di `.kiro/specs/sop-akun-quotes-x/sop/` sesuai "Rencana Output File SOP Final" pada design:

```
sop/
├─ README.md                  # Indeks utama deliverable SOP
├─ operasional-konten/        # SOP operasional konten (Bagian 0–11) & lampiran
│  ├─ README.md               # Indeks & ringkasan folder operasional konten
│  ├─ SOP-Akun-Quotes-X.md    # Dokumen master (Bagian 0–11)
│  ├─ lampiran-template.md     # Template postingan, klarifikasi, log pembelajaran
│  ├─ lampiran-checklist.md    # Checklist pra-posting, moderasi, keamanan
│  ├─ lampiran-contoh.md       # Minimal 3 contoh format postingan
│  ├─ lampiran-monetisasi-x.md # Peraturan boleh & tidak boleh monetisasi (acuan Content Monetization Standards X)
│  └─ panduan-brand-identitas.md # Identitas verbal, visual, bio, konsistensi/Template_Baku, do & don't visual (SOP-BR.1–BR.5, R15.1–R15.5)
├─ operasional-bisnis/         # Folder ketentuan bisnis antar-Founder (R12)
│  ├─ README.md                # Indeks & ringkasan folder, hubungan ke SOP konten
│  ├─ modal-dan-bagi-hasil.md  # Modal awal 6× Premium+, dana cadangan 12×, waterfall bagi hasil (SOP-B.1–B.5, R12.1–R12.5)
│  └─ ketentuan-bisnis.md      # Kepemilikan, peran Founder, pengeluaran, pencatatan, tata kelola/sengketa (SOP-B.6–B.10, R12.6–R12.10)
└─ legal-kepatuhan/            # Folder kebijakan legal, kepatuhan & AI (R13, R14)
   ├─ README.md                # Indeks & ringkasan folder legal & kepatuhan (SOP-L, SOP-AI)
   ├─ kebijakan-hak-cipta-privasi.md # Hak cipta & fair use, klaim/takedown, data pribadi/UU PDP, disclosure iklan, disclaimer (SOP-L.1–L.5, R13.1–R13.5)
   └─ kebijakan-penggunaan-ai.md # Ruang lingkup AI, verifikasi wajib, larangan, keaslian/tanggung jawab manusia, privasi data pada alat AI (SOP-AI.1–AI.5, R14.1–R14.5)
```

Setiap tugas menulis/menyusun bagian dokumen SOP dan lampirannya, membangun secara bertahap di atas tugas sebelumnya, dan diakhiri dengan review verifikasi yang menyatukan seluruh dokumen. Konvensi yang ditegakkan di setiap aturan: ID stabil `SOP-N.x`, anotasi keterlacakan `(Requirement R{n}.{m})`, dan penanda ketidaklengkapan `> [TODO: ...]` bila bagian belum lengkap (R1.5).

> Catatan verifikasi: sesuai Testing Strategy pada design, korektnessnya bersifat kelengkapan/konsistensi/keterlacakan dokumen. Karena itu tidak ada property-based testing otomatis; verifikasi dilakukan melalui **review/checklist manusia** (presence review, consistency & traceability review, dan property review atas 30 correctness properties).

## Tasks

- [x] 1. Siapkan struktur folder, kerangka dokumen, dan kontrol dokumen
  - [x] 1.1 Buat struktur folder `sop/` (root `README.md`, `operasional-konten/`, `operasional-konten/README.md`) dan kerangka (skeleton) semua berkas
    - Buat `sop/operasional-konten/SOP-Akun-Quotes-X.md` dengan heading level 1 judul dokumen dan kerangka heading level 2 untuk `## Bagian 0` s.d. `## Bagian 11` sesuai pemetaan struktur pada design
    - Buat kerangka `sop/operasional-konten/lampiran-template.md`, `sop/operasional-konten/lampiran-checklist.md`, dan `sop/operasional-konten/lampiran-contoh.md` dengan judul dan heading kosong
    - Sisipkan penanda `> [TODO: ...]` pada setiap bagian yang belum diisi sebagai dasar penegakan penanda ketidaklengkapan (R1.5)
    - Tetapkan konvensi penomoran heading, ID aturan `SOP-N.x`, dan anotasi `(Requirement R{n}.{m})` di catatan pembuka dokumen master
    - _Requirements: 1.2_

  - [x] 1.2 Tulis Bagian 0: Metadata & Kontrol Dokumen (dokumen master)
    - Tulis header dokumen: Nomor Versi (mis. `v1.0.0`), Tanggal Berlaku, dan Pihak yang Menyetujui (Admin_Utama)
    - Buat tabel Riwayat Perubahan dengan kolom: Tanggal, Versi, Ringkasan Perubahan, Penanggung Jawab Revisi
    - Tulis aturan bahwa revisi boleh disimpan meski riwayat perubahan belum lengkap, sekaligus mewajibkan penanda ketidaklengkapan `> [TODO]` selalu ditegakkan pada bagian yang belum selesai
    - _Requirements: 1.3, 1.4, 1.5_

- [x] 2. Tulis bagian inti dokumen master (Bagian 1–6)
  - [x] 2.1 Tulis Bagian 1: Tujuan, Ruang Lingkup, Definisi Istilah, dan Peran
    - Tulis tujuan project (kelayakan & optimasi sharing revenue berlandaskan nilai moral), ruang lingkup, dan glosarium (adopsi Glossary requirements)
    - Tulis daftar bagian wajib SOP sebagai daftar isi kontraktual (kriteria konten, styleguide, following, interaksi/komentar, moderasi, eskalasi krisis, keamanan, jadwal, metrik)
    - Tulis matriks peran & wewenang (Pengelola vs Admin_Utama) sebagai antarmuka bersama yang dirujuk seluruh bagian
    - _Requirements: 1.1, 1.2_

  - [x] 2.2 Tulis Bagian 2: Kriteria Konten & Quotes yang Diposting
    - Tulis definisi nilai moral dan larangan mutlak (ujaran kebencian, diskriminasi SARA, pornografi) sebagai single source of truth (R2.1)
    - Tulis tabel dua kolom tema diizinkan vs tema dilarang (R2.2); gerbang persetujuan Admin_Utama untuk topik politik/agama/isu sensitif (R2.3)
    - Tulis aturan penolakan pra-posting (REJECTED) untuk Quotes yang gagal kriteria (R2.4) dan prosedur penghapusan pascapublikasi (REMOVED) dengan batas waktu eksplisit (R2.5)
    - Tulis batas panjang karakter selaras batas Platform_X (R2.6) dan gerbang persetujuan wajib berbasis lifecycle status Quotes DRAFT→PENDING→APPROVED→POSTED (R2.7)
    - _Requirements: 2.1, 2.2, 2.3, 2.4, 2.5, 2.6, 2.7_

  - [x] 2.3 Tulis Bagian 3: Verifikasi Sumber & Atribusi Kutipan
    - Tulis aturan verifikasi tokoh bernama (min. dua rujukan tepercaya sebelum posting) (R3.1) dan atribusi sumber anonim/tradisi (R3.2)
    - Tulis aturan penundaan status PENDING untuk sumber tak terverifikasi (R3.3) dan penghormatan hak cipta (R3.4)
    - Tulis kewajiban atribusi tercantum pada setiap postingan, termasuk label anonim (R3.5)
    - Tulis aturan Kategori_Sumber_Perolehan (metadata internal): original / website-media sosial / AI, dicatat untuk audit; tiap kategori memicu pemeriksaan sesuai (verifikasi R3.1, hak cipta R3.4, kebijakan AI Requirement 14) (SOP-3.6, R3.6)
    - Sertakan/rujuk diagram Alur Verifikasi Sumber & Atribusi dari design
    - _Requirements: 3.1, 3.2, 3.3, 3.4, 3.5, 3.6_

  - [x] 2.4 Tulis Bagian 4: Format Penulisan & Tata Bahasa (Styleguide)
    - Tulis aturan ejaan baku PUEBI (R4.1); tanda baca, huruf kapital, format kutipan/pemisah atribusi (R4.2)
    - Tulis aturan Inisial_Admin penanggung jawab pada akhir baris atribusi, dipisah koma dari Atribusi sumber tanpa menggantikannya (SOP-4.3, R4.3)
    - Tulis aturan tagar minimum 1 maksimum 5 per postingan beserta daftar tagar baku (R4.4) dan tone of voice moral/sopan/reflektif (R4.5)
    - Tulis kebijakan terjemahan sebagai kebijakan umum yang selalu ada (R4.6); rujuk ke Lampiran untuk ≥3 contoh format (R4.7)
    - Tulis gerbang bahasa asing: blokir posting Quotes berbahasa asing selama aturan terjemahan belum ditetapkan (R4.8)
    - _Requirements: 4.1, 4.2, 4.3, 4.4, 4.5, 4.6, 4.7, 4.8_

  - [x] 2.5 Tulis Bagian 5: Kriteria Akun yang Diikuti (Following)
    - Tulis syarat simultan following (relevansi tema DAN reputasi positif DAN kesesuaian nilai moral) (R5.1) dan daftar kategori akun dilarang diikuti (R5.2)
    - Tulis aturan peninjauan Admin_Utama untuk kandidat berisu komentar (R5.3) dan fail-safe pemblokiran following bila proses peninjauan belum tersedia (R5.4)
    - Tulis aturan peninjauan ulang & opsi unfollow (R5.5) dan frekuensi peninjauan berkala daftar Following (R5.6)
    - Rujuk status Following (CANDIDATE/UNDER_REVIEW/BLOCKED/FOLLOWED/UNFOLLOWED) dari design
    - _Requirements: 5.1, 5.2, 5.3, 5.4, 5.5, 5.6_

  - [x] 2.6 Tulis Bagian 6: Kriteria Isi Komentar & Interaksi
    - Tulis kriteria komentar diperbolehkan (logika OR: sopan / relevan / mendukung nilai moral) dan aturan larangan bila tidak satu pun terpenuhi (R6.1)
    - Tulis klasifikasi komentar dilarang: provokatif, ujaran kebencian, perdebatan SARA (R6.2)
    - Tulis aturan balasan mengikuti Styleguide & nada sopan (R6.3), larangan balasan emosional + ikuti moderasi (R6.4)
    - Tulis aturan interaksi keluar hanya pada konten selaras nilai moral (R6.5)
    - Tulis aturan frekuensi keterlibatan minimum: minimum 10 balasan/komentar per hari tanpa batas maksimum pada akun berpengaruh (pengikut tinggi atau impressions tinggi), tiap balasan mematuhi gerbang nilai moral (R6.5) & Styleguide/nada sopan (R6.3) guna mendukung Program_Sharing_Revenue (SOP-6.6, R6.6)
    - Tulis aturan opini pribadi orisinal kontekstual pada setiap balasan di akun berpengaruh sebagai mitigasi spam — bukan templat, ucapan generik, tempelan kutipan tanpa tanggapan, maupun balasan seragam massal (SOP-6.6, R6.7)
    - _Requirements: 6.1, 6.2, 6.3, 6.4, 6.5, 6.6, 6.7_

- [x] 3. Checkpoint - Tinjau kelengkapan Bagian 0–6
  - Ensure all tests pass, ask the user if questions arise.

- [x] 4. Tulis bagian operasional dokumen master (Bagian 7–11)
  - [x] 4.1 Tulis Bagian 7: Moderasi Komentar
    - Tulis kriteria komentar wajib disembunyikan/dihapus (spam, ujaran kebencian, tautan berbahaya) (R7.1)
    - Tulis langkah tindakan (sembunyikan/hapus/blokir) yang dieksekusi manual oleh Pengelola (R7.2)
    - Tulis daftar kata kunci sensitif yang dipantau (R7.3) dan frekuensi pemeriksaan kolom komentar (R7.4)
    - Tulis aturan eskalasi area abu-abu ke Admin_Utama, dengan catatan kelonggaran bila seluruh kasus jelas (R7.5)
    - _Requirements: 7.1, 7.2, 7.3, 7.4, 7.5_

  - [x] 4.2 Tulis Bagian 8: Prosedur Eskalasi Krisis
    - Tulis definisi & level Krisis (K1/K2/K3) beserta indikator per level (R8.1) dan langkah tanggap awal + batas waktu respons per level (R8.2)
    - Tulis urutan eskalasi & penanggung jawab per level (R8.3) dan kriteria keputusan hapus/edit/pertahankan konten sumber krisis (R8.4)
    - Tulis aturan penyusunan & persetujuan klarifikasi/permintaan maaf sebelum publikasi (R8.5) dan evaluasi pascakrisis + pencatatan pembelajaran (R8.6)
    - Sertakan/rujuk diagram Alur Eskalasi Krisis Bertingkat dari design
    - _Requirements: 8.1, 8.2, 8.3, 8.4, 8.5, 8.6_

  - [x] 4.3 Tulis Bagian 9: Jadwal Posting & Kalender Konten
    - Tulis frekuensi posting harian minimum 10 postingan per hari tanpa batas maksimum, dan setiap postingan yang dihitung wajib berstatus APPROVED sebelum diposting (R9.1); rentang jam posting yang direkomendasikan (R9.2)
    - Tulis aturan penggunaan Kalender_Konten merencanakan Quotes minimal satu minggu ke depan (R9.3)
    - Tulis fallback konten cadangan disetujui bila slot tak terisi terverifikasi (R9.4) dan fallback kedua: kosongkan slot & lewati posting bila tak ada keduanya (R9.5)
    - Tulis aturan pengelompokan thread (utas): Quotes bertema sama/terkait diterbitkan sebagai satu utas — bukan postingan terpisah beruntun dalam jendela waktu singkat — sebagai mitigasi spam; postingan pembuka utas dimulai dengan kalimat/paragraf pembuka yang disesuaikan dengan tema Quotes di dalam utas (memperkenalkan tema, patuh Styleguide/nada R4.5 & batas maksimum karakter R2.6); tiap Quotes dalam utas tetap patuh format posting (Atribusi, Inisial_Admin, batas tagar) & berstatus APPROVED, penomoran utas (mis. 1/n) direkomendasikan (SOP-9.1, R9.6)
    - _Requirements: 9.1, 9.2, 9.3, 9.4, 9.5, 9.6_

  - [x] 4.4 Tulis Bagian 10: Metrik & Kelayakan Program Sharing Revenue
    - Tulis syarat kelayakan Program_Sharing_Revenue Platform_X (R10.1) dan daftar Metrik_Kelayakan yang dipantau (pengikut, impressions, engagement) (R10.2)
    - Tulis frekuensi peninjauan & pelaporan metrik (R10.3) dan trigger tindakan perbaikan saat metrik di bawah ambang, termasuk kondisi zero activity (R10.4)
    - Tulis fail-safe pengawasan manual bila trigger otomatis gagal aktif (R10.5) dan kepatuhan kebijakan monetisasi Platform_X (R10.6)
    - Rujuk lampiran monetisasi khusus (`operasional-konten/lampiran-monetisasi-x.md`) yang menetapkan konten & perilaku akun yang diperbolehkan dan dilarang, mengacu Content Monetization Standards X (R10.7)
    - _Requirements: 10.1, 10.2, 10.3, 10.4, 10.5, 10.6, 10.7_

  - [x] 4.5 Tulis Bagian 11: Keamanan Akun
    - Tulis aturan wajib 2FA (R11.1) dan kebijakan kata sandi: kompleksitas minimum & frekuensi pembaruan (R11.2)
    - Tulis kelonggaran tahap penyiapan awal (akun/kata sandi sementara sebelum kebijakan penuh) (R11.3) dan daftar Pengelola berikut tingkat wewenang (R11.4)
    - Tulis aturan pencabutan akses saat Pengelola berhenti dalam batas waktu + kepatuhan bukti pencabutan (R11.5) dan langkah tanggap keamanan saat akses tidak sah terdeteksi (R11.6)
    - _Requirements: 11.1, 11.2, 11.3, 11.4, 11.5, 11.6_

- [x] 5. Checkpoint - Tinjau kelengkapan Bagian 7–11
  - Ensure all tests pass, ask the user if questions arise.

- [x] 6. Susun lampiran modular SOP
  - [x] 6.1 Tulis `operasional-konten/lampiran-template.md`
    - Tulis Template Format Postingan Quotes (acuan R4.6)
    - Tulis Template Klarifikasi/Permintaan Maaf Krisis dengan baris persetujuan Admin_Utama (acuan R8.5)
    - Tulis Template Pencatatan Pembelajaran Pascakrisis (tabel field) yang merujuk ID `SOP-N.x` (acuan R8.6)
    - _Requirements: 4.6, 8.5, 8.6_

  - [x] 6.2 Tulis `operasional-konten/lampiran-checklist.md`
    - Tulis Checklist Pra-Posting yang mencakup nilai moral, tema, sensitif, verifikasi sumber, atribusi, inisial admin, hak cipta, panjang karakter, styleguide/tagar, dan status APPROVED (acuan R2, R3, R4)
    - Tulis Checklist Moderasi (kriteria sembunyikan/hapus/blokir, kata kunci sensitif, frekuensi pemeriksaan) (acuan R7)
    - Tulis Checklist Keamanan (2FA, kebijakan kata sandi, daftar akses & wewenang, pencabutan akses) (acuan R11)
    - _Requirements: 2.1, 2.2, 2.3, 2.6, 2.7, 3.1, 3.2, 3.3, 3.4, 3.5, 4.1, 4.2, 4.3, 4.4, 7.1, 7.3, 7.4, 11.1, 11.2, 11.4, 11.5_

  - [x] 6.3 Tulis `operasional-konten/lampiran-contoh.md`
    - Tulis minimal tiga contoh format postingan benar: (1) kutipan tokoh bernama terverifikasi, (2) kutipan anonim, (3) kutipan tradisi/peradaban
    - Pastikan setiap contoh mematuhi atribusi tercantum, Inisial_Admin, dan batas 1–5 tagar (R4.7)
    - Tulis contoh format thread/utas untuk Quotes bertema sama/terkait dengan penomoran 1/n, termasuk paragraf pembuka yang disesuaikan dengan tema utas pada postingan pembuka (R9.6)
    - Tulis contoh balasan pada akun berpengaruh yang memuat opini pribadi orisinal kontekstual (R6.7)
    - _Requirements: 4.7, 6.7, 9.6_

  - [x] 6.4 Tulis `operasional-konten/lampiran-monetisasi-x.md`
    - Tulis Peraturan Boleh & Tidak Boleh Monetisasi (acuan Content Monetization Standards X): prasyarat kelayakan, kategori konten diperbolehkan, kategori konten dilarang, dan perilaku manipulasi platform yang dilarang (SOP-M.1–SOP-M.5)
    - _Requirements: 10.6, 10.7_

  - [x] 6.5 Tulis `operasional-konten/panduan-brand-identitas.md`
    - Tulis Identitas_Verbal: nama tampil, @handle, tagline, dan persona suara konsisten dengan nada komunikasi/tone of voice (R4.5) (SOP-BR.1, R15.1)
    - Tulis Identitas_Visual: avatar, banner, palet warna dengan kontras aksesibel, tipografi, dan gaya kartu kutipan (SOP-BR.2, R15.2)
    - Tulis isi Bio_Profil: identitas singkat, nilai/tema, Disclaimer ringkas, dan tautan resmi, serta tidak menyesatkan (SOP-BR.3, R15.3)
    - Tulis kewajiban konsistensi Identitas_Verbal & Identitas_Visual pada seluruh materi serta penggunaan Template_Baku; perubahan identitas dicatat melalui kontrol dokumen Bagian 0 (SOP-BR.4, R15.4)
    - Tulis panduan do & don't visual: batasan keterbacaan/kontras serta pencantuman Atribusi dan Inisial_Admin pada kartu kutipan (selaras R3.5, R4.3) (SOP-BR.5, R15.5)
    - _Requirements: 15.1, 15.2, 15.3, 15.4, 15.5_

- [x] 7. Verifikasi akhir dokumen SOP (review/checklist manusia)
  - [x]* 7.1 Presence review (checklist kelengkapan dokumen)
    - Verifikasi keberadaan seluruh bagian wajib, daftar, header versi/tanggal/penyetuju, tabel riwayat perubahan, dan contoh format (≥3)
    - Tandai item yang belum lengkap dengan `> [TODO]` alih-alih membiarkannya hilang (R1.5)
    - Cakupan presence: R1.1–1.3, R2.2, R4.2, R4.4, R4.5, R4.6, R5.2, R5.6, R7.1, R7.3, R7.4, R8.1, R8.4, R9.1, R9.2, R10.1, R10.2, R10.3, R10.6, R11.1, R11.2, R11.4
    - _Requirements: 1.1, 1.2, 1.3_

  - [x]* 7.2 Consistency & traceability review
    - Verifikasi setiap aturan memiliki ID `SOP-N.x` dan anotasi `(Requirement R{n}.{m})`
    - Verifikasi tidak ada requirement tanpa aturan dan tidak ada kontradiksi antaraturan (definisi nilai moral tunggal dirujuk konsisten)
    - Verifikasi seluruh 12 requirement terpetakan ke minimal satu bagian/aturan (keterlacakan penuh)
    - _Requirements: 1.2, 1.4, 1.5_

  - [x]* 7.3 Property review (pemetaan 30 correctness properties)
    - Telusuri teks SOP untuk memastikan setiap properti menjadi invarian yang ditegakkan dokumen/prosedur (review manusia, bukan PBT otomatis)
    - **Property 1: Kelengkapan lifecycle persetujuan sebelum tayang** — Validates: R2.3, 2.7, 3.1, 3.3
    - **Property 2: Setiap postingan memiliki atribusi valid berikut inisial penanggung jawab** — Validates: R3.2, 3.5, 4.3
    - **Property 3: Konten gagal kriteria tidak pernah tayang permanen** — Validates: R2.4, 2.5
    - **Property 4: Batas panjang karakter dipatuhi** — Validates: R2.6
    - **Property 5: Batas jumlah tagar dipatuhi** — Validates: R4.4
    - **Property 6: Gerbang bahasa asing saat aturan terjemahan absen** — Validates: R4.6, 4.8
    - **Property 7: Semua akun yang diikuti memenuhi syarat simultan** — Validates: R5.1, 5.3, 5.4
    - **Property 8: Klasifikasi komentar konsisten dengan aturan** — Validates: R6.1, 6.2
    - **Property 9: Interaksi keluar & balasan selaras nilai moral serta Styleguide** — Validates: R6.3, 6.5
    - **Property 10: Setiap komentar pelanggar ditindak secara manual** — Validates: R7.1, 7.2
    - **Property 11: Setiap level krisis memiliki penanganan lengkap** — Validates: R8.1, 8.2, 8.3
    - **Property 12: Pernyataan publik krisis selalu disetujui sebelum terbit** — Validates: R8.5
    - **Property 13: Setiap krisis selesai menghasilkan catatan pembelajaran** — Validates: R8.6
    - **Property 14: Kalender konten selalu terisi minimal satu minggu** — Validates: R9.3, 9.4, 9.5
    - **Property 15: Metrik di bawah ambang selalu memicu tindakan** — Validates: R10.4, 10.5
    - **Property 16: Setiap penandaan ketidaklengkapan ditegakkan lintas revisi** — Validates: R1.4, 1.5
    - **Property 17: Pencabutan akses tepat waktu saat offboarding** — Validates: R11.5
    - **Property 18: Frekuensi keterlibatan minimum pada akun berpengaruh** — Validates: R6.6
    - **Property 19: Balasan pada akun berpengaruh memuat opini orisinal kontekstual** — Validates: R6.7
    - **Property 20: Quotes bertema sama disajikan sebagai satu thread** — Validates: R9.6
    - **Property 21: Cakupan konten/perilaku monetisasi ditetapkan boleh atau dilarang** — Validates: R10.7
    - **Property 22: Alokasi bagi hasil sesuai fase status cadangan** — Validates: R12.4
    - **Property 23: Cadangan tidak melampaui target dan langganan dibayar dari cadangan** — Validates: R12.3, 12.5
    - **Property 24: Keputusan finansial material dan pemindahtanganan aset memerlukan persetujuan Founder dan Co-Founder** — Validates: R12.2, 12.6, 12.8
    - **Property 25: Kepatuhan hak cipta & penanganan klaim** — Validates: R13.1, R13.2
    - **Property 26: Perlindungan data & keterbukaan komersial** — Validates: R13.3, R13.4
    - **Property 27: Konten ber-AI tetap terverifikasi & tidak difabrikasi** — Validates: R14.2, R14.3
    - **Property 28: Konsistensi identitas brand** — Validates: R15.1, R15.2, R15.4
    - **Property 29: Kategori sumber perolehan diklasifikasikan & diperiksa** — Validates: R3.6
    - **Property 30: Komitmen & kontribusi Founder/Co-Founder ditetapkan, ditinjau, dan ditindaklanjuti** — Validates: R12.11, R12.12, R12.13, R12.14
    - _Requirements: 1.4, 1.5, 2.3, 2.4, 2.5, 2.6, 2.7, 3.1, 3.2, 3.3, 3.6, 4.3, 4.4, 4.6, 4.8, 5.1, 5.3, 5.4, 6.1, 6.2, 6.3, 6.5, 6.6, 6.7, 7.1, 7.2, 8.1, 8.2, 8.3, 8.5, 8.6, 9.3, 9.4, 9.5, 9.6, 10.4, 10.5, 10.7, 11.5, 12.2, 12.3, 12.4, 12.5, 12.6, 12.8, 12.11, 12.12, 12.13, 12.14, 13.1, 13.2, 13.3, 13.4, 14.2, 14.3, 15.1, 15.2, 15.4_

- [x] 9. Susun folder `operasional-bisnis/` (ketentuan bisnis antar-Founder)
  - [x] 9.1 Tulis `operasional-bisnis/README.md`
    - Tulis indeks & ringkasan folder `operasional-bisnis/` beserta hubungannya ke SOP konten (Bagian 0–11) dan tautan ke `modal-dan-bagi-hasil.md` serta `ketentuan-bisnis.md`
    - Tegaskan folder tetap tunduk pada kontrol dokumen (Bagian 0) dan memakai konvensi ID `SOP-B.x`
    - _Requirements: 12.1_

  - [x] 9.2 Tulis `operasional-bisnis/modal-dan-bagi-hasil.md`
    - Tulis Modal_Awal sebesar 6× Biaya_Langganan Premium+ yang disediakan bersama Founder dan Co-Founder (SOP-B.1, R12.1)
    - Tulis struktur satu Founder + satu Co-Founder, kepemilikan 70:30, namun bagi hasil waterfall tetap setara 50:50 (R12.2) dan pemeliharaan Dana_Cadangan_Langganan dengan target akumulasi 12× Biaya_Langganan (runway 12 periode) (R12.3)
    - Tulis sistem bagi hasil waterfall berbasis status fase cadangan: Fase 1 (BELUM_PENUH, <12×) 50% ke cadangan & 50% dibagi rata setara antara Founder dan Co-Founder; Fase 2 (PENUH, ≥12×) 100% dibagi rata setara antara Founder dan Co-Founder; periode transisi hanya menyisihkan kekurangan menuju 12× tanpa melampaui target (R12.4)
    - Tulis distribusi berkala disertai pencatatan & transparansi keuangan bagi Founder dan Co-Founder dan pembayaran langganan tepat waktu untuk menjaga kelayakan monetisasi (R12.5)
    - _Requirements: 12.1, 12.2, 12.3, 12.4, 12.5_

  - [x] 9.3 Tulis `operasional-bisnis/ketentuan-bisnis.md`
    - Tulis kepemilikan bersama Akun_Quotes & aset terkait (termasuk Dana_Cadangan_Langganan) sesuai Kepemilikan_Ekuitas 70:30; pemindahtanganan aset wajib disetujui Founder dan Co-Founder (R12.6)
    - Tulis peran operasional Founder selaras Matriks Peran & Wewenang (SOP-1.6), sekurang-kurangnya satu Founder berperan Admin_Utama (R12.7)
    - Tulis kewajiban persetujuan Founder dan Co-Founder atas pengeluaran di luar Biaya_Langganan sebelum dibelanjakan beserta pencatatannya (R12.8)
    - Tulis pemeliharaan catatan keuangan (pemasukan, pengeluaran, saldo cadangan, distribusi) & pelaporan berkala yang dapat diakses Founder dan Co-Founder (R12.9)
    - Tulis tata kelola perubahan kesepakatan, penyelesaian sengketa, dan keluarnya Founder, termasuk pencabutan akses selaras R11.5 (R12.10)
    - Tulis komitmen waktu minimum Founder & Co-Founder (default Founder ≥7 jam/mgg, Co-Founder ≥5 jam/mgg; ≥1 pihak aktif tiap hari; alasan wajar dikecualikan) (SOP-B.11, R12.11)
    - Tulis matriks pembagian peran Founder vs Co-Founder (penanggung jawab utama & cadangan per area, selaras SOP-1.6) (SOP-B.12, R12.12)
    - Tulis tinjauan kontribusi berkala berbasis data terukur bersama pelaporan keuangan (SOP-B.13, R12.13)
    - Tulis konsekuensi bertingkat bila kontribusi tak terpenuhi: klarifikasi → rencana perbaikan → redistribusi → penyesuaian bagi hasil/kepemilikan (persetujuan kedua pihak, opsi vesting) → exit (SOP-B.14, R12.14)
    - _Requirements: 12.6, 12.7, 12.8, 12.9, 12.10, 12.11, 12.12, 12.13, 12.14_

- [x] 11. Susun folder `legal-kepatuhan/` (kebijakan legal, kepatuhan & AI)
  - [x] 11.1 Tulis `legal-kepatuhan/README.md`
    - Tulis indeks & ringkasan folder `legal-kepatuhan/` beserta tautan ke `kebijakan-hak-cipta-privasi.md` dan `kebijakan-penggunaan-ai.md`
    - Tegaskan folder tetap tunduk pada kontrol dokumen (Bagian 0) dan memakai konvensi ID `SOP-L.x` serta `SOP-AI.x`
    - _Requirements: 13.1_

  - [x] 11.2 Tulis `legal-kepatuhan/kebijakan-hak-cipta-privasi.md`
    - Tulis aturan hak cipta & Penggunaan_Wajar (fair use): larangan penyalinan substansial tanpa izin, pengutamaan sumber domain publik/berlisensi, bukti lisensi aset gambar, fail-safe menahan konten bila status meragukan (SOP-L.1, R13.1)
    - Tulis prosedur penanganan klaim/Takedown: penilaian klaim, penurunan/penyuntingan bila berdasar, pendokumentasian, kanal resmi Platform_X (SOP-L.2, R13.2)
    - Tulis perlindungan data pribadi selaras UU_PDP: minimalisasi data, larangan Doxxing, kerahasiaan DM, penanganan permintaan subjek data (SOP-L.3, R13.3)
    - Tulis disclosure iklan/Konten_Berbayar: pengungkapan jelas hubungan komersial disertai kejujuran, tetap selaras Nilai_Moral (SOP-L.4, R13.4)
    - Tulis Disclaimer: Quotes bukan nasihat profesional, penghormatan tokoh tanpa endorsement, larangan memotong kutipan hingga menyesatkan (SOP-L.5, R13.5)
    - _Requirements: 13.1, 13.2, 13.3, 13.4, 13.5_

  - [x] 11.3 Tulis `legal-kepatuhan/kebijakan-penggunaan-ai.md`
    - Tulis ruang lingkup penggunaan AI yang diperbolehkan: ide/kurasi tema, penyuntingan bahasa, draf teks pendukung yang wajib disunting manusia, riset awal; AI bukan pengganti penilaian manusia (SOP-AI.1, R14.1)
    - Tulis verifikasi wajib: Quotes/Atribusi berbantuan AI wajib verifikasi manusia ≥2 rujukan tepercaya sebelum tayang; AI bukan satu-satunya sumber (penegakan R3.1, R3.3) (SOP-AI.2, R14.2)
    - Tulis larangan: fabrikasi kutipan/Atribusi, konten menyesatkan/media manipulatif, pelanggaran hak cipta, manipulasi keterlibatan (SOP-AI.3, R14.3)
    - Tulis keaslian & tanggung jawab manusia: tanggung jawab akhir pada manusia, suara akun sesuai persona, keterbukaan penandaan konten ber-AI selaras keaslian Platform_X (SOP-AI.4, R14.4)
    - Tulis privasi data pada alat AI: larangan memasukkan data pribadi/sensitif ke alat AI pihak ketiga (selaras R13.3 & Requirement 11) (SOP-AI.5, R14.5)
    - _Requirements: 14.1, 14.2, 14.3, 14.4, 14.5_

- [ ] 12. Checkpoint akhir - Pastikan Definition of Done SOP terpenuhi
  - Ensure all tests pass, ask the user if questions arise.

## Notes

- Ini adalah project **dokumentasi/SOP**, bukan software. Seluruh tugas adalah aktivitas menulis/menyusun dokumen Markdown.
- Tugas bertanda `*` bersifat opsional (review/verifikasi) dan dapat dilewati untuk draf cepat, tetapi disarankan untuk mencapai Definition of Done.
- Setiap tugas merujuk klausa requirement spesifik untuk keterlacakan.
- Verifikasi menggunakan review/checklist manusia (presence, consistency & traceability, property review) — bukan property-based testing otomatis, sesuai Testing Strategy pada design.
- Bagian 1–11 ditulis ke dokumen master yang sama sehingga dijadwalkan pada wave berbeda agar tidak terjadi konflik penyuntingan berkas.

## Task Dependency Graph

```json
{
  "waves": [
    { "id": 0, "tasks": ["1.1"] },
    { "id": 1, "tasks": ["1.2", "6.1", "6.2", "6.3", "6.4", "6.5"] },
    { "id": 2, "tasks": ["2.1"] },
    { "id": 3, "tasks": ["2.2"] },
    { "id": 4, "tasks": ["2.3"] },
    { "id": 5, "tasks": ["2.4"] },
    { "id": 6, "tasks": ["2.5"] },
    { "id": 7, "tasks": ["2.6"] },
    { "id": 8, "tasks": ["4.1"] },
    { "id": 9, "tasks": ["4.2"] },
    { "id": 10, "tasks": ["4.3"] },
    { "id": 11, "tasks": ["4.4"] },
    { "id": 12, "tasks": ["4.5"] },
    { "id": 13, "tasks": ["9.1", "9.2", "9.3"] },
    { "id": 14, "tasks": ["11.1", "11.2", "11.3"] },
    { "id": 15, "tasks": ["7.1", "7.2", "7.3"] }
  ]
}
```
