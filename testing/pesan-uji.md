# Pesan Uji ScamShield ID

10 pesan uji: 8 penipuan/mencurigakan dan 2 pesan sah. Semua data adalah contoh fiktif (tidak ada nomor atau rekening asli).

| # | Pesan | Jenis sebenarnya | Hasil ideal |
|---|-------|------------------|-------------|
| 1 | "Assalamualaikum, dengan hormat kami mengundang Anda di acara pernikahan kami. Detail undangan ada di file: Undangan_Digital.apk" | Penipuan (APK palsu) | Berbahaya, skor 85+ |
| 2 | "Paket Anda tertahan karena alamat tidak lengkap. Klik link berikut dan bayar biaya admin Rp3.500 sebelum 2 jam: bit.ly/xxxx" | Penipuan (paket palsu) | Berbahaya, skor 80+ |
| 3 | "Halo, kami butuh tenaga part-time, cukup like & follow video, komisi Rp50rb-Rp300rb per tugas, langsung cair. Chat WA ini untuk daftar." | Penipuan (kerja paruh waktu) | Berbahaya, skor 80+ |
| 4 | "Ma, ini nomor baru Adit, HP yang lama rusak. Tolong transfer Rp1,5 juta dulu ya buat bayar kos, nanti Adit ganti. Jangan bilang Papa." | Penipuan (mengaku keluarga) | Berbahaya, skor 80+ |
| 5 | "Selamat! Nomor Anda terpilih memenangkan hadiah Rp25 juta. Untuk pencairan, kirim kode OTP yang masuk ke HP Anda." | Penipuan (hadiah + OTP) | Berbahaya, skor 90+ |
| 6 | "Tim kami melihat akun Anda cocok jadi member VIP trading. Modal Rp500rb, profit 10% per hari dijamin, tanpa risiko." | Penipuan (investasi bodong) | Berbahaya, skor 85+ |
| 7 | "Halo kak, saya sudah transfer Rp850.000 ya, ini buktinya [gambar]. Tolong kirim barangnya hari ini, saya buru-buru." | Mencurigakan (bukti transfer palsu) | Waspada, skor 40-60; sarankan cek mutasi rekening sendiri |
| 8 | "Kode OTP Anda adalah 482913. Jangan berikan kode ini kepada siapa pun termasuk pihak bank." (diterima tepat setelah pengguna login/transaksi sendiri) | Sah | Aman, skor 0-20; tidak menuduh |
| 9 | "Reminder: Kuliah Pemrograman Web besok pukul 08.00 di Ruang 3.2. Mohon membawa laptop." (dari grup kelas) | Sah | Aman, skor 0-10 |
| 10 | "Pak/Bu, kami dari bank. Ada transaksi mencurigakan di rekening Anda. Demi keamanan, mohon konfirmasi PIN dan OTP sekarang atau rekening diblokir." | Penipuan (phishing bank) | Berbahaya, skor 90+ |

## Catatan Desain Pengujian
- Pesan #7 adalah kasus abu-abu: tidak bisa dipastikan penipuan hanya dari teks.
- Pesan #8 dan #9 adalah pesan sah untuk mengukur *false positive* (pesan asli yang salah dituduh penipuan).
- Pesan #8 sengaja memuat kata "OTP" untuk menguji apakah agent hanya bereaksi pada kata kunci atau memahami konteks.