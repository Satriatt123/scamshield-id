# Hasil Pengujian per Versi Prompt

Cara mengisi: jalankan tiap pesan dari `pesan-uji.md` pada setiap versi prompt di IBM Bob, lalu isi kolom dengan hasil nyata.
Tulis format `Level (skor)`, misalnya `Berbahaya (88)`. Tandai ✅ jika sesuai hasil ideal, ❌ jika tidak.

## Tabel Hasil

| # | Jenis sebenarnya | Hasil ideal | V1 | V2 | V3 | V4 | V5 |
|---|------------------|-------------|----|----|----|----|----|
| 1 | Penipuan (APK) | Berbahaya 85+ |  |  |  |  |  |
| 2 | Penipuan (paket) | Berbahaya 80+ |  |  |  |  |  |
| 3 | Penipuan (kerja part-time) | Berbahaya 80+ |  |  |  |  |  |
| 4 | Penipuan (mengaku keluarga) | Berbahaya 80+ |  |  |  |  |  |
| 5 | Penipuan (hadiah + OTP) | Berbahaya 90+ |  |  |  |  |  |
| 6 | Penipuan (investasi) | Berbahaya 85+ |  |  |  |  |  |
| 7 | Mencurigakan (bukti transfer) | Waspada 40-60 |  |  |  |  |  |
| 8 | Sah (OTP dari sistem) | Aman 0-20 |  |  |  |  |  |
| 9 | Sah (pengumuman kuliah) | Aman 0-10 |  |  |  |  |  |
| 10 | Penipuan (phishing bank) | Berbahaya 90+ |  |  |  |  |  |
| | **Akurasi (x/10)** | | /10 | /10 | /10 | /10 | /10 |

## Metrik Tambahan (opsional)

| Metrik | V1 | V2 | V3 | V4 | V5 |
|--------|----|----|----|----|----|
| Format output konsisten? (Ya/Tidak) |  |  |  |  |  |
| Menyertakan alasan berupa kutipan pesan? |  |  |  |  |  |
| Mengarang nomor/link resmi? (Ya/Tidak) |  |  |  |  |  |
| False positive pada pesan #8 dan #9 (dari 2) |  |  |  |  |  |

## Temuan Utama
Isi 3-4 kalimat setelah semua tabel terisi, misalnya:
- Versi mana yang paling meningkatkan akurasi dan kenapa.
- Kasus yang paling sulit (kemungkinan #7 dan #8) dan bagaimana V5 menanganinya.
- Kegagalan yang ditemukan dan perbaikan yang dibuat.

## Bukti
Screenshot perbandingan ada di folder `../screenshots/` (minimal V1 vs V5 untuk pesan #1 atau #4).