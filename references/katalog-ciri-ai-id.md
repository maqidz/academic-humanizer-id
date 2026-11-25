# Layer 1 & Layer 2: Katalog Ciri AI Umum & Akademik Bahasa Indonesia

Gunakan referensi ini pada tahap **Audit** dan **Tulis Ulang** untuk mendeteksi
pola tulisan generik AI, kalke terjemahan, dan klise akademik khas Bahasa
Indonesia.

---

## Layer 1: Katalog Ciri AI Umum Bahasa Indonesia

### 1. Kosakata Klise AI
Tandai dan ganti kecuali digunakan dalam makna teknis yang ketat:
- **Kata kerja:** *menyelami, menggarisbawahi, menyoroti (berlebihan), memupuk, memanfaatkan (berulang untuk "menggunakan"), memperkuat/mendongkrak secara metaforis, menjembatani kesenjangan, merevolusi, menavigasi (metaforis), mengurai benang merah*
- **Kata benda:** *lanskap (metaforis), permadani/jalinan (tapestry), bukti nyata (testament), ranah (berlebihan), paradigma (tanpa dasar teoretis), landasan/pilar utama, sinergi, dinamika kompleks, segudang/beragam sekali*
- **Kata sifat / keterangan:** *krusial, vital, transformatif, revolusioner, bernuansa (nuanced), multifaset, rumit/intrikat, mulus (seamless), holistik (tanpa definisi), komprehensif (tanpa ruang lingkup), mendalam (berlebihan), signifikan (tanpa uji statistik)*

### 2. Kalke Terjemahan Inggris -> Indonesia
AI sering menerjemahkan struktur sintaksis bahasa Inggris mentah-mentah ke
Bahasa Indonesia:

| Kalke Terjemahan (Hindari) | Bahasa Indonesia Akademik Alami |
| :--- | :--- |
| *Adalah penting untuk dicatat bahwa...* | *Perlu dicatat bahwa...* (atau hapus pembukanya dan langsung tulis intinya) |
| *Memainkan peran penting / krusial dalam...* | *Berperan dalam...* / *Memengaruhi...* |
| *Dalam hal ini, ...* (diulang terus-menerus) | Gunakan rujukan konkret (*Pada tahap ini, ...* / *Untuk skenario tersebut, ...*) |
| *...yang mana...* (terjemahan kaku dari *which*) | *...yang...* atau pecah menjadi dua kalimat |
| *...di mana...* (bukan penunjuk tempat, dari *where*) | *...ketika...*, *...dengan kondisi...*, *...yang menunjukkan...* |
| *Berdasarkan fakta bahwa...* (*based on the fact that*) | *Karena...* / *Mengingat...* |
| *Memiliki potensi untuk mengubah...* | *Berpotensi menurunkan/meningkatkan [variabel spesifik]...* |
| *Sejumlah besar studi telah dilakukan...* | *Berbagai penelitian terdahulu membahas...* (sebutkan cakupannya) |

### 3. Pola Struktur & Tanda Baca Khas AI
| Pola | Contoh (Hindari) | Perbaikan |
| :--- | :--- | :--- |
| **Tanda pisah panjang (`—` / em-dash)** | *Model ini—yang dilatih pada data bising—menghasilkan presisi lebih tinggi.* | Hapus seluruh *em-dash*; ubah memakai koma, tanda kurung, titik dua, atau dua kalimat. |
| **Paralelisme negatif** | *Metode ini bukan hanya sekadar lebih cepat, melainkan juga lebih akurat.* | Nyatakan langsung: *Metode ini berjalan 2,1 kali lebih cepat dengan akurasi 1,4 poin lebih tinggi.* |
| **Ekor partisipial terjemahan** | *..., yang menyoroti pentingnya regularisasi dan menggarisbawahi potensinya.* | Potong ekornya, atau jadikan satu temuan konkret sebagai kalimat tersendiri. |
| **Nominalisasi bertumpuk** | *Pelaksanaan pengoptimalan pemrosesan dilakukan guna pencapaian peningkatan akurasi.* | Ubah ke kata kerja aktif/pasif yang jernih: *Proses dioptimalkan untuk meningkatkan akurasi.* |
| **Daftar tiga serangkai kosong** | *...akurat, skalabel, dan mudah diinterpretasikan...* (padahal hanya akurasi yang diuji) | Pertahankan hanya sifat yang benar-benar diuji dalam naskah. |
| **Transisi mekanis berulang** | *Selain itu, ... Lebih lanjut, ... Di samping itu, ... Pada akhirnya, ...* di setiap awal kalimat | Variasikan dengan hubungan logis (*Namun, Karena itu, Sebaliknya, Secara khusus*) atau biarkan alur topik mengalir alami. |

---

## Layer 2: Ciri AI Khusus Akademik Indonesia

| Ciri Akademik | Contoh (Hindari) | Pengganti Berbasis Bukti |
| :--- | :--- | :--- |
| **Pembuka klise era/tahun** | *Di era globalisasi dan digitalisasi saat ini...* / *Dalam beberapa tahun terakhir, X berkembang pesat...* | Langsung buka dengan masalah teknis, kesenjangan riset, atau fenomena empiris spesifik. |
| **Klaim kebaruan kosong** | *Sepengetahuan penulis, penelitian ini adalah yang pertama membahas...* | Jelaskan keterbatasan studi terdahulu dan kontribusi spesifik naskah ini tanpa klaim "pertama" yang tidak terverifikasi. |
| **Penguat tanpa ukuran** | *pengujian yang ekstensif*, *evaluasi menyeluruh*, *peningkatan yang sangat signifikan* (tanpa p-value) | Sebutkan jumlah & metriknya: *pengujian pada empat dataset*, *meningkatkan F1 sebesar 3,2 poin (p < 0,01)*. |
| **Hiperbola masa depan** | *membuka jalan bagi...*, *membuka babak baru...*, *menetapkan standar baru...* | Sebutkan keterbatasan penelitian atau langkah lanjutan yang konkret. |
| **Kata kerja melebihi bukti** | *membuktikan*, *memastikan*, *menyelesaikan masalah* (untuk studi empiris/observasional) | Gunakan *menunjukkan secara empiris*, *mengindikasikan*, *menurunkan galat pada [dataset]* (lihat Layer 4). |
| **Penumpukan sitasi (*citation dumping*)** | *Banyak metode telah diusulkan [1, 2, 3, 4, 5, 6].* | Kelompokkan sitasi berdasarkan pendekatan atau kelemahannya: *Studi terdahulu mengatasi X melalui pembobotan ulang [1, 2] atau augmentasi data [3, 4].* |
| **Pagar makna kabur** | *sedikit lebih baik*, *cukup memadai*, *relatif stabil* | Ganti dengan rentang angka atau pernyataan batas yang jelas. |
| **Penanda bagian bertele-tele** | *Pada bagian ini, kami akan menyelami secara mendalam rincian metodologi yang digunakan.* | *Bagian 3 menguraikan formulasi fungsi kerugian dan skenario pelatihan.* (Atau langsung masuk ke isi metode.) |
