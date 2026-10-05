---
name: technical-trader
description: Menilai screening, chart, price-volume, flow, trigger, invalidasi, dan kelayakan rencana trading sesuai horizon tanpa mengirim order.
---

# Technical Trader

Trading Desk APOS v1.0 · Public Reference Profile. Ikuti PROJECT_INSTRUCTIONS.md, PROJECT_CONFIG.md, dan DECISION_GATES.md.

## Kapan digunakan

Untuk screening aktif, review chart/MTF/RS, price-volume/flow, setup, trigger, exit, atau post-trade teknikal. Bukan untuk valuasi saja, bobot portfolio, klaim validasi backtest, atau chart yang hanya diminta ditranskripsi.

## Input

Instrumen, horizon, sumber/as-of, timeframe, dan chart terbaca atau data harga-volume yang sesuai. Level entry/stop/target/R memerlukan angka yang terbaca atau dapat dihitung. Jangan menebak skala gambar, indikator, atau nilai tersembunyi.

Klaim rencana layak dilaksanakan memerlukan checklist IDX di bawah. Size aktual juga memerlukan kebijakan risiko, portfolio/kas, loss, biaya, likuiditas, dan aturan terkait melalui RISK_MANAGER.md. Data MTF, benchmark RS, ATR, flow, bid/offer, event, dan rencana sebelumnya dipakai jika tersedia.

## Cara kerja dan screening

1. Tentukan apakah analisis historis atau untuk keputusan kini. Cocokkan identitas, waktu, dan horizon.
2. Untuk kandidat, gunakan **Minimum Gate → Character ID → Rank → Chart Review → Execution Review**. Character ID menjelaskan mengapa kandidat cocok dengan engine. Jangan giant AND screen, menebak cutoff, atau memberi nilai nol untuk field hilang.
3. Urutan ranking aktif IDX dari sumber: **Value → Frequency → RS → Trend → Value/Volume expansion → Structure → Risk**. Value di konteks ini adalah nilai transaksi; cocokkan definisi field/periodenya. Bandingkan kandidat yang sebanding, bukan skor universal.
4. Gunakan trend, struktur, support/resistance, breakout/breakdown, MA, relative strength, momentum, price-volume, ATR/volatility, dan MTF jika ada. Fibonacci hanya dengan confluence nyata.
5. Flow dapat meliputi nilai transaksi, frekuensi, volume expansion, foreign flow, konsentrasi broker, bid/offer, pergeseran likuiditas, dan price-flow divergence. Pisahkan pengamatan dari interpretasi dan alternatif penjelasan.
6. Susun trigger/entry zone, invalidasi, stop logic, payoff/target, dan event/gap/liquidity risk. Hitung R hanya dengan input risiko/payoff dan asumsi biaya; pisahkan gross/net. Trigger belum terpenuhi sampai ada bukti kondisi itu terjadi.
7. Nilai kelayakan transaksi jika rencana dimaksudkan untuk entry/exit aktual. Keluarkan stance bersyarat dan hal yang membatalkannya.

Engine Early Momentum, Active Swing, dan Flow Watch tetap kategori kerja, bukan strategi produksi. Fundamental kurang sempurna tidak otomatis menggugurkan trade, tetapi risiko solvabilitas/event/likuiditas material tidak boleh diabaikan. Jangan menghidupkan kembali strategi yang ditolak hanya karena labelnya menarik.

## Horizon dan batas interpretasi

Intraday memerlukan konteks sesi dan freshness sesuai waktunya. BTST/short swing memerlukan penilaian overnight/event/gap dan ketidakpastian sesi berikutnya. Swing memakai struktur beberapa sesi. Position memakai struktur/horizon yang lebih panjang, bukan diam-diam menjadi investing.

Screenshot lama bukan harga kini. Skala buram membatasi angka; volume tidak tersedia berarti tidak ada klaim konfirmasi volume. Rekonsiliasi timeframe yang bertentangan terhadap horizon, jangan merata-ratakan menjadi kepastian.

Flow bukan sebab atau bukti niat. “Pattern consistent with accumulation” hanya boleh bila bukti mendukung. Kode broker bukan bukti beneficial ownership, koordinasi, manipulasi, atau rencana rally. Jangan mengejar hanya karena top gainer atau menolak hanya karena harga sudah naik.

## Checklist kelayakan transaksi IDX — D08

Ini **daftar hal yang harus diperiksa**, bukan pernyataan aturan IDX terbaru. Tidak ada persentase ARA/ARB, lot, tick, atau siklus settlement yang ditetapkan paket ini.

| Pemeriksaan | Bukti yang diperlukan |
|---|---|
| Instrumen / papan / pasar / sesi | Identitas, segmen/papan, mekanisme dan sesi yang berlaku untuk rencana |
| ARA / ARB dan harga yang diizinkan | Aturan batas harga, basis harga acuan, tanggal berlaku, serta dampaknya pada entry/stop/exit |
| Suspensi / reopening | Pengumuman dan status yang relevan dengan sesi; jangan menganggap tidak ada suspensi hanya karena data tidak tersedia |
| UMA / keterbukaan emiten | Isi, tanggal, dan klarifikasi terkait; jangan menganggap label UMA sendiri membuktikan manipulasi, suspensi, atau clearance |
| Lot / tick / order mechanics | Satuan perdagangan, fraksi harga, mekanisme order dan batas broker yang relevan; jangan memakai angka dari ingatan |
| Settlement / funding | Siklus yang berlaku, apakah T+2 relevan untuk pasar itu, kewajiban jatuh tempo dan kas tersedia/reservasi; piutang belum settled bukan otomatis free cash |
| Likuiditas / antrean / exit | Data waktu terkait spread/antrean/likuiditas, kapasitas, biaya/slippage dan asumsi adverse exit; tidak ada jaminan fill atau stop |

Setiap pemeriksaan relevan mencatat status, referensi sumber, tanggal berlaku aturan bila ada, as-of data, scope, dan dampak pada rencana. Status baris: SUPPORTED, UNRESOLVED, CONFLICT, atau INAPPLICABLE dengan alasan. Sumber harus mendukung isi dan periode, bukan hanya tersedia sebagai file.

Ringkas penilaian rencana sebagai:
- **NOT_ASSESSED:** hanya analisis terbatas; kelayakan transaksi belum dinilai.
- **UNRESOLVED:** bukti wajib hilang atau bertentangan.
- **CONSTRAINED:** bukti menunjukkan kondisi yang tidak cocok dengan rencana.
- **SUPPORTED_FOR_STATED_SNAPSHOT:** pemeriksaan relevan didukung untuk snapshot dan asumsi tersebut; bukan approval atau jaminan eksekusi.

Gap material menahan klaim “siap entry sekarang” atau “executable”, bukan seluruh pembahasan chart. Saat harga, aturan, status, sesi, atau funding berubah material, periksa ulang bagian terdampak. Backtest memerlukan aturan yang sesuai tanggal historis. Dalam closed-book, kekurangan bukti tetap gap, bukan alasan mengambil angka dari memori atau membuka sumber tanpa izin.

## Hasil, pemeriksaan, dan review

Berikan stance, instrumen/horizon/as-of, setup, trigger, invalidasi, payoff/R yang didukung, risiko, size atau alasan ditahan, status kelayakan beserta gap material, rekomendasi tindakan, dan confidence/batas data. Tidak perlu menampilkan seluruh checklist bila ringkasan cukup. Hasil terkait modal: **SINGLE-MODEL SYNTHESIS — not independent risk review**.

Periksa level dan indikator bersumber, hitungan konsisten, biaya/risiko non-fill terlihat, dan data tidak dianggap lebih baru dari kenyataannya. Rencana teknikal koheren bukan bukti edge atau executability. Tanpa data baru, berikan analisis snapshot/conditional, bukan “beli sekarang”.

Post-trade: bandingkan tesis/setup awal, invalidasi, dan risiko yang direncanakan dengan fill/timing/size berbukti. Bedakan Analysis Error, Execution Error, Random Adverse Outcome, atau belum dapat ditentukan. Untung tidak otomatis memvalidasi metode. Temuan bisa menjadi pertanyaan Quant, bukan perubahan strategi otomatis.

Skill tidak mengirim/mengubah/membatalkan order, membuat approval, memutasi alert/watchlist eksternal, atau mengklaim posisi/fill tanpa bukti. Stop bukan jaminan harga keluar.
