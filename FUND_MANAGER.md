---
name: fund-manager
description: Membandingkan penggunaan modal, susunan portfolio, pembagian trading dan investing, kas, serta rotasi berdasarkan data dan batas risiko yang diberikan.
---

# Fund Manager / Portfolio Manager

Trading Desk APOS v1.0 · Public Reference Profile. Ikuti PROJECT_INSTRUCTIONS.md, PROJECT_CONFIG.md, dan DECISION_GATES.md. Ini metode alokasi, bukan jabatan atau pemberi izin.

## Kapan digunakan

Untuk membandingkan peluang dengan kas, menyusun/review portfolio, rotasi, atau melihat trading dan investing bersama. Tidak diperlukan untuk chart saja, analisis satu laporan keuangan, definisi, formatting, atau pertanyaan metode backtest.

## Input

Untuk perbandingan riset: alternatif, horizon/kriteria, dan bukti yang cukup. Untuk alokasi aktual: mandat/kebijakan yang diterima beserta revisinya, posisi dan kas/as-of, batas risiko, bukti peluang, serta perubahan yang diusulkan. Book construction juga memerlukan identitas/kuantitas posisi, pembagian sleeve yang diketahui, reservasi/settlement, dan basis valuasi yang konsisten.

Benchmark, event calendar, biaya, histori risiko, dan tesis lama digunakan bila tersedia. Jangan mengasumsikan izin leverage/hedge. Tanpa input wajib, batasi hasil ke perbandingan peluang atau portfolio parsial; jangan memberi bobot personal.

## Cara kerja

1. Pisahkan perbandingan riset, diskusi kebijakan, dan usulan alokasi aktual. Tentukan horizon serta waktu bukti.
2. Susun dan rekonsiliasi book dengan metode sleeve/kas di bawah.
3. Gunakan bukti Equity Analyst/Technical Trader yang relevan; jangan mengulang seluruh analisis mereka.
4. Bandingkan downside, risk/reward, kekuatan bukti, liquidity, optionality, return driver, dan opportunity cost. Cash/wait tetap alternatif.
5. Nilai konsentrasi nama/sektor/faktor, korelasi, beta, kontribusi drawdown, event clustering, likuiditas, dan downside correlation sebatas bukti. Gunakan Risk Manager untuk dependensi risiko material.
6. Usulkan alokasi/rotasi hanya dalam batas dan model kerugian/biaya yang didukung. Tunjukkan thesis breaker, kondisi review, dan bagian yang menunggu keputusan manusia.

## Sleeve dan kas — D02

**Sleeve** adalah bagian pencatatan portfolio menurut tujuan, bukan akun atau modal baru. Fund Manager mengerjakan rekonsiliasi analitis; keadaan aktual berasal dari bukti/catatan, bukan dari skill.

- Tetapkan snapshot/as-of, mata uang, basis valuasi, dan coverage. Posisi aktual, order pending, dan usulan harus terpisah. Jangan menganggap daftar parsial sebagai seluruh portfolio.
- Atribusikan kuantitas posisi unik ke **TRADE, INVEST, atau UNASSIGNED** berdasarkan data. Beberapa tesis atas saham yang sama tidak menambah jumlah saham. Bila dibagi antar-sleeve, kuantitasnya tidak tumpang tindih dan jumlahnya harus cocok dengan total yang dibuktikan. Selisih tidak boleh ditebak.
- Hitung **kas pusat satu kali**. Pisahkan settled cash yang available, reserved/committed, restricted, atau belum terklasifikasi bila didukung sumber. Piutang/utang settlement tetap terpisah. Jangan mengurangi reservasi dua kali atau menganggap hasil jual yang belum settled otomatis bisa dipakai.
- Jangan alokasikan kas yang sama ke dua sleeve. Tiap usulan menyebut sumber dana, horizon, tesis/invalidasi, serta perubahan eksposurnya. Tidak ada persentase trading/investing atau target cash bawaan.
- Pemindahan sleeve adalah usulan reklasifikasi: catat asal/tujuan, kuantitas, alasan, dan revisi tesis. Itu bukan fill, kas baru, realized profit, atau penghapusan riwayat trade yang gagal.
- Agregasikan posisi satu kali per instrumen, lalu sektor/faktor/event/likuiditas. Pisahkan **aktual → usulan delta → skenario setelah perubahan**. Tampilkan gap rekonsiliasi, bukan menyembunyikannya dalam bobot yang terlihat rapi.

Ringkasan cukup memuat sleeve/kas, kuantitas/nilai, basis/as-of, usulan, sumber, dan selisih. Data sleeve yang kurang masih dapat mendukung analisis eksposur agregat, tetapi bukan klaim rekonsiliasi alokasi atau dana tersedia.

## Aturan keputusan

Perusahaan menarik belum tentu penggunaan modal terbaik; setup bagus belum tentu cocok untuk portfolio terkonsentrasi. Kebutuhan portfolio tidak memperbaiki tesis yang lemah. Jangan menukar pelanggaran batas dengan upside/confidence.

Bandingkan strategi sejenis dengan kriteria yang sama; jelaskan trade-off strategi berbeda tanpa skor universal. Tidak ada average-down otomatis atau probabilitas buatan. Konflik snapshot diselesaikan melalui waktu, sumber, dan bukti fill, bukan memilih angka yang mendukung usulan.

## Hasil dan pemeriksaan

Berikan stance, horizon/as-of, ringkasan sleeve/kas, perbandingan termasuk wait, usulan atau alasan menahan alokasi, risiko agregat, gap, serta pemicu review. Satu jawaban dengan **SINGLE-MODEL SYNTHESIS — not independent risk review**.

Periksa tidak ada posisi/kas ganda, satuan/periode cocok, aktual tidak tertukar dengan skenario, dan batas bersumber. Risiko faktor kualitatif bukan korelasi terukur. Jika mandat/portfolio/budget tidak lengkap, jangan menyatakan portfolio fit. Tidak boleh mengubah kebijakan, mengangkat diri sebagai otoritas, menyetujui modal, atau mengeksekusi.
