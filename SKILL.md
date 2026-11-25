---
name: academic-humanizer-id
description: >-
  Menghilangkan ciri tulisan AI, frasa klise, kalke terjemahan Inggris-Indonesia,
  nominalisasi bertumpuk, dan klaim berlebihan dari naskah akademik berbahasa
  Indonesia (skripsi, tesis, disertasi, artikel jurnal Sinta/Scopus, tanggapan
  reviewer, dan proposal hibah BIMA/BRIN/LPDP) sambil mempertahankan suara
  ilmiah penulis, kaidah EYD V/KBBI, sitasi, angka, rumus, dan ketepatan bukti.
  Gunakan skill ini ketika pengguna meminta untuk menghumanisasi, memoles,
  menyunting, menghilangkan kesan AI, atau merapikan teks akademik berbahasa
  Indonesia.
---

# Academic Humanizer (Bahasa Indonesia)

Sunting naskah akademik dan proposal hibah berbahasa Indonesia agar terbaca
seperti tulisan peneliti manusia yang jernih, ringkas, dan berdisiplin ilmiah
— bukan terjemahan kaku atau pola generik AI.

> **Batas Integritas (Wajib Dipatuhi):** Skill ini adalah alat penyuntingan
> kejelasan dan ketepatan ilmiah, bukan alat kecurangan akademik atau penghindar
> detektor AI. **Jangan pernah** mengarang atau mengubah angka, nilai statistik
> (*p-value*, F1, akurasi, ukuran sampel), sitasi, nama penulis, persamaan
> matematika, simbol, atau kesimpulan eksperimen. Jangan pernah memfabrikasi
> bukti agar klaim tampak lebih kuat.

---

## Alur Kerja Utama: Baca -> Audit -> Tulis Ulang -> Laporkan

Selalu jalankan empat langkah berikut secara berurutan kecuali pengguna secara
eksplisit hanya meminta satu tahap (misalnya: *"audit saja"*).

### Langkah 1: Baca & Klasifikasi
1. Identifikasi **jenis naskah**:
   - Bagian artikel jurnal / prosiding (Abstrak, Pendahuluan, Tinjauan Pustaka, Metode, Hasil & Pembahasan, Kesimpulan)
   - Bab skripsi, tesis, atau disertasi
   - Surat tanggapan reviewer (*rebuttal* / *response to reviewers*)
   - Proposal hibah penelitian (mengaktifkan **Layer 6: Mode Proposal Hibah**)
2. Identifikasi **target publikasi / gaya selingkung** (misalnya: pedoman skripsi/tesis kampus, Jurnal Sinta 1–6, prosiding nasional, atau skema hibah BIMA/BRIN/LPDP).
3. Jika pengguna melampirkan contoh tulisan sebelumnya, catat pola panjang kalimat, pilihan pronomina (*penelitian ini*, *penulis*, *kami*, atau kalimat pasif), serta tingkat kehati-hatian (*hedging*) untuk diselaraskan pada Layer 5.
4. Pertahankan seluruh markup struktural (`\cite{}`, `\ref{}`, `\label{}`, `$...$`, tautan Markdown, catatan kaki, isi tabel) secara persis, kecuali memperbaiki tanda baca yang keliru di sekitarnya.

### Langkah 2: Audit (Diagnosis Awal)
Sebelum menulis ulang, pindai teks melewati enam layer dan tampilkan daftar
temuan konkret secara ringkas:
- **Lokasi** (paragraf / cuplikan kalimat)
- **Layer & Pola** (misalnya: `L1: kalke terjemahan`, `L1: em-dash`, `L2: pembuka klise`, `L4: klaim melebihi bukti`)
- **Status Bukti** (khusus klaim empiris: *Didukung*, *Berlebihan*, atau *Metrik hilang — butuh input penulis*)
- **Rencana Perbaikan**

Jika naskah sangat panjang (misalnya satu bab penuh), rangkum pola berulang
utama dan soroti bagian paling berdampak terlebih dahulu.

### Langkah 3: Tulis Ulang (Enam Layer)
Terapkan keenam layer berikut sambil menjaga seluruh angka, sitasi, simbol, dan
definisi teknis tetap utuh:

1. **Layer 1 — Katalog Ciri AI Umum (Bahasa Indonesia)**:
   Hapus kosakata klise AI (*menyelami, menggarisbawahi, lanskap, permadani,
   bukti nyata, sinergi, holistik, komprehensif tanpa cakupan, krusial, vital,
   mulus*), kalke terjemahan Inggris-Indonesia (*"adalah penting untuk..."*,
   *"memainkan peran kunci"*), nominalisasi bertumpuk, paralelisme negatif
   (*"bukan hanya sekadar X, melainkan juga Y"*), ekor partisipial terjemahan
   (*"..., yang menyoroti pentingnya..."*), transisi mekanis berulang
   (*"Selain itu,", "Lebih lanjut,"*), serta **tanda pisah panjang (`—` /
   em-dash)** yang diganti dengan koma, titik dua, tanda kurung, atau dua
   kalimat terpisah.
   -> Katalog lengkap: [katalog-ciri-ai-id.md](./references/katalog-ciri-ai-id.md)

2. **Layer 2 — Ciri AI Khusus Akademik Indonesia**:
   Ganti pembuka klise (*"Di era globalisasi/digitalisasi saat ini..."*,
   *"Dalam beberapa tahun terakhir..."*), klaim kebaruan kosong
   (*"Sepengetahuan penulis, ini adalah penelitian pertama..."*), penguat tanpa
   bukti (*"pengujian ekstensif"*, *"peningkatan signifikan"* tanpa uji
   statistik), *hype* masa depan (*"membuka jalan bagi paradigma baru"*),
   penumpukan sitasi tanpa sintesis, dan penanda bagian yang bertele-tele.
   -> Katalog & contoh perbaikan: [katalog-ciri-ai-id.md](./references/katalog-ciri-ai-id.md)

3. **Layer 3 — Pelestarian Konvensi Ilmiah & EYD V / KBBI**:
   Jangan menghapus elemen akademik yang sah. Pertahankan *hedging* berbasis
   bukti (*mengindikasikan, sejalan dengan, dalam cakupan sampel ini*), kalimat
   pasif yang wajar pada Metode Penelitian, istilah teknis baku, serta terapkan
   kaidah EYD V (pembedaan `di-` imbuhan vs `di` kata depan, huruf miring untuk
   istilah asing yang belum diserap, tanda baca baku).
   -> Panduan lengkap: [konvensi-kalibrasi-id.md](./references/konvensi-kalibrasi-id.md)

4. **Layer 4 — Kalibrasi Klaim ↔ Bukti**:
   Pastikan kekuatan kata kerja tidak pernah melampaui jenis bukti yang ada.
   Ganti besaran kabur (*"jauh lebih baik"*, *"meningkat drastis"*) dengan
   angka aktual dari draf; jika angka belum tersedia, turunkan klaim dan
   sisipkan `[PENULIS: masukkan angka/metrik pasti]` tanpa mengarang data.
   -> Tangga kata kerja & contoh: [konvensi-kalibrasi-id.md](./references/konvensi-kalibrasi-id.md)

5. **Layer 5 — Kalibrasi Gaya, Ritme, & Target Publikasi**:
   Sesuaikan laras bahasa dengan target (skripsi/tesis/disertasi, jurnal Sinta,
   prosiding, atau tanggapan reviewer) dan contoh tulisan penulis jika ada.
   Variasikan panjang kalimat agar tidak terjebak irama monoton khas AI.
   -> Profil publikasi: [konvensi-kalibrasi-id.md](./references/konvensi-kalibrasi-id.md)

6. **Layer 6 — Mode Proposal Hibah Indonesia** *(aktifkan hanya untuk proposal hibah)*:
   Berbeda dari artikel jurnal, proposal hibah perlu menunjukkan visi dan
   urgensi yang kuat sekaligus kelayakan teknis. Pertahankan ambisi riset yang
   terukur, optimalkan halaman pertama (Ringkasan/Urgensi), tautkan Peta Jalan
   (*Roadmap*) ke rekam jejak pengusul, selaraskan target TKT/TRL dan Luaran
   Wajib/Tambahan (BIMA, BRIN, LPDP Rispro), serta sertakan mitigasi risiko.
   -> Protokol proposal: [mode-proposal-hibah-id.md](./references/mode-proposal-hibah-id.md)

### Langkah 4: Laporkan (Hasil & Ringkasan Perubahan)
Sajikan keluaran dalam empat bagian singkat:
1. **Ringkasan Audit**: Daftar ringkas pola AI dan klaim berlebihan yang ditemukan.
2. **Teks Hasil Revisi**: Naskah bersih siap pakai (mempertahankan markup LaTeX/Markdown jika ada).
3. **Catatan Perubahan (*Changelog*)**: Poin singkat dikelompokkan menjadi:
   - Pola AI, kalke terjemahan, & pengisi (*filler*) yang dihapus
   - Klaim yang dikalibrasi terhadap bukti (beserta daftar tanda `[PENULIS: ...]` jika ada)
   - Penyesuaian gaya, ritme kalimat, dan kaidah EYD V
4. **Verifikasi Integritas**: Nyatakan secara eksplisit bahwa seluruh angka, sitasi, rumus, dan simbol teknis tetap utuh tanpa perubahan.

---

## Contoh Singkat Sebelum & Sesudah

**Sebelum (sarat ciri AI & klaim berlebihan):**
> Di era digitalisasi saat ini, deteksi ujaran kebencian di media sosial telah menarik perhatian yang sangat besar. Dalam penelitian ini, kami mengusulkan pendekatan inovatif—dengan memanfaatkan mekanisme pembobotan adaptif—dan membuktikan melalui serangkaian pengujian komprehensif bahwa metode kami secara signifikan melampaui seluruh metode sebelumnya, sehingga membuka jalan bagi paradigma baru dalam moderasi konten.

**Sesudah (`academic-humanizer-id`):**
> Metode klasifikasi ujaran kebencian pada teks berbahasa Indonesia umumnya masih mengalami penurunan kinerja pada kelas minoritas dan data berlabel bising. Penelitian ini menambahkan komponen pembobotan kerugian yang adaptif terhadap kebisingan label dan mengevaluasinya pada tiga korpus publik berbahasa Indonesia. Hasil pengujian menunjukkan peningkatan skor F1 kelas minoritas sebesar 3–6 poin dibandingkan *focal loss*, dengan selisih akurasi kelas mayoritas kurang dari 1 poin.
