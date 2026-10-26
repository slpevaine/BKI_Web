# PT Bintang Khatulistiwa Internusa (BKI) — Website

Prototipe website company profile PT Bintang Khatulistiwa Internusa (BKI), penyedia solusi konektivitas satelit terkelola (BKIConnect) untuk operasional maritim.

Situs statis (HTML, CSS, dan sedikit JavaScript). Tanpa framework, build step, atau backend.

## Halaman

| File | Isi |
|---|---|
| `index.html` | Beranda |
| `tentang.html` | Profil, visi dan misi, perjalanan, peran BKI |
| `solusi.html` | BKIConnect, paket bertingkat (Lite, Standard, Plus, Prime), teknologi, proses |
| `industri.html` | Sektor yang dilayani |
| `klien.html` | Klien |
| `kontak.html` | Kontak, alamat, media sosial |

Bahasa: judul utama berbahasa Inggris, isi berbahasa Indonesia.

## Menjalankan secara lokal

Butuh Python 3 (atau server statis apa pun).

```bash
python3 -m http.server 8080
```

Buka http://localhost:8080.

## Struktur

```
.
├── *.html
└── assets/
    ├── css/style.css   # seluruh gaya, design token ada di :root
    ├── js/main.js      # hanya toggle menu mobile
    └── img/            # foto, logo, ornamen
```

## Catatan pengembangan

- **Desain:** font Lexend dan Source Sans 3 (Google Fonts), warna mengikuti logo (navy `#095994`, cyan `#00ADEF`). Mengutamakan aksesibilitas: skip link, fokus terlihat, `prefers-reduced-motion`, responsif hingga 375 px.
- **Navigasi dan footer** ditulis ulang di setiap file HTML. Jika menu berubah, perbarui semua halaman.
- **Posisi regulasi:** konten sengaja tidak memposisikan BKI sebagai ISP. Kapasitas satelit disebut diperoleh dari operator satelit melalui mitra resmi. Teks ini perlu ditinjau konsultan hukum sebelum rilis publik.
- **Harga** belum dicantumkan. Penawaran diberikan setelah konsultasi.
- **Form kontak** tidak ada. Permintaan penawaran memakai tautan `mailto:`.

## Yang perlu dilengkapi sebelum rilis

- Verifikasi nomor telepon dan email di footer dan halaman Kontak.
- Konfirmasi paket kecepatan (Speed 2, Speed 8, Speed Max) di `solusi.html`.
- Ganti foto industri dan klien dengan foto beresolusi tinggi yang jelas lisensinya.
- Halaman Karier dihapus sementara.
