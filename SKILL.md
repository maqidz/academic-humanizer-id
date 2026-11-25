---
name: academic-humanizer-id
version: 1.0.0
description: >-
  Meningkatkan kejelasan dan suara ilmiah tulisan akademik berbahasa Indonesia
  berbantuan AI (artikel jurnal Sinta/Scopus, skripsi, tesis, disertasi,
  tanggapan reviewer) serta proposal hibah (BIMA Kemdiktisaintek, RIIM BRIN,
  LPDP Rispro, maupun NSF/NIH): menjaga konvensi ilmiah dan kaidah EYD V/KBBI,
  menyelaraskan klaim dengan bukti (dan kelayakan pada proposal), serta
  menyesuaikan gaya tulis penulis. Tidak pernah mengubah angka, hasil statistik,
  rumus, atau sitasi, dan bukan alat untuk menghindari pengungkapan penggunaan
  AI. Gunakan saat menyunting draf akademik atau proposal hibah.
license: MIT
compatibility: antigravity claude-code codex morphmind opencode
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Academic Humanizer (ID)

Meningkatkan kejelasan, ketepatan, dan suara ilmiah tulisan *akademik*
berbantuan AI dalam Bahasa Indonesia (serta mendukung istilah/naskah bilingual
ID–EN) sambil menjaga ketelitian berbasis bukti yang dituntut karya ilmiah dan
menyelaraskannya dengan gaya tulis penulis sendiri. Skill ini menjaga setiap
angka, hasil, rumus, dan sitasi tetap utuh, dan **bukan** alat untuk
menghindari kebijakan pengungkapan penggunaan AI (*AI-use disclosure*).

---

## Prinsip Integritas (Wajib Dipatuhi)

1. **Jangan pernah mengubah data:** Angka, persentase, *p-value*, interval
   kepercayaan, ukuran sampel (*n*), skor evaluasi (F1, akurasi, RMSE, AUC),
   rumus matematika, simbol, dan hasil eksperimen harus tetap sama persis.
2. **Jangan pernah mengubah sitasi & markup:** Pertahankan `\cite{}`, `\ref{}`,
   `\label{}`, format sitasi APA/IEEE/Chicago, tautan Markdown, catatan kaki,
   dan isi tabel secara utuh.
3. **Jangan pernah memfabrikasi bukti:** Jika draf memuat klaim tanpa metrik
   pendukung (misalnya *"meningkat drastis"*), turunkan klaimnya dan sisipkan
   `[PENULIS: masukkan angka/metrik pasti]` daripada mengarang angka.
4. **Hormati suara penulis:** Jika pengguna menyediakan contoh tulisan
   sebelumnya, tiru ritme kalimat, sudut pandang, dan gaya *hedging*-nya.

---

## Alur Kerja: Baca → Audit → Tulis Ulang → Laporkan

Jalankan keempat tahap berikut secara berurutan kecuali pengguna secara
eksplisit hanya meminta satu tahap (misalnya *"audit saja"*).

### 1. Baca & Klasifikasi
- Tentukan **jenis naskah**: artikel jurnal/prosiding, bab skripsi/tesis/disertasi,
  tanggapan *reviewer* (*rebuttal*), atau proposal hibah (aktifkan **Layer 6**).
- Tentukan **target publikasi / gaya selingkung**: Skripsi/Tesis/Disertasi,
  Jurnal Sinta 1–6, Scopus/internasional, Prosiding, atau skema hibah
  (BIMA, RIIM BRIN, LPDP Rispro, NSF/NIH).
- Jika ada contoh tulisan penulis (*writing sample*), catat rata-rata panjang
  kalimat, pilihan pronomina (*penelitian ini*, *kami*, atau pasif), dan
  kepadatan transisi.

### 2. Audit (Diagnosis Sebelum Mengubah Teks)
Pindai naskah melewati enam layer dan tampilkan tabel audit singkat:

| Lokasi | Layer & Pola | Status Bukti | Rencana Perbaikan |
| :--- | :--- | :--- | :--- |
| Paragraf 1, Kal. 1 | `L2: Pembuka klise era` | N/A | Buka langsung dengan celah riset konkret |
| Paragraf 1, Kal. 2 | `L1: Em-dash & kalke` | N/A | Hapus `—`, ubah struktur lebih lugas |
| Paragraf 1, Kal. 3 | `L4: Klaim melebihi bukti` | Berlebihan (*membuktikan*) | Ganti dengan *menunjukkan secara empiris* + metrik |

### 3. Tulis Ulang (Enam Layer)
Terapkan seluruh layer di bawah ini tanpa mengorbankan ketepatan ilmiah.

### 4. Laporkan (Keluaran & Catatan Perubahan)
Sajikan keluaran dalam format berikut:
1. **Ringkasan Audit** (tabel/poin temuan utama)
2. **Teks Hasil Revisi** (siap salin, markup LaTeX/Markdown utuh)
3. **Catatan Perubahan (*Changelog*)**:
   - Pola AI, kalke terjemahan, & pengisi (*filler*) yang dihapus
   - Klaim yang dikalibrasi terhadap bukti (+ daftar `[PENULIS: ...]` jika ada)
   - Penyesuaian gaya, ritme kalimat, dan kaidah EYD V/KBBI
4. **Verifikasi Integritas**: Konfirmasi eksplisit bahwa seluruh angka, sitasi,
   rumus, dan simbol teknis tidak berubah.

---

## Arsitektur Enam Layer

### Layer 1: Katalog Ciri AI Umum (Bahasa Indonesia)
Hapus pola mekanis, kosakata klise AI, dan kalke terjemahan Inggris–Indonesia
(katalog lengkap: [katalog-ciri-ai-id.md](./references/katalog-ciri-ai-id.md)):

- **Kosakata klise AI:** *menyelami, menggarisbawahi, menyoroti (berlebihan),
  lanskap (metaforis), permadani/jalinan, bukti nyata, ranah, paradigma (tanpa
  dasar teoretis), sinergi, holistik (tanpa definisi), komprehensif (tanpa
  cakupan), krusial, vital, transformatif, revolusioner, mulus (seamless)*.
- **Kalke terjemahan Inggris–Indonesia:**
  - *"Adalah penting untuk dicatat bahwa..."* → *"Perlu dicatat bahwa..."* atau hapus pembukanya.
  - *"Memainkan peran kunci/penting dalam..."* → *"Berperan dalam..."* / *"Memengaruhi..."*.
  - *"...yang mana..."* / *"...di mana..."* (bukan tempat) → *"...yang..."*, *"...ketika..."*, atau pecah kalimat.
  - *"Berdasarkan fakta bahwa..."* → *"Karena..."* / *"Mengingat..."*.
- **Nominalisasi bertumpuk:** *"Pelaksanaan pengoptimalan pemrosesan dilakukan guna pencapaian peningkatan akurasi"* → *"Proses dioptimalkan untuk meningkatkan akurasi."*
- **Tanda pisah panjang (`—` / em-dash):** Hapus seluruh *em-dash*; ganti dengan koma, tanda kurung, titik dua, atau dua kalimat.
- **Paralelisme negatif:** *"bukan hanya sekadar X, melainkan juga Y"* → nyatakan langsung kedua poin secara konkret.
- **Ekor partisipial terjemahan:** *"..., yang menyoroti pentingnya..."*, *"..., sehingga membuka jalan bagi..."* → potong atau jadikan kalimat temuan tersendiri.
- **Transisi mekanis berulang:** Hindari mengawali setiap kalimat dengan *"Selain itu,"*, *"Lebih lanjut,"*, *"Di samping itu,"*, *"Pada akhirnya,"*.

### Layer 2: Ciri AI Khusus Akademik Indonesia
- **Pembuka klise:** Ganti *"Di era globalisasi/digitalisasi saat ini..."* atau *"Dalam beberapa tahun terakhir, X telah menarik perhatian besar..."* dengan masalah spesifik atau celah riset.
- **Klaim kebaruan kosong:** Hindari *"Sepengetahuan penulis, ini adalah penelitian pertama..."* kecuali terverifikasi; jelaskan keterbatasan studi terdahulu dan kontribusi spesifik.
- **Penguat tanpa ukuran:** Ganti *"pengujian ekstensif"*, *"evaluasi menyeluruh"*, *"peningkatan signifikan"* (tanpa *p-value*) dengan jumlah dataset dan angka aktual.
- **Hiperbola masa depan:** Hapus *"membuka jalan bagi paradigma baru"*, *"membuka babak baru"*; nyatakan batasan atau langkah riset lanjutan yang nyata.
- **Penumpukan sitasi (*citation dumping*):** Ubah *"Banyak metode telah diusulkan [1–6]"* menjadi pengelompokan berbasis mekanisme/keterbatasan.
- **Penanda bagian bertele-tele:** Ubah *"Pada bagian ini, kami akan menyelami rincian metodologi..."* menjadi *"Bagian 3 menguraikan formulasi metode dan skenario uji."*

### Layer 3: Pelestarian Konvensi Ilmiah & EYD V / KBBI
Jangan menghapus konvensi ilmiah yang sah (panduan lengkap: [konvensi-kalibrasi-id.md](./references/konvensi-kalibrasi-id.md)):
- **Pertahankan *hedging* berbasis bukti:** *mengindikasikan, sejalan dengan, dalam cakupan sampel ini, pada kondisi pengujian tersebut*.
- **Pertahankan kalimat pasif wajar di Metode:** *"Sampel disentrifugasi pada 3.000 rpm selama 10 menit"*.
- **Pertahankan istilah teknis baku:** *signifikan secara statistik*, *robustness*, *focal loss*, *loss landscape*.
- **Terapkan EYD V & KBBI:** bedakan `di` kata depan (*di lapangan, di atas*) vs `di-` imbuhan pasif (*dianalisis, dilakukan*); cetak miring istilah asing yang belum diserap (*overfitting, p-value*); gunakan ejaan baku (*analisis, sistem, metode, efektivitas, praktik, risiko, objek, subjek, hipotesis*).

### Layer 4: Kalibrasi Klaim ↔ Bukti
Kekuatan kata kerja tidak boleh melampaui jenis bukti dalam draf:

| Jenis Bukti | Kata Kerja yang Tepat | Hindari |
| :--- | :--- | :--- |
| Pembuktian matematis formal | *membuktikan, menjamin, berlaku bahwa* | — |
| Eksperimen terkontrol / kausal | *menunjukkan, menurunkan/meningkatkan sebesar X* | *membuktikan mutlak, menuntaskan* |
| Evaluasi *benchmark* / komputasi | *meningkatkan [metrik] sebesar X pada [dataset]* | *mengungguli semua metode* |
| Observasional / korelasional / survei | *berasosiasi dengan, berkorelasi dengan, mengindikasikan* | *menyebabkan, menentukan, membuktikan* |
| Studi kasus / kualitatif | *menggambarkan, menunjukkan indikasi pada kasus ini* | *membuktikan secara umum* |

### Layer 5: Kalibrasi Gaya, Ritme, & Target Publikasi
- **Skripsi / Tesis / Disertasi:** Bahasa Indonesia baku EYD V, impersonal (*"Penelitian ini..."*), runtut, bebas hiperbola.
- **Jurnal Sinta 1–6 / Prosiding:** Ringkas, padat, pembukaan langsung ke celah penelitian, hasil kuantitatif jelas, pembahasan terhubung ke literatur.
- **Tanggapan Reviewer (*Rebuttal*):** Sopan, lugas, langsung merujuk lokasi revisi (bagian/halaman/tabel), tanpa pujian berlebihan.
- **Variasi ritme kalimat:** Pecah deretan 4–6 kalimat seragam (22–30 kata) dengan memadukan kalimat deklaratif pendek (8–15 kata) dan analitis menengah (18–26 kata).

### Layer 6: Mode Proposal Hibah *(Aktif Khusus Proposal Pendanaan)*
Untuk proposal hibah (BIMA Kemdiktisaintek, RIIM BRIN, LPDP Rispro, hibah internal, atau NSF/NIH; detail: [mode-proposal-hibah-id.md](./references/mode-proposal-hibah-id.md)):
- **Keunggulan halaman pertama:** Ringkasan dan Urgensi langsung memuat masalah nyata, gagasan utama, tujuan terukur, kesiapan tim, dan target luaran.
- **Klaim ↔ Kelayakan (*Feasibility*):** Tautkan setiap target ambisius ke data pendahuluan, Peta Jalan (*Roadmap*) rekam jejak tim, target TKT/TRL, tonggak capaian (*milestones*), dan mitigasi risiko. Jika jangkar kelayakan belum ada, sisipkan `[PENULIS: tautkan ke data pendahuluan atau mitigasi risiko]`.
- **Hapus retorika proposal kosong:** Ganti *"berpotensi merevolusi sektor X"* dengan hambatan spesifik dan pengguna sasaran; ganti *"tim kami memiliki posisi unik"* dengan bukti publikasi, dataset, atau fasilitas nyata.

---

## Contoh Sebelum & Sesudah

**Sebelum (sarat ciri AI & klaim berlebihan):**
> Di era digitalisasi saat ini, deteksi ujaran kebencian di media sosial telah menarik perhatian yang sangat besar. Dalam penelitian ini, kami mengusulkan pendekatan inovatif—dengan memanfaatkan mekanisme pembobotan adaptif—dan membuktikan melalui serangkaian pengujian komprehensif bahwa metode kami secara signifikan melampaui seluruh metode sebelumnya, sehingga membuka jalan bagi paradigma baru dalam moderasi konten.

**Sesudah (`academic-humanizer-id`):**
> Metode klasifikasi ujaran kebencian pada teks berbahasa Indonesia umumnya masih mengalami penurunan kinerja pada kelas minoritas dan data berlabel bising. Penelitian ini menambahkan komponen pembobotan kerugian yang adaptif terhadap kebisingan label dan mengevaluasinya pada tiga korpus publik berbahasa Indonesia. Hasil pengujian menunjukkan peningkatan skor F1 kelas minoritas sebesar 3–6 poin dibandingkan *focal loss*, dengan selisih akurasi kelas mayoritas kurang dari 1 poin.
