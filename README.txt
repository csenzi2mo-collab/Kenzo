KENZO MARKET - VERCEL + MIDTRANS

PAKAI SANDBOX DULU

1. Upload folder project ini ke GitHub lalu import ke Vercel.
2. Vercel -> Project -> Settings -> Environment Variables.
3. Tambahkan:
   MIDTRANS_SERVER_KEY = Server Key SANDBOX Midtrans Anda
4. Di index.html ganti:
   GANTI_DENGAN_CLIENT_KEY_SANDBOX
   menjadi Client Key SANDBOX Anda.
5. Redeploy project.

WEBHOOK
Set Notification URL Midtrans SANDBOX ke:
https://NAMA-PROJECT-ANDA.vercel.app/api/notification

ALUR
pilih paket -> isi nama/email/whatsapp -> Snap Midtrans -> pembayaran

CATATAN
- Server Key hanya di Environment Variables Vercel.
- Client Key berada di index.html.
- Harga dikirim sebagai data-harga sehingga tidak lagi dibaca dari teks "Rp 3.000".
- Harga juga divalidasi ulang di server.
- Endpoint notification memverifikasi signature Midtrans.
- Versi ini belum menyimpan order ke database.

SETELAH SANDBOX BERHASIL
Untuk production, ganti endpoint Snap dan API Midtrans dari sandbox ke production,
lalu gunakan Client Key dan Server Key PRODUCTION.
