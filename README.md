# Kalkulator Kurs Invoice

Halaman kalkulator USD ke IDR untuk admin invoicing. Satu file HTML, tanpa instalasi, dibuka langsung di browser (Chrome/Edge).

## Cara pakai

1. Unduh `index.html`, lalu buka di browser.
2. Kurs otomatis terisi dari Frankfurter (kurs referensi ECB).
3. Isi item invoice dalam USD. Nilai IDR, total, dan terbilang terhitung otomatis.
4. Salin total, terbilang, atau seluruh tabel (bisa ditempel ke Excel).

## Fitur

- **Kurs otomatis** dari `https://api.frankfurter.dev/v1/latest?base=USD&symbols=IDR`, dicek ulang tiap 10 menit. Kurs terakhir disimpan untuk dipakai saat offline.
- **Mode manual** untuk Kurs KMK (Faktur Pajak), JISDOR, atau kurs kontrak, dengan kolom dasar kurs yang ikut tercantum saat tabel disalin.
- **Kunci kurs** agar angka satu invoice tidak berubah saat dikerjakan.
- **Input angka fleksibel** (`1,250.50` atau `1.250,50`), dengan tampilan angka yang terbaca di bawah setiap kolom.
- **Pembulatan per baris** ke rupiah penuh, sehingga total sama dengan jumlah baris di invoice.
- **Terbilang** otomatis dalam bahasa Indonesia.
- Isian tersimpan di browser (localStorage).

## Catatan kurs

Frankfurter memakai kurs referensi Bank Sentral Eropa yang terbit sekali tiap hari kerja (sekitar 16.00 CET). Pada akhir pekan dan hari libur ECB, kurs yang dipakai adalah kurs hari kerja terakhir. Untuk dokumen pajak, gunakan Kurs KMK lewat mode Manual.
