# Aturan: Tautan Dokumentasi

Setiap kali sebuah dokumen di repositori ini (terutama README dan file SOP) **merujuk berkas lain**, rujukan tersebut **harus berupa tautan Markdown relatif yang dapat diklik**, bukan sekadar nama berkas dalam teks/backtick.

Berlaku saat:
- Membuat berkas baru → tambahkan tautan ke berkas itu dari README/indeks dan dokumen terkait yang merujuknya.
- Memindahkan/mengganti nama berkas → perbarui semua tautan yang menunjuk ke berkas tersebut agar tidak rusak.
- Menghapus berkas → hapus atau alihkan tautan yang menunjuk ke berkas itu.

Ketentuan:
- Gunakan path relatif yang benar (mis. `[nama](../folder/berkas.md)`).
- Tujuan: memudahkan pembaca non-teknis menelusuri seluruh isi dengan sekali klik.
- Pengecualian: nama berkas di dalam blok kode (fenced code block, mis. pohon direktori) tidak bisa ditautkan; sediakan daftar tautan terpisah di luar blok kode bila perlu.
- Setelah menamb/memindahkan berkas, verifikasi tidak ada tautan yang menggantung (broken link).
