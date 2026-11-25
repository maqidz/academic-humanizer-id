# Layer 3, Layer 4 & Layer 5: Konvensi Ilmiah, Kalibrasi Bukti & Gaya Bahasa Indonesia

Gunakan referensi ini agar penyuntingan tidak merusak kaidah ilmiah yang sah,
menjaga setiap klaim sebanding dengan buktinya, dan menyelaraskan gaya dengan
target publikasi di Indonesia.

---

## Layer 3: Konvensi Ilmiah & Kaidah EYD V yang Harus Dipertahankan

Jangan menandai atau menghapus elemen berikut sebagai ciri AI:

1. **Kehati-hatian ilmiah berbasis bukti (*evidence-tied hedging*)**:
   *mengindikasikan, menunjukkan kecenderungan, sejalan dengan, dalam batas
   sampel yang diuji, pada kondisi eksperimen ini*.
2. **Kalimat pasif yang tepat**: Lazim dan dianjurkan pada bagian Metode
   Penelitian (*"Sampel disentrifugasi pada 3.000 rpm selama 10 menit"*, *"Data
   dikumpulkan menggunakan kuesioner terstruktur"*). Hanya ubah ke aktif jika
   kalimat pasif mengaburkan pelaku atau memperumit alur.
3. **Konsistensi sudut pandang**:
   - Skripsi/tesis/disertasi umumnya memakai sudut pandang impersonal
     (*"Penelitian ini mengevaluasi..."*) atau pasif sesuai pedoman kampus.
   - Artikel jurnal/prosiding dapat memakai *"kami"* atau *"penelitian ini"*
     secara konsisten dari awal hingga akhir.
4. **Istilah teknis & padanan baku**: Pertahankan istilah bidang ilmu meski
   mirip kata klise umum (misalnya *signifikan secara statistik*, *ketangguhan /
   robustness* dalam pembelajaran mesin, *lanskap energi* dalam fisika/kimia).
5. **Kaidah EYD V & KBBI dasar**:
   - Pisahkan kata depan `di` (*di lapangan, di atas, di dalam*) dan gabungkan
     awalan pasif `di-` (*dianalisis, dilakukan, dibandingkan*).
   - Gunakan huruf miring untuk istilah asing yang belum diserap (*overfitting,
     focal loss, p-value*), dan ejaan serapan baku untuk yang sudah masuk KBBI
     (*analisis, sistem, metode, efektivitas, praktik, risiko, objek, subjek,
     hipotesis*).
   - Gunakan tanda koma untuk angka desimal Bahasa Indonesia (`3,45%`, `p < 0,05`)
     jika seluruh naskah berbahasa Indonesia, kecuali di dalam blok persamaan
     LaTeX atau tabel baku yang memang mengikuti notasi titik.

---

## Layer 4: Tangga Kalibrasi Klaim ↔ Bukti

Sesuaikan kekuatan kata kerja dengan jenis bukti yang benar-benar ada di draf:

| Jenis Bukti | Kata Kerja yang Tepat | Hindari |
| :--- | :--- | :--- |
| **Pembuktian matematis formal** | *membuktikan, menjamin, menurunkan, berlaku bahwa* | — |
| **Eksperimen terkontrol / identifikasi kausal** | *menunjukkan, menurunkan/meningkatkan sebesar X, berpengaruh terhadap* | *membuktikan secara mutlak, menuntaskan* |
| **Evaluasi benchmark / komputasional** | *meningkatkan [metrik] sebesar X pada [dataset], mengungguli [baseline] pada...* | *mengungguli seluruh metode sebelumnya, membuktikan keunggulan* |
| **Data observasional / korelasional / survei** | *berasosiasi dengan, berkorelasi dengan, mengindikasikan, sejalan dengan* | *menyebabkan, menentukan, membuktikan dampak langsung* |
| **Studi kasus / kualitatif** | *menggambarkan, menunjukkan indikasi, memperlihatkan pola pada kasus ini* | *membuktikan secara umum, berlaku untuk semua* |

### Aturan Jika Metrik Hilang
Jika draf menulis *"secara signifikan mengungguli metode sebelumnya"* atau
*"mempercepat waktu komputasi secara drastis"* tanpa angka di dalam teks:
- **Jangan** mengarang angka.
- Turunkan klaimnya dan sisipkan penanda eksplisit:
  `meningkatkan akurasi dibandingkan [baseline] ([PENULIS: masukkan selisih angka dan nama dataset])`.

---

## Layer 5: Kalibrasi Gaya, Ritme, & Target Publikasi

### Menyelaraskan Contoh Tulisan Penulis
Jika pengguna memberikan contoh tulisan sebelumnya, tiru secara alami:
- Rata-rata panjang kalimat dan variasi kalimat pendek vs. majemuk
- Pilihan pronomina (*penelitian ini* vs. *kami* vs. pasif)
- Kepadatan transisi dan cara merujuk tabel/gambar

### Profil Target Publikasi Indonesia
- **Skripsi / Tesis / Disertasi:** Bahasa Indonesia baku sesuai EYD V, nada
  objektif dan impersonal (*"Penelitian ini..."*), alur deduktif yang rapi,
  tanpa bahasa jurnalistik atau hiperbola.
- **Jurnal Nasional Terakreditasi (Sinta 1–6):** Ringkas, padat informasi,
  pembukaan langsung pada celah penelitian (*research gap*), hasil dilaporkan
  kuantitatif/spesifik, pembahasan membandingkan temuan dengan studi terdahulu.
- **Prosiding / Konferensi Ilmiah:** Langsung ke inti masalah, kalimat lebih
  pendek dan tegas, metrik utama muncul jelas di Abstrak dan Pendahuluan.
- **Surat Tanggapan Reviewer (*Rebuttal*):** Sopan, lugas, tidak defensif,
  langsung menjawab poin kritik dengan lokasi revisi spesifik (halaman,
  paragraf, tabel/gambar) tanpa pujian berlebihan (*"Terima kasih banyak atas
  komentar Anda yang sangat brilian dan luar biasa..."* -> *"Terima kasih atas
  masukan terkait X. Kami telah menambahkan analisis Y pada Bagian 3.2."*).

### Pemeriksaan Ritme Kalimat
Teks buatan AI sering menghasilkan 4–6 kalimat berturut-turut dengan panjang
seragam (22–30 kata) dan struktur sama (`[Subjek] [Predikat] [Objek], sehingga
[klausa ekor]`). Pecah irama monoton ini dengan memadukan kalimat deklaratif
pendek (8–15 kata) dan kalimat analitis menengah (18–26 kata).
