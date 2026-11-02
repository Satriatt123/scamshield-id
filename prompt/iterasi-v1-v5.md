# Iterasi Prompt V1 sampai V5

Setiap versi diuji dengan 10 pesan yang sama (lihat `../testing/pesan-uji.md`). Hasil lengkap ada di `../testing/hasil-uji.md`.

---

## V1: Prompt Satu Kalimat
```
Cek apakah pesan ini penipuan.
```
- **Tujuan:** baseline, melihat perilaku agent tanpa arahan.
- **Masalah yang ditemukan:** [isi dari hasil ujimu, misalnya: jawaban singkat tanpa alasan, format berubah-ubah, terlalu yakin]
- **Keputusan:** tambahkan Layer 1 agar agent punya peran dan konteks.

---

## V2: Menambah Layer 1 (Role & Context)
```
[Layer 1 dari prompt-final.md]

Cek apakah pesan ini penipuan.
```
- **Perubahan:** menambahkan identitas ScamShield ID, audiens awam, dan daftar modus lokal Indonesia.
- **Alasan:** V1 tidak mengenal modus khas Indonesia dan bahasanya tidak disesuaikan untuk orang awam.
- **Dampak:** [isi dari hasil ujimu]
- **Masalah tersisa:** [isi, misalnya: alasan masih umum, belum ada skor]

---

## V3: Menambah Layer 2 (Task & Requirement)
```
[Layer 1]
[Layer 2 tanpa paragraf terakhir "Jika ada tanda pesan sah..."]
```
- **Perubahan:** menambahkan 5 langkah analisis (klasifikasi modus, red flag, skor 0-100, alasan dengan kutipan, langkah aman).
- **Alasan:** penilaian perlu sistematis dan bisa dibandingkan antar pesan.
- **Dampak:** [isi dari hasil ujimu]
- **Masalah tersisa:** [isi, misalnya: format tidak konsisten, kadang terlalu yakin, kadang mengarang kontak resmi]

---

## V4: Menambah Layer 3 (Constraints & Output)
```
[Layer 1]
[Layer 2 tanpa paragraf terakhir "Jika ada tanda pesan sah..."]
[Layer 3 tanpa baris "Jangan menuduh jika bukti lemah..."]
```
- **Perubahan:** menambahkan batasan (tingkat keyakinan, larangan data sensitif, larangan mengarang kontak) dan format output tetap.
- **Alasan:** mencegah halusinasi, menjaga keamanan, dan membuat output konsisten.
- **Dampak:** [isi dari hasil ujimu]
- **Masalah tersisa:** [isi, misalnya: pesan sah #8 dan #9 masih dinilai Waspada karena ada kata "OTP"]

---

## V5: Aturan Anti False-Positive (Versi Final)
- **Perubahan:** menambahkan dua aturan:
  1. Layer 2: "Jika ada tanda pesan sah ... nyatakan dengan jelas dan turunkan skor."
  2. Layer 3: "Jangan menuduh jika bukti lemah; sarankan verifikasi lewat kanal resmi."
- **Alasan:** pesan sah dan pesan abu-abu perlu dibedakan dari penipuan nyata supaya agent tidak menimbulkan panik atau kehilangan kepercayaan pengguna.
- **Dampak:** [isi dari hasil ujimu]
- **Prompt lengkap:** lihat `prompt-final.md`.

---

## Ringkasan Evolusi

| Versi | Layer | Fokus perbaikan |
|-------|-------|-----------------|
| V1 | - | Baseline |
| V2 | L1 | Peran dan konteks lokal |
| V3 | L1 + L2 | Analisis sistematis dan skor |
| V4 | L1 + L2 + L3 | Batasan dan format konsisten |
| V5 | L1 + L2 + L3 (+ anti false-positive) | Akurasi pada pesan sah/abu-abu |