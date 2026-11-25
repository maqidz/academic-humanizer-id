# academic-humanizer-id

Skill agen AI (*agent skill*) khusus **naskah akademik berbahasa Indonesia** untuk menghilangkan ciri tulisan AI, frasa klise, kalke terjemahan Inggris–Indonesia, nominalisasi bertumpuk, dan klaim berlebihan — sambil menjaga suara ilmiah penulis, kaidah **EYD V / KBBI**, sitasi, angka, rumus, markup LaTeX/Markdown, dan ketepatan bukti.

Terinspirasi dari arsitektur 6-layer [AIScientists-Dev/academic-humanizer](https://github.com/AIScientists-Dev/academic-humanizer), lalu dirancang ulang secara khusus untuk konteks akademik Indonesia (skripsi, tesis, disertasi, artikel jurnal Sinta/Scopus, tanggapan *reviewer*, dan proposal hibah BIMA/BRIN/LPDP).

> **Batas Integritas:** Skill ini adalah alat penyuntingan kejelasan dan ketepatan ilmiah, bukan alat kecurangan akademik. Skill ini **tidak pernah** mengarang atau mengubah angka, nilai statistik (*p-value*, F1, akurasi, ukuran sampel), sitasi, persamaan, simbol, atau kesimpulan eksperimen.

---

## Struktur Repositori

```text
academic-humanizer-id/
├── SKILL.md                                  # Instruksi utama (alur kerja + ringkasan 6 layer)
├── README.md                                 # Dokumentasi & cara pemasangan
└── references/
    ├── katalog-ciri-ai-id.md                 # Layer 1 & 2: Kosakata klise AI, kalke terjemahan, & ciri akademik ID
    ├── konvensi-kalibrasi-id.md              # Layer 3, 4 & 5: EYD V/KBBI, tangga klaim-bukti, & profil publikasi
    └── mode-proposal-hibah-id.md             # Layer 6: Protokol proposal hibah BIMA, RIIM BRIN, & LPDP Rispro
```

---

## Alur Kerja & Arsitektur 6 Layer

Setiap naskah diproses melalui empat tahap: **Baca → Audit → Tulis Ulang → Laporkan**.

1. **Layer 1 — Katalog Ciri AI Umum (Bahasa Indonesia):** Menghapus kosakata klise AI (*menyelami, menggarisbawahi, lanskap, permadani, sinergi, holistik*), kalke terjemahan (*"adalah penting untuk..."*, *"memainkan peran kunci"*, *"yang mana"*), nominalisasi bertumpuk, paralelisme negatif (*"bukan hanya sekadar X, melainkan juga Y"*), ekor partisipial terjemahan, transisi mekanis berulang, serta *em-dash* (`—`).
2. **Layer 2 — Ciri AI Khusus Akademik Indonesia:** Mengganti pembuka klise (*"Di era globalisasi/digitalisasi saat ini..."*), klaim kebaruan kosong, penguat tanpa ukuran (*"pengujian ekstensif"*), *hype* masa depan, dan penumpukan sitasi (*citation dumping*) tanpa sintesis.
3. **Layer 3 — Pelestarian Konvensi Ilmiah & EYD V / KBBI:** Menjaga *hedging* berbasis bukti (*mengindikasikan, sejalan dengan*), kalimat pasif wajar di Metode, konsistensi pronomina, pembedaan `di-` imbuhan vs `di` kata depan, huruf miring istilah asing, serta ejaan baku KBBI.
4. **Layer 4 — Kalibrasi Klaim ↔ Bukti:** Menyesuaikan kekuatan kata kerja dengan jenis bukti (matematis, eksperimen terkontrol, *benchmark*, observasional, kualitatif). Jika metrik tidak ada di draf, menyisipkan `[PENULIS: masukkan angka/metrik pasti]` tanpa mengarang data.
5. **Layer 5 — Kalibrasi Gaya, Ritme, & Target Publikasi:** Menyesuaikan laras bahasa untuk Skripsi/Tesis/Disertasi, Jurnal Sinta 1–6, Prosiding, atau Tanggapan Reviewer, serta memecah irama panjang kalimat yang monoton.
6. **Layer 6 — Mode Proposal Hibah Indonesia:** Aktif khusus untuk proposal hibah (BIMA Kemdiktisaintek, RIIM BRIN, LPDP Rispro, hibah internal) agar urgensi halaman pertama, Peta Jalan (*Roadmap*), TKT/TRL, Luaran Wajib/Tambahan, dan mitigasi risiko tersaji kuat namun realistis.

---

## Cara Memasang

### Antigravity (Global Skill)
```bash
git clone https://github.com/maqidz/academic-humanizer-id.git ~/.gemini/config/skills/academic-humanizer-id
```

### Claude Code / Codex
```bash
git clone https://github.com/maqidz/academic-humanizer-id.git ~/.claude/skills/academic-humanizer-id
```

### Chat Browser (Gemini, ChatGPT, Claude.ai)
Unggah file `SKILL.md` (dan file di folder `references/` bila diperlukan) bersama draf naskah Anda, lalu minta model menerapkan aturan pada skill tersebut.

---

## Contoh Penggunaan

- *"Audit dan humanize bagian Pendahuluan skripsi ini dengan skill `academic-humanizer-id`."*
- *"Rapikan abstrak dan pembahasan artikel ini untuk target Jurnal Sinta 2."*
- *"Sunting draf Ringkasan dan Urgensi proposal hibah BIMA ini dengan mode proposal hibah."*
- *"Periksa tanggapan reviewer ini supaya sopan, lugas, dan tidak berlebihan."*
