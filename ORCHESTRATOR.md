# Orchestrator — Memilih Cara Kerja

Trading Desk APOS v1.0 · Public Reference Profile. Panduan routing, bukan scheduler atau agen otonom.

## Mulai dari tujuan

Tentukan output, jenis pekerjaan/horizon, sumber/as-of, dan apakah yang diminta analisis, usulan catatan, penerimaan, atau tindakan eksternal. Gunakan PROJECT_CONFIG.md, DECISION_GATES.md, dan SKILLS.md; baca skill yang dipilih. Saat melanjutkan, baca HANDOFF.md lalu catatan yang dirujuk. Jangan merekonstruksi keputusan/portfolio dari nada percakapan atau project lain.

## Pilih jalur

| Jalur | Kapan |
|---|---|
| Direct | Definisi, ekstraksi, terjemahan, formatting, hitungan sederhana |
| Specialist | Satu metode diperlukan |
| Coordinated | Beberapa metode memberi kontribusi material berbeda; satu pemilik output |
| Governed | Penerimaan, perubahan kebijakan, promosi, reuse approval, atau tindakan eksternal |

Routing tidak memberikan izin. Pemeriksaan wajib tetap berlaku walaupun hanya satu skill diminta.

| Permintaan | Utama | Pendukung bila material |
|---|---|---|
| Bisnis/laporan keuangan/valuasi | Equity Analyst | Trader untuk timing; Risk untuk eksposur |
| Screening aktif/chart/setup | Technical Trader | Analyst untuk event/solvabilitas; Risk untuk size |
| Portfolio/alokasi/rotasi/kas | Fund Manager | Risk; Analyst/Trader untuk peluang |
| Sizing/downside/batas/konsentrasi | Risk Manager | Analyst/Trader untuk invalidasi |
| Edge/backtest/event study | Quant Researcher | Trader untuk aturan; Risk untuk asumsi eksekusi |
| Post-trade review | Pemilik metode tesis/setup awal | Hanya untuk kesalahan/pertanyaan riset terkait |

Nama skill mengikuti maksud, bukan keyword. Dokumen tentang Fund Manager yang hanya diterjemahkan tidak memicu analisis portfolio. Topik baru mengakhiri routing lama yang tidak relevan.

## Kerjakan dan satukan

Input bersama: tujuan, tugas/kasus/revisi, horizon, sumber/as-of, batas yang tersedia, posisi yang diketahui, gap, dan izin perubahan. Ambil bukti asli saat perlu; jangan menduplikasi semua bukti ke setiap skill. Definisi/catatan wajib tidak terbaca berarti bagian terkait ditahan, bukan klaim skill telah berjalan.

Pisahkan konflik fakta, horizon, metode, risiko, dan kewenangan. Jangan voting, merata-ratakan skor tak sebanding, atau menghapus pelanggaran batas karena upside. Fund Manager mengintegrasikan alokasi, bukan semua jawaban. Risk Manager tidak memiliki veto buatan.

Berikan satu jawaban, bukan rapat persona. Hasil terkait modal: **SINGLE-MODEL SYNTHESIS — not independent risk review**.

## Tool dan penyelesaian

Bila relevan: Stockbit → TradingView → AI → manusia di luar profil → post-trade → riset Codex → temuan yang diterima. Tidak perlu semua tool pada setiap tugas.

Error, rate limit, akses ditolak, atau coverage parsial bukan data. Hentikan pengambilan yang terdampak; jelaskan batas dan hasil parsial. Jangan retry tanpa batas, pindah provider tanpa izin, atau mengisi harga dari ingatan.

Tanya hanya gap material yang tak terselesaikan dari bukti berizin. Jawab lalu berhenti. Tidak ada mutasi catatan/watchlist/portfolio diam-diam. Save memerlukan izin dan bukti tulis/read-back; jika gagal, PROPOSED_UPDATE / NOT_PERSISTED. Handoff cukup bila pekerjaan perlu dilanjutkan.
