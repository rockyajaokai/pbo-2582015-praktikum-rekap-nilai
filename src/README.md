# Praktikum — Rekap Nilai Kelas

Program Java untuk merekap nilai satu kelas mahasiswa yang dimasukkan satu per satu,
tanpa mengetahui di awal berapa jumlah mahasiswa yang akan diinput.

## Cara Kerja

- Program membaca nilai satu per satu hingga user mengetik `-1` (sentinel).
- Nilai di luar rentang 0–100 ditolak dan tidak menaikkan pencacah mahasiswa.
- Setiap nilai valid diberi **grade** (A/B/C/D/E) dan **keterangan grade**.
- Di akhir, program menampilkan **rata-rata kelas** dan **status kelas**.

## Ketentuan yang Diimplementasikan

- [x] `do-while` dengan sentinel `static final int SELESAI = -1;`
- [x] Nilai di luar 0–100 ditolak lewat `continue`, pencacah tidak ikut naik
- [x] Ladder `if / else if / else` untuk grade: A ≥ 90, B ≥ 80, C ≥ 70, D ≥ 60, sisanya E
- [x] Keterangan grade menggunakan `switch` gaya lambda (arrow)
- [x] Rata-rata dihitung dengan `total += nilai`
- [x] Status kelas menggunakan `ternary`, bukan `if`

## Cara Menjalankan

1. Buka project di IntelliJ IDEA.
2. Jalankan `src/RekapNilai.java`.
3. Masukkan nilai satu per satu, ketik `-1` untuk mengakhiri.

## Struktur Project

```
pbo-2582006-praktikum-rekap-nilai/
└── src/
    └── RekapNilai.java
```

## Catatan Pribadi

- **Kenapa `do-while`, bukan `while`?** Karena program harus meminta minimal satu
  input dulu sebelum bisa mengecek apakah sentinel sudah dimasukkan.
- **Kenapa urutan ladder grade harus dari tertinggi ke terendah?** Kalau dibalik,
  nilai tinggi (misal 95) akan langsung tertangkap kondisi `nilai >= 60` di awal
  dan salah dikategorikan sebagai D, bukan A.
