# 14 Operator

Proses pencocokan order (order matching) dieksekusi oleh **operator yang dijalankan oleh Oxly**, yang mengoperasikan infrastruktur matching engine dan mengirimkan hasil pencocokan (match) ke smart contract. Alamat operator didaftarkan secara on-chain melalui otorisasi multisig owner dan dipublikasikan di portal developer. Kontrak membatasi apa yang dapat dilakukan operator, siapa pun yang menjalankannya.

### Batasan Kewenangan (Permissions & Guardrails) Operator

| Kewenangan yang Diizinkan (Authorized Actions) | Batasan Mutlak (Strict Prohibitions) |
|---|---|
| Mengirimkan transaksi match antara dua order yang saling bersilangan (crossing orders). | Memindahkan dana ke pihak mana pun selain kepada kedua pihak yang bertransaksi dan alamat penerima biaya (fee recipient). |
| Membatalkan order atas nama sistem (dengan pengembalian dana sepenuhnya ke akun trader). | Mengeksekusi transaksi pada tingkat harga yang lebih buruk daripada harga limit yang ditetapkan trader. |
| — | Menarik, menahan, maupun mengalihkan dana yang tersimpan di dalam kontrak escrow. |
