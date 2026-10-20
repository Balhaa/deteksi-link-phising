# Detektor Link Phishing dan Pelacak Redirect URL

Aplikasi web satu halaman untuk memeriksa indikator risiko pada URL dan melihat rantai pengalihannya.

## Fitur

- Memeriksa indikator seperti penggunaan alamat IP, karakter `@`, domain Punycode, HTTP, peniruan nama brand, TLD berisiko, dan rantai redirect yang panjang.
- Mengambil rantai redirect melalui layanan Redirect Check.
- Menampilkan skor risiko, peringatan, tujuan akhir, serta riwayat pemindaian selama halaman dibuka.
- Tetap menganalisis struktur URL jika layanan pelacak redirect tidak dapat diakses.

## Menjalankan

Buka [`detektor_link_phishing_pelacak_url.html`](./detektor_link_phishing_pelacak_url.html) di browser. Koneksi internet diperlukan untuk memuat React, Tailwind CSS, Font Awesome, Google Fonts, dan layanan Redirect Check dari CDN atau layanan eksternal.

## Deploy ke GitHub Pages

Workflow GitHub Actions di `.github/workflows/pages.yml` akan menerbitkan aplikasi ke GitHub Pages setiap kali ada push ke branch `main`. File HTML aplikasi disajikan sebagai halaman utama situs.

Untuk deploy pertama kali:

1. Push workflow ini ke branch `main`.
2. Di repository GitHub, buka **Settings > Pages** dan pilih **GitHub Actions** sebagai *Build and deployment source* jika belum dipilih.
3. Buka tab **Actions** dan tunggu workflow **Deploy to GitHub Pages** selesai.
4. Buka URL situs yang ditampilkan pada deployment workflow atau di **Settings > Pages**.

## Privasi dan batasan

URL yang diperiksa dikirim ke `redirectcheck.org` untuk memperoleh informasi redirect. Jangan masukkan URL yang memuat token, kata sandi, atau informasi privat. Analisis menggunakan indikator sederhana dan bukan jaminan bahwa suatu tautan aman atau berbahaya; selalu verifikasi tautan melalui sumber tepercaya.
