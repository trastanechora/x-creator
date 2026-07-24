# Requirements Document

## Introduction

Dokumen ini memuat kebutuhan (requirements) untuk penyusunan **Standar Operasional Prosedur (SOP)** sebuah project akun media sosial di platform X. Akun ini berfokus pada konten Kata Kutipan (Quotes) yang bersumber dari tokoh, literasi peradaban atau bangsa, maupun sumber anonim, dengan prinsip dasar konten yang berlandaskan **nilai moral**. Tujuan utama project adalah memenuhi syarat dan mengoptimalkan partisipasi dalam program **sharing revenue** (bagi hasil pendapatan) yang disediakan platform X.

SOP yang dihasilkan berfungsi sebagai pedoman operasional harian bagi pengelola akun agar konten, interaksi, moderasi, keamanan, dan penanganan krisis dilakukan secara konsisten, terukur, dan sesuai nilai moral yang dijunjung. Requirements dalam dokumen ini berfokus pada **isi dan aturan SOP**, bukan pada pembangunan perangkat lunak.

Setiap kriteria penerimaan (acceptance criteria) menggunakan pola EARS dan ditulis agar dapat diverifikasi. Frasa "SOP SHALL memuat" berarti dokumen SOP final wajib memuat ketentuan tersebut.

## Glossary

- **SOP**: Dokumen Standar Operasional Prosedur yang menjadi keluaran akhir dari spec ini, memuat seluruh aturan pengelolaan akun.
- **Akun_Quotes**: Akun media sosial di platform X yang menjadi objek pengelolaan, berfokus pada konten kutipan bernilai moral.
- **Platform_X**: Platform media sosial tempat Akun_Quotes beroperasi dan mengikuti program sharing revenue.
- **Program_Sharing_Revenue**: Program bagi hasil pendapatan dari Platform_X yang menjadi tujuan monetisasi Akun_Quotes.
- **Pengelola**: Orang atau tim yang bertanggung jawab menjalankan operasional Akun_Quotes berdasarkan SOP.
- **Admin_Utama**: Pengelola dengan wewenang tertinggi yang bertanggung jawab atas keputusan strategis, keamanan akun, dan eskalasi krisis.
- **Quotes**: Konten utama berupa kutipan kata bernilai moral yang diposting oleh Akun_Quotes.
- **Sumber_Kutipan**: Asal-usul sebuah Quotes, dapat berupa tokoh bernama, karya literasi, tradisi peradaban/bangsa, atau anonim.
- **Atribusi**: Pencantuman Sumber_Kutipan pada sebuah Quotes.
- **Kategori_Sumber_Perolehan**: Klasifikasi internal sebuah Quotes berdasarkan cara/asal materi diperoleh — (a) karangan sendiri/original, (b) website/media sosial, atau (c) AI — yang dicatat sebagai metadata untuk audit dan menentukan pemeriksaan tambahan; berbeda dari jenis Sumber_Kutipan (tokoh/anonim/tradisi).
- **Inisial_Admin**: Inisial Pengelola/Admin_Utama penanggung jawab yang dicantumkan pada akhir baris atribusi setiap postingan sebagai penanda akuntabilitas.
- **Styleguide**: Panduan format penulisan dan tata bahasa untuk seluruh konten dan interaksi Akun_Quotes.
- **Interaksi**: Aktivitas komentar, balasan, repost, like, dan mention yang dilakukan Akun_Quotes terhadap konten atau pengguna lain.
- **Following**: Daftar akun lain yang diikuti oleh Akun_Quotes.
- **Blunder**: Kesalahan konten atau interaksi yang berpotensi menimbulkan reaksi negatif publik atau merusak reputasi Akun_Quotes.
- **Krisis**: Situasi eskalasi reaksi negatif publik akibat Blunder yang memerlukan penanganan khusus.
- **Prosedur_Eskalasi**: Rangkaian langkah penanganan Krisis yang terdefinisi dalam SOP.
- **Kalender_Konten**: Jadwal terencana berisi rencana posting Quotes beserta waktu tayang.
- **Metrik_Kelayakan**: Indikator kinerja yang menjadi syarat kelayakan dan optimasi Program_Sharing_Revenue.
- **Founder**: Orang yang mendirikan dan memimpin project Akun_Quotes; memegang 70% kepemilikan (ekuitas). Berbeda dari peran operasional Pengelola/Admin_Utama.
- **Co-Founder**: Rekan Founder (co-founding partner) yang turut mendirikan dan memodali project Akun_Quotes; memegang 30% kepemilikan (ekuitas).
- **Kepemilikan_Ekuitas**: Porsi kepemilikan project sebesar 70:30 (Founder 70%, Co-Founder 30%). Porsi kepemilikan ini secara sengaja dibedakan dari pembagian hasil pada waterfall (lihat Pembagian_Hasil); keduanya tidak sama.
- **Pembagian_Hasil**: Distribusi pembagian hasil pada waterfall bagi hasil yang disepakati setara 50:50 antara Founder dan Co-Founder, terlepas dari Kepemilikan_Ekuitas 70:30. Pemisahan antara kepemilikan (70:30) dan distribusi (50:50) bersifat disengaja.
- **Biaya_Langganan**: Biaya berlangganan Premium+ Platform_X per periode yang diperlukan untuk menopang kelayakan monetisasi (nominal to-be-confirmed sesuai harga resmi Platform_X).
- **Modal_Awal**: Dana awal untuk memulai operasi project, ditetapkan setara 6× Biaya_Langganan, disediakan bersama oleh Founder dan Co-Founder.
- **Dana_Cadangan_Langganan**: Kas khusus yang disisihkan untuk membiayai perpanjangan langganan Premium+, dengan target akumulasi setara 12× Biaya_Langganan (runway 12 periode).
- **Pendapatan_Bersih**: Pendapatan dari Program_Sharing_Revenue pada satu periode setelah dikurangi biaya wajib langsung bila ada; menjadi dasar perhitungan bagi hasil antar-Founder.
- **Nilai_Moral**: Prinsip dasar konten Akun_Quotes yang menjunjung kesantunan, kebermanfaatan, dan keluhuran budi, serta bebas dari ujaran kebencian, diskriminasi SARA, dan pornografi (lihat Requirement 2).
- **Penggunaan_Wajar**: Prinsip fair use, yaitu batas penggunaan materi berhak cipta secara terbatas dan sah tanpa izin pemegang hak; batas amannya bersifat to-be-confirmed oleh penasihat hukum.
- **Takedown**: Permintaan atau tindakan penurunan konten akibat klaim pelanggaran (hak cipta, merek, atau lainnya).
- **UU_PDP**: Undang-Undang Perlindungan Data Pribadi yang menjadi acuan prinsip perlindungan data pribadi bagi Akun_Quotes; kewajiban spesifiknya bersifat to-be-confirmed oleh ahli.
- **Doxxing**: Penyebaran data pribadi atau sensitif seseorang tanpa izin yang dilarang bagi Akun_Quotes.
- **Konten_Berbayar**: Postingan atau interaksi yang merupakan endorsement, sponsor, atau kerja sama komersial yang wajib diungkapkan secara jelas.
- **Disclaimer**: Pernyataan penyangkalan yang menegaskan bahwa Quotes bersifat inspiratif/reflektif dan bukan nasihat profesional, serta bukan endorsement tokoh.
- **AI**: Alat kecerdasan buatan yang dipakai sebagai alat bantu operasional Akun_Quotes, bukan pengganti penilaian manusia.
- **Identitas_Verbal**: Elemen identitas berbasis bahasa Akun_Quotes, mencakup nama tampil, @handle, tagline, dan persona suara.
- **Identitas_Visual**: Elemen identitas berbasis tampilan Akun_Quotes, mencakup avatar, banner, palet warna, tipografi, dan gaya kartu kutipan.
- **Bio_Profil**: Isi deskripsi profil Akun_Quotes yang memuat identitas singkat, nilai/tema, disclaimer ringkas, dan tautan resmi.
- **Template_Baku**: Format standar postingan dan materi visual Akun_Quotes yang digunakan untuk menjaga konsistensi identitas.

## Requirements
<!-- Bagian: Persyaratan -->

### Requirement 1: Struktur dan Cakupan Dokumen SOP

**User Story:** Sebagai Admin_Utama, saya ingin SOP memiliki struktur lengkap dan cakupan yang jelas, agar seluruh Pengelola memiliki satu pedoman operasional yang konsisten.

#### Acceptance Criteria

1. THE SOP SHALL memuat bagian tujuan, ruang lingkup, definisi istilah, dan pihak yang bertanggung jawab.
2. THE SOP SHALL memuat bagian terpisah untuk kriteria konten, styleguide, kriteria following, kriteria interaksi/komentar, moderasi, prosedur eskalasi krisis, keamanan akun, jadwal posting, dan metrik program sharing revenue.
3. THE SOP SHALL mencantumkan tanggal berlaku, nomor versi, dan pihak yang menyetujui dokumen.
4. WHEN SOP direvisi, THE SOP SHALL mencatat riwayat perubahan berupa tanggal, ringkasan perubahan, dan penanggung jawab revisi.
5. THE SOP SHALL memperbolehkan revisi disimpan meskipun dokumentasi riwayat perubahan belum lengkap, dan THE SOP SHALL selalu menegakkan penandaan setiap bagian yang belum lengkap untuk dilengkapi kemudian, terlepas dari status ketidaklengkapan sebelumnya.

### Requirement 2: Kriteria Konten dan Quotes yang Diposting

**User Story:** Sebagai Pengelola, saya ingin kriteria konten yang jelas, agar setiap Quotes yang diposting selaras dengan prinsip nilai moral akun.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan bahwa setiap Quotes yang diposting berlandaskan nilai moral dan bebas dari ujaran kebencian, diskriminasi SARA, dan pornografi.
2. THE SOP SHALL menetapkan daftar tema Quotes yang diperbolehkan dan daftar tema yang dilarang.
3. WHERE sebuah Quotes menyentuh topik politik, agama, atau isu sensitif, THE SOP SHALL menetapkan aturan bahwa Quotes tersebut memerlukan persetujuan Admin_Utama sebelum diposting.
4. IF sebuah Quotes tidak memenuhi kriteria nilai moral, THEN THE SOP SHALL menetapkan aturan bahwa Quotes tersebut tidak diposting.
5. IF sebuah Quotes yang tidak memenuhi kriteria nilai moral lolos penyaringan awal dan terlanjur diposting, THEN THE SOP SHALL menetapkan prosedur penghapusan pascapublikasi beserta batas waktu penghapusan.
6. THE SOP SHALL menetapkan panjang maksimum karakter Quotes yang sesuai dengan batas Platform_X.
7. WHEN sebuah Quotes akan diposting, THE SOP SHALL mewajibkan setiap Quotes menyelesaikan proses persetujuan terlebih dahulu, termasuk Quotes yang telah memenuhi kriteria namun masih menunggu review.

### Requirement 3: Verifikasi Sumber dan Atribusi Kutipan

**User Story:** Sebagai Pengelola, saya ingin prosedur verifikasi sumber dan atribusi, agar setiap Quotes akurat dan terhindar dari misattribution serta pelanggaran hak cipta.

#### Acceptance Criteria

1. WHEN sebuah Quotes berasal dari tokoh bernama, THE SOP SHALL menetapkan aturan verifikasi Sumber_Kutipan menggunakan minimal dua rujukan tepercaya sebelum posting.
2. WHEN sebuah Quotes berasal dari sumber anonim atau tradisi peradaban, THE SOP SHALL menetapkan aturan pencantuman Atribusi sebagai "Anonim" atau nama tradisi/peradaban terkait.
3. IF Sumber_Kutipan sebuah Quotes tidak dapat diverifikasi, THEN THE SOP SHALL menetapkan aturan verifikasi dan menunda Quotes tersebut dengan menetapkan statusnya menjadi PENDING hingga verifikasi selesai.
4. THE SOP SHALL menetapkan aturan penghormatan hak cipta dengan tidak memposting materi berhak cipta tanpa izin atau di luar batas penggunaan wajar.
5. WHEN sebuah Quotes diposting, THE SOP SHALL menetapkan aturan pencantuman Atribusi dan memastikan kepatuhan bahwa Atribusi benar-benar tercantum pada setiap postingan, dan Atribusi tersebut boleh berupa tipe apa pun termasuk label anonim (misalnya "Anonim" atau nama tradisi/peradaban).
6. THE SOP SHALL mewajibkan setiap Quotes diklasifikasikan menurut Kategori_Sumber_Perolehan — (a) karangan sendiri/original, (b) website/media sosial, atau (c) AI — dan kategori tersebut dicatat sebagai metadata internal untuk audit; setiap kategori menuntut pemeriksaan sesuai: original wajib benar-benar orisinal dan tunduk pada Nilai_Moral (R2.1) serta Styleguide (Requirement 4); website/media sosial wajib verifikasi Sumber_Kutipan (R3.1) bila dinisbahkan pada tokoh bernama, menghormati hak cipta (R3.4), dan mencatat asal/tautan sumber; AI tunduk pada Kebijakan Penggunaan AI (Requirement 14), termasuk verifikasi manusia terhadap minimal dua rujukan tepercaya dan larangan fabrikasi. (SOP-3.6)

### Requirement 4: Format Penulisan dan Tata Bahasa (Styleguide)

**User Story:** Sebagai Pengelola, saya ingin Styleguide yang baku, agar seluruh konten dan interaksi memiliki gaya penulisan yang konsisten dan profesional.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan aturan penggunaan ejaan Bahasa Indonesia yang baku sesuai PUEBI untuk seluruh konten berbahasa Indonesia.
2. THE SOP SHALL menetapkan aturan tanda baca, penggunaan huruf kapital, dan format kutipan (misalnya penggunaan tanda petik dan pemisah atribusi).
3. THE SOP SHALL mewajibkan setiap Quotes yang diposting mencantumkan, pada akhir baris atribusi, Inisial_Admin Pengelola/Admin_Utama penanggung jawab yang dipisahkan dari Atribusi sumber dengan tanda koma, tanpa menggantikan Atribusi sumber.
4. THE SOP SHALL menetapkan aturan penggunaan tagar (hashtag) sebanyak minimum satu tagar dan maksimum lima tagar per postingan, beserta daftar tagar baku akun.
5. THE SOP SHALL menetapkan aturan nada komunikasi (tone of voice) yang mencerminkan nilai moral, sopan, dan reflektif.
6. THE SOP SHALL selalu menetapkan aturan penyertaan terjemahan Bahasa Indonesia sebagai kebijakan umum SOP, meskipun seluruh Quotes saat ini berbahasa Indonesia.
7. THE SOP SHALL menyediakan minimal tiga contoh format postingan Quotes yang benar sebagai acuan.
8. IF aturan terjemahan belum ditetapkan, THEN THE SOP SHALL memblokir posting Quotes berbahasa asing hingga aturan terjemahan ditetapkan.

### Requirement 5: Kriteria Akun yang Diikuti (Following)

**User Story:** Sebagai Pengelola, saya ingin kriteria following yang jelas, agar daftar akun yang diikuti mendukung reputasi dan menghindari asosiasi dengan isu komentar yang bermasalah.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan kriteria akun yang boleh diikuti dengan mewajibkan ketiga syarat berikut dipenuhi secara simultan: relevansi tema, reputasi positif, dan kesesuaian dengan nilai moral.
2. THE SOP SHALL menetapkan daftar kategori akun yang dilarang diikuti, termasuk akun penyebar ujaran kebencian, hoaks, dan konten kontroversial.
3. WHEN sebuah akun kandidat following memiliki riwayat isu komentar bermasalah, THE SOP SHALL menetapkan aturan peninjauan Admin_Utama yang mengevaluasi baik isu komentar maupun relevansi tema, dan menunda following hingga peninjauan selesai.
4. IF proses peninjauan Admin_Utama belum tersedia sementara akun kandidat memiliki isu komentar, THEN THE SOP SHALL menetapkan aturan pemblokiran following hingga proses peninjauan tersedia.
5. IF akun yang telah diikuti kemudian terlibat kontroversi atau isu komentar bermasalah, THEN THE SOP SHALL menetapkan aturan peninjauan ulang dan opsi unfollow.
6. THE SOP SHALL menetapkan frekuensi peninjauan berkala daftar Following.

### Requirement 6: Kriteria Isi Komentar dan Interaksi

**User Story:** Sebagai Pengelola, saya ingin kriteria interaksi dan komentar yang jelas, agar setiap Interaksi Akun_Quotes menjaga reputasi dan mencerminkan nilai moral.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan kriteria isi komentar yang diperbolehkan, yaitu komentar yang memenuhi minimal salah satu dari kriteria berikut: sopan, relevan, atau mendukung nilai moral; IF sebuah komentar tidak memenuhi satu pun dari ketiga kriteria tersebut, THEN THE SOP SHALL menetapkan bahwa komentar tersebut tidak diperbolehkan.
2. WHEN sebuah komentar menunjukkan karakteristik provokatif, ujaran kebencian, atau perdebatan SARA, THE SOP SHALL mengklasifikasikan komentar tersebut sebagai komentar yang dilarang.
3. WHEN Akun_Quotes membalas komentar pengguna, THE SOP SHALL menetapkan aturan bahwa balasan mengikuti Styleguide dan menjaga nada sopan.
4. IF sebuah komentar dari pengguna lain bersifat provokatif atau menyerang, THEN THE SOP SHALL menetapkan aturan untuk tidak membalas secara emosional dan mengikuti prosedur moderasi.
5. WHERE Akun_Quotes berinteraksi pada konten akun lain, THE SOP SHALL menetapkan aturan bahwa Interaksi hanya dilakukan pada konten yang selaras dengan nilai moral akun.
6. THE SOP SHALL mewajibkan Akun_Quotes melakukan minimum 10 (sepuluh) balasan atau komentar (Interaksi) per hari tanpa batas maksimum pada postingan akun berpengaruh (akun dengan jumlah pengikut tinggi atau tayangan/impressions tinggi), dan setiap balasan tersebut wajib mematuhi gerbang keselarasan nilai moral (R6.5) serta Styleguide dan nada sopan (R6.3) guna mendukung pertumbuhan keterlibatan untuk Program_Sharing_Revenue (Requirement 10); ambang kuantitatif akun berpengaruh ditetapkan kemudian pada SOP.
7. WHEN Akun_Quotes melakukan balasan pada akun berpengaruh (per R6.6), THE SOP SHALL mewajibkan setiap balasan memuat pendapat pribadi (opini) orisinal Pengelola/Admin_Utama yang relevan dengan konteks postingan — bukan templat, ucapan generik, tempelan kutipan tanpa tanggapan, maupun balasan seragam massal — sebagai mitigasi spam, sambil tetap mematuhi gerbang keselarasan nilai moral (R6.5) serta Styleguide dan nada sopan (R6.3).

### Requirement 7: Moderasi Komentar

**User Story:** Sebagai Pengelola, saya ingin prosedur moderasi komentar, agar kolom komentar Akun_Quotes tetap sehat dan sesuai nilai moral.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan kriteria komentar pengguna yang wajib disembunyikan atau dihapus, termasuk spam, ujaran kebencian, dan tautan berbahaya.
2. WHEN sebuah komentar melanggar kriteria moderasi, THE SOP SHALL menetapkan langkah tindakan berupa menyembunyikan, menghapus, atau memblokir pengguna, dan menetapkan bahwa tindakan tersebut dieksekusi secara manual oleh Pengelola.
3. THE SOP SHALL menetapkan daftar kata kunci sensitif yang dipantau pada kolom komentar.
4. THE SOP SHALL menetapkan frekuensi pemeriksaan kolom komentar oleh Pengelola.
5. IF sebuah komentar berada di area abu-abu yang sulit dinilai, THEN THE SOP SHALL menetapkan aturan eskalasi keputusan kepada Admin_Utama; WHERE seluruh kasus komentar bersifat jelas, THE SOP SHALL diperbolehkan beroperasi tanpa aturan eskalasi yang telah ditetapkan sebelumnya.

### Requirement 8: Prosedur Eskalasi Krisis

**User Story:** Sebagai Admin_Utama, saya ingin Prosedur_Eskalasi yang terstruktur, agar Blunder di komentar atau konten dapat ditangani cepat dan meminimalkan kerusakan reputasi.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan definisi dan tingkatan (level) Krisis beserta indikator untuk setiap tingkatan.
2. WHEN sebuah Blunder terdeteksi, THE SOP SHALL menetapkan langkah tanggap awal beserta batas waktu respons untuk setiap tingkatan Krisis.
3. THE SOP SHALL menetapkan urutan eskalasi dan pihak penanggung jawab pada setiap tingkatan Krisis.
4. WHEN sebuah konten menjadi sumber Krisis, THE SOP SHALL menetapkan kriteria keputusan untuk menghapus, mengedit, atau mempertahankan konten tersebut.
5. WHERE Krisis memerlukan pernyataan publik, THE SOP SHALL menetapkan aturan penyusunan dan persetujuan klarifikasi atau permintaan maaf sebelum dipublikasikan.
6. WHEN sebuah Krisis selesai ditangani, THE SOP SHALL menetapkan aturan evaluasi pascakrisis dan pencatatan pembelajaran.

### Requirement 9: Jadwal Posting dan Kalender Konten

**User Story:** Sebagai Pengelola, saya ingin jadwal posting yang terencana, agar frekuensi konten konsisten dan mendukung pertumbuhan akun.

#### Acceptance Criteria

1. THE SOP SHALL mewajibkan Akun_Quotes memposting minimum 10 (sepuluh) postingan per hari tanpa batas maksimum, dan setiap postingan yang dihitung terhadap frekuensi harian tersebut wajib berstatus APPROVED sebelum diposting.
2. THE SOP SHALL menetapkan rentang waktu (jam) posting yang direkomendasikan berdasarkan aktivitas audiens.
3. THE SOP SHALL menetapkan penggunaan Kalender_Konten untuk merencanakan Quotes minimal satu minggu ke depan.
4. IF sebuah slot jadwal tidak terisi konten terverifikasi, THEN THE SOP SHALL menetapkan aturan penggunaan konten cadangan yang telah disetujui.
5. IF sebuah slot jadwal tidak memiliki konten terverifikasi maupun konten cadangan yang telah disetujui, THEN THE SOP SHALL menetapkan aturan untuk mengosongkan slot dan melewati posting pada periode waktu tersebut.
6. WHERE frekuensi minimum posting harian tinggi (10 postingan per hari, R9.1), THE SOP SHALL mewajibkan beberapa Quotes bertema sama atau terkait dikelompokkan dan diterbitkan sebagai satu utas (thread) — alih-alih sebagai postingan terpisah yang dikirim berturut-turut dalam jendela waktu singkat — sebagai mitigasi spam, dan setiap Quotes di dalam utas tersebut tetap wajib mematuhi format posting (Atribusi, Inisial_Admin, batas tagar) serta berstatus APPROVED sebelum diposting; penomoran utas (misalnya 1/n) direkomendasikan; dan WHEN sebuah utas diterbitkan, THE SOP SHALL mewajibkan postingan pembuka utas dimulai dengan kalimat atau paragraf pembuka yang disesuaikan dengan tema Quotes di dalam utas tersebut (memperkenalkan tema utas), dan kalimat/paragraf pembuka tersebut wajib mematuhi Styleguide dan nada komunikasi (R4.5) serta batas maksimum karakter Platform_X (R2.6).

### Requirement 10: Metrik dan Kelayakan Program Sharing Revenue

**User Story:** Sebagai Admin_Utama, saya ingin pemantauan Metrik_Kelayakan, agar Akun_Quotes memenuhi syarat dan mengoptimalkan Program_Sharing_Revenue.

#### Acceptance Criteria

1. THE SOP SHALL mencantumkan syarat kelayakan Program_Sharing_Revenue dari Platform_X yang wajib dipenuhi Akun_Quotes.
2. THE SOP SHALL menetapkan daftar Metrik_Kelayakan yang dipantau, termasuk jumlah pengikut, tayangan (impressions), dan tingkat keterlibatan (engagement).
3. THE SOP SHALL menetapkan frekuensi peninjauan dan pelaporan Metrik_Kelayakan.
4. IF sebuah Metrik_Kelayakan berada di bawah ambang syarat program, THEN THE SOP SHALL menetapkan aturan pemicuan otomatis tindakan perbaikan, termasuk untuk Akun_Quotes tanpa aktivitas (zero activity).
5. IF pemicuan otomatis tindakan perbaikan gagal aktif sementara sebuah Metrik_Kelayakan masih berada di bawah ambang syarat program, THEN THE SOP SHALL menetapkan syarat pengawasan manual oleh Pengelola untuk memicu tindakan perbaikan.
6. THE SOP SHALL menetapkan aturan kepatuhan terhadap kebijakan monetisasi Platform_X untuk menjaga kelayakan Program_Sharing_Revenue.
7. THE SOP SHALL memuat bagian atau lampiran khusus yang menetapkan konten dan perilaku akun yang diperbolehkan dan yang dilarang untuk menjaga kelayakan monetisasi, dengan merujuk Content Monetization Standards Platform_X (https://help.x.com/en/rules-and-policies/content-monetization-standards), dan mencakup minimum: prasyarat kelayakan, kategori konten yang diperbolehkan, kategori konten yang dilarang, dan perilaku manipulasi platform yang dilarang; ambang atau spesifik kebijakan mengikuti kebijakan resmi Platform_X dan boleh ditandai to-be-confirmed.

### Requirement 11: Keamanan Akun

**User Story:** Sebagai Admin_Utama, saya ingin prosedur keamanan akun, agar Akun_Quotes terlindungi dari peretasan dan penyalahgunaan akses.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan aturan penggunaan autentikasi dua faktor (2FA) pada Akun_Quotes.
2. THE SOP SHALL menetapkan aturan pengelolaan kata sandi berupa kompleksitas minimum dan frekuensi pembaruan.
3. WHERE project berada pada tahap penyiapan awal, THE SOP SHALL memperbolehkan pembuatan akun Admin_Utama sementara dengan kebijakan kata sandi sementara sebelum kebijakan penuh diberlakukan.
4. THE SOP SHALL menetapkan daftar Pengelola yang memiliki akses beserta tingkat wewenang masing-masing.
5. WHEN seorang Pengelola berhenti dari project, THE SOP SHALL menetapkan aturan pencabutan akses dalam batas waktu yang ditentukan dan memastikan kepatuhan bahwa akses benar-benar dicabut dalam batas waktu tersebut.
6. IF terdeteksi akses tidak sah pada Akun_Quotes, THEN THE SOP SHALL menetapkan langkah tanggap keamanan berupa pengamanan akun dan pemberitahuan Admin_Utama.

### Requirement 12: Operasional dan Ketentuan Bisnis

**User Story:** Sebagai Founder atau Co-Founder, saya ingin aturan permodalan dan bagi hasil yang jelas, agar project berkelanjutan secara finansial dan adil bagi Founder dan Co-Founder.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan Modal_Awal project sebesar 6× Biaya_Langganan Premium+ yang disediakan bersama oleh Founder dan Co-Founder untuk membiayai langganan awal dan menopang kelayakan monetisasi. (SOP-B.1)
2. THE SOP SHALL menetapkan struktur satu Founder dan satu Co-Founder dengan Kepemilikan_Ekuitas 70:30 (Founder 70%, Co-Founder 30%), dan THE SOP SHALL menetapkan bahwa Pembagian_Hasil pada waterfall bagi hasil tetap setara 50:50 antara Founder dan Co-Founder sebagai pembedaan yang disengaja dari Kepemilikan_Ekuitas, dan WHEN sebuah keputusan finansial material diambil, THE SOP SHALL mewajibkan persetujuan Founder dan Co-Founder. (SOP-B.2)
3. THE SOP SHALL menetapkan pemeliharaan Dana_Cadangan_Langganan dengan target akumulasi 12× Biaya_Langganan (runway 12 periode) yang dipakai membayar langganan Premium+. (SOP-B.3)
4. WHILE saldo Dana_Cadangan_Langganan kurang dari 12× Biaya_Langganan, THE SOP SHALL menetapkan alokasi 50% Pendapatan_Bersih ke Dana_Cadangan_Langganan dan 50% dibagi rata (50:50) ke Founder dan Co-Founder; WHEN saldo Dana_Cadangan_Langganan mencapai atau melebihi 12× Biaya_Langganan, THE SOP SHALL menetapkan alokasi 100% Pendapatan_Bersih dibagi rata (50:50) ke Founder dan Co-Founder; WHERE sebuah periode bersifat transisi, THE SOP SHALL menetapkan bahwa hanya kekurangan menuju 12× Biaya_Langganan yang disisihkan ke Dana_Cadangan_Langganan dan sisanya dibagi rata (50:50) ke Founder dan Co-Founder. (SOP-B.4)
5. THE SOP SHALL menetapkan distribusi bagi hasil secara berkala disertai pencatatan dan transparansi keuangan bagi Founder dan Co-Founder, dan THE SOP SHALL menetapkan bahwa pembayaran langganan dilakukan tepat waktu untuk menjaga kelayakan monetisasi. (SOP-B.5)
6. THE SOP SHALL menetapkan bahwa kepemilikan Akun_Quotes beserta aset terkait (termasuk Dana_Cadangan_Langganan) merupakan milik bersama Founder dan Co-Founder sesuai Kepemilikan_Ekuitas 70:30, dan IF terdapat rencana pemindahtanganan aset, THEN THE SOP SHALL mewajibkan persetujuan Founder dan Co-Founder sebelum pemindahtanganan dilakukan. (SOP-B.6)
7. THE SOP SHALL menetapkan peran operasional Founder selaras dengan Matriks Peran & Wewenang (R1, SOP-1.6), dengan sekurang-kurangnya satu Founder berperan sebagai Admin_Utama. (SOP-B.7)
8. WHEN sebuah pengeluaran di luar Biaya_Langganan diajukan, THE SOP SHALL mewajibkan persetujuan Founder dan Co-Founder sebelum pengeluaran dibelanjakan dan mewajibkan pengeluaran tersebut dicatat. (SOP-B.8)
9. THE SOP SHALL menetapkan pemeliharaan catatan keuangan yang mencakup pemasukan, pengeluaran, saldo Dana_Cadangan_Langganan, dan distribusi bagi hasil, serta menyusun pelaporan berkala yang dapat diakses Founder dan Co-Founder. (SOP-B.9)
10. THE SOP SHALL menetapkan tata kelola perubahan kesepakatan, penyelesaian sengketa, dan keluarnya Founder atau Co-Founder, termasuk pencabutan akses yang selaras dengan aturan pencabutan akses (R11.5). (SOP-B.10)

### Requirement 13: Legal dan Kepatuhan

**User Story:** Sebagai Admin_Utama atau Founder yang menginginkan kepatuhan hukum, saya ingin aturan legal dan kepatuhan yang jelas, agar Akun_Quotes terhindar dari risiko hukum dan tetap memenuhi syarat monetisasi.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan aturan hak cipta dan Penggunaan_Wajar (fair use) yang mencakup larangan penyalinan substansial tanpa izin, pengutamaan Sumber_Kutipan dari domain publik atau berlisensi, penggunaan aset gambar berlisensi disertai bukti lisensi, dan prinsip fail-safe untuk menahan konten bila status hak cipta meragukan, sebagai pendalaman R3.4. (SOP-L.1)
2. WHEN Akun_Quotes menerima klaim pelanggaran atau permintaan Takedown, THE SOP SHALL menetapkan prosedur penanganan cepat yang mencakup penilaian klaim, penurunan atau penyuntingan konten bila klaim berdasar, pendokumentasian klaim dan tindakan, serta penggunaan kanal resmi Platform_X. (SOP-L.2)
3. THE SOP SHALL menetapkan aturan perlindungan data pribadi yang selaras UU_PDP, mencakup minimalisasi pengumpulan data, larangan Doxxing, kerahasiaan isi pesan langsung (DM), dan penanganan permintaan subjek data. (SOP-L.3)
4. WHERE sebuah postingan atau interaksi merupakan Konten_Berbayar, endorsement, atau kerja sama, THE SOP SHALL mewajibkan pengungkapan yang jelas atas hubungan komersial disertai kejujuran mengenai hubungan tersebut, dan tetap selaras dengan Nilai_Moral. (SOP-L.4)
5. THE SOP SHALL mencantumkan Disclaimer yang menegaskan bahwa Quotes bukan nasihat profesional, penghormatan terhadap tokoh tanpa menyiratkan endorsement, dan larangan memotong kutipan hingga menyesatkan makna aslinya. (SOP-L.5)

### Requirement 14: Kebijakan Penggunaan AI

**User Story:** Sebagai Pengelola, saya ingin aturan penggunaan AI yang jelas, agar AI membantu operasional tanpa merusak akurasi, keaslian, dan kelayakan monetisasi Akun_Quotes.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan ruang lingkup penggunaan AI yang diperbolehkan sebagai alat bantu, mencakup ide dan kurasi tema, penyuntingan bahasa, penyusunan draf teks pendukung yang wajib disunting manusia sebelum tayang, dan riset awal, serta menegaskan bahwa AI bukan pengganti penilaian manusia. (SOP-AI.1)
2. WHEN sebuah Quotes atau Atribusi diperoleh atau disusun dengan bantuan AI, THE SOP SHALL mewajibkan verifikasi manusia terhadap minimal dua rujukan tepercaya sebelum tayang dan menetapkan bahwa AI tidak boleh menjadi satu-satunya sumber, sebagai penegakan R3.1 dan R3.3. (SOP-AI.2)
3. THE SOP SHALL melarang penggunaan AI untuk fabrikasi kutipan atau Atribusi, produksi konten menyesatkan atau media manipulatif, pelanggaran hak cipta, dan manipulasi keterlibatan. (SOP-AI.3)
4. THE SOP SHALL menetapkan bahwa tanggung jawab akhir atas setiap konten berada pada manusia (Pengelola atau Admin_Utama), suara akun tetap sesuai persona akun, dan akun mempertimbangkan keterbukaan penandaan konten ber-AI selaras dengan keaslian yang disyaratkan Platform_X. (SOP-AI.4)
5. THE SOP SHALL melarang pemasukan data pribadi atau sensitif ke alat AI pihak ketiga, selaras dengan perlindungan data pribadi R13.3 dan keamanan akun Requirement 11. (SOP-AI.5)

### Requirement 15: Brand dan Identitas

**User Story:** Sebagai Pengelola, saya ingin identitas brand yang konsisten, agar Akun_Quotes mudah dikenali dan tampil profesional.

#### Acceptance Criteria

1. THE SOP SHALL menetapkan Identitas_Verbal yang mencakup nama tampil, @handle, tagline, dan persona suara yang konsisten dengan nada komunikasi (tone of voice) pada R4.5. (SOP-BR.1)
2. THE SOP SHALL menetapkan Identitas_Visual yang mencakup avatar, banner, palet warna dengan kontras yang aksesibel, tipografi, dan gaya kartu kutipan. (SOP-BR.2)
3. THE SOP SHALL menetapkan isi Bio_Profil yang mencakup identitas singkat, nilai atau tema, Disclaimer ringkas, dan tautan resmi, serta tidak menyesatkan. (SOP-BR.3)
4. THE SOP SHALL mewajibkan konsistensi Identitas_Verbal dan Identitas_Visual pada seluruh materi serta penggunaan Template_Baku, dan menetapkan bahwa perubahan identitas dicatat melalui kontrol dokumen (Bagian 0). (SOP-BR.4)
5. THE SOP SHALL menetapkan panduan do dan don't visual yang mencakup batasan keterbacaan dan kontras serta pencantuman Atribusi dan Inisial_Admin pada kartu kutipan, selaras dengan R3.5 dan R4.3. (SOP-BR.5)
