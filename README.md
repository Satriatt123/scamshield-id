# ScamShield ID

AI Agent (IBM Bob) untuk menganalisis pesan penipuan digital berbahasa Indonesia. Pengguna menempelkan pesan mencurigakan, lalu agent memberi verdict, skor risiko 0-100, red flag, dan langkah aman.

## Capstone Project Track IBM Bob
- **Use case:** Scam Message Analyzer (topic baru)
- **Target pengguna:** masyarakat umum, orang tua, mahasiswa, pelaku UMKM

## Struktur Repo
| Path | Isi |
|------|-----|
| `prompt/prompt-final.md` | Prompt 3 layer versi final |
| `prompt/iterasi-v1-v5.md` | Riwayat perubahan prompt dan alasannya |
| `testing/pesan-uji.md` | 10 pesan uji (penipuan dan pesan sah) |
| `testing/hasil-uji.md` | Hasil uji tiap versi prompt |
| `screenshots/` | Bukti tampilan di IBM Bob |

## Arsitektur Prompt
- **Layer 1: Role & Context.** Peran analis keamanan digital dan konteks modus lokal.
- **Layer 2: Task & Requirement.** Langkah analisis, red flag, dan skor risiko.
- **Layer 3: Constraints & Output.** Batasan keamanan dan format output tetap.

## Cara Menjalankan
1. Buka agent di IBM Bob dan tempel prompt dari `prompt/prompt-final.md`.
2. Kirim pesan yang ingin dicek.
3. Baca hasil analisis dan ikuti langkah aman.

## Pengembangan Lanjutan
Analisis screenshot, pengecekan link/nomor, bot WhatsApp/Telegram, mode edukasi, draf laporan otomatis.