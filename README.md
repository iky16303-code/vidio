# Malam Hujan – Animasi 3D Cinematic (Three.js)

## Menjalankan
1. Butuh **Chrome / Edge desktop terbaru** dan koneksi internet (Three.js r128 dan mp4-muxer dimuat dari CDN).
2. Buka `index.html` langsung dengan klik dua kali, atau jalankan server lokal:
   `python -m http.server 8000` lalu buka http://localhost:8000
3. Preview langsung berjalan (24 detik, loop).

## Kontrol
- **Spasi**: play/pause · **← / →**: mundur/maju 1 detik
- Tombol ⏸/▶, ⏮ (ulang), slider seek
- **Suara**: aktifkan ambience hujan di preview (perlu klik karena kebijakan browser)
- **Kualitas preview**: 540p / 720p / 1080p

## Ekspor MP4
Klik **⬇ Ekspor MP4**. Video dirender offline frame demi frame (bukan rekam layar), jadi hasilnya mulus walau komputer lambat:
- 1080 × 1920 (9:16), 60 FPS, 24 detik, H.264 + AAC, ±16 Mbps
- Audio hujan, gemuruh petir, dan tetes air dibuat prosedural dan ikut dimasukkan ke MP4
- Proses memakan beberapa menit; file otomatis terunduh (`malam-hujan-1080x1920-60fps.mp4`)

## Isi adegan
Karakter chibi (rambut hitam tebal berantakan, mata anime besar, kaos hitam aksen oranye, celana cargo hitam, sandal hitam) duduk mengetik di depan komputer. Kepala menoleh ke jendela, tangan mengetik lalu memegang mouse, berkedip. Layar menyala dengan kode bergulir, lampu meja hangat dengan bayangan, hujan di luar jendela dan tetes di kaca, kilat tipis, kamera orbit pelan dari belakang ke profil samping. Efek: depth of field, bloom, pantulan di lantai/kaca, vignette, grain. Fade in/out halus, tidak ada objek yang muncul/hilang tiba-tiba (tetes air mengecil perlahan).

## Penyesuaian
Di bagian atas `<script>`: `D` (durasi, detik, 23–30 disarankan), `FPS`, `EXPOSURE` (kecerahan).

## Catatan
- Karakter dibangun dari bentuk 3D prosedural yang meniru desain referensi (warna, rambut, pakaian, proporsi chibi), bukan model hasil konversi gambar. Untuk wajah yang 100% identik, ganti dengan model `.glb` karakter Anda memakai `GLTFLoader`.
- Kode belum bisa diuji di browser dari sisi saya. Jika tampilan terlalu terang/gelap, ubah `EXPOSURE`.
