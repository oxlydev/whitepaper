# 15 Keamanan & Tata Kelola (Security & Governance)

## 15.1 Jaminan Kriptografis yang Ditegakkan Kontrak (Contract-Enforced Guarantees)

Arsitektur smart contract Oxly dirancang dengan pembatasan hak akses (guardrails) yang bersifat permanen di level kode untuk melindungi aset pengguna dari risiko penyalahgunaan kewenangan:

* **Perlindungan Mutlak Dana Escrow:** Dana escrow pengguna tidak dapat diakses maupun ditarik oleh pihak mana pun, termasuk owner protokol. Fungsi pemulihan aset (rescue function) yang dimiliki owner dibatasi secara ketat hanya untuk menarik token yang terkirim secara tidak sengaja ke alamat kontrak, tanpa menyentuh saldo escrow pengguna.
* **Jaminan Fungsi Pembatalan (Unconditional Order Cancellation):** Fungsi pembatalan order (cancel) senantiasa dapat dieksekusi oleh pengguna setiap saat, termasuk ketika status operasional exchange sedang dijeda sementara (paused).
* **Batas Atas Tarif Biaya (Hard Fee Cap):** Tarif biaya transaksi dibatasi secara permanen di dalam kontrak maksimal sebesar 1% per sisi (maker maupun taker).
* **Disiplin Supply yang Tidak Dapat Diubah:** Seluruh kuota per kategori alokasi, batas maksimal supply tetap (fixed supply cap), serta kunci permanen pada kontrak minter berjadwal (immutable vesting) ditegakkan sepenuhnya oleh kode smart contract.
* **Batasan Eksekusi Relayer:** Seluruh pengiriman order tanpa biaya gas mewajibkan tanda tangan kriptografis pengguna berstandar EIP-712 yang dilengkapi parameter tenggat kedaluwarsa (expiration deadline) serta batas maksimal potongan biaya (maximum fee cap).
* **Mekanisme Cadangan Pembayaran Native (Wrapped Native Fallback):** Apabila alamat penerima menolak atau gagal menerima transfer token native jaringan (seperti BNB atau ETH), kontrak secara otomatis mengonversi dan menyalurkan dana tersebut dalam bentuk versi wrapped-nya (WBNB atau WETH) guna mencegah kegagalan transaksi maupun penguncian dana (denial-of-service).

## 15.2 Peran dan Batasan Kewenangan Owner (Owner Role & Multisig Governance)

Kendali administratif atas smart contract protokol dikelola melalui dompet **multisig**. Di dalam koridor batasan yang diizinkan oleh kode kontrak, owner memiliki kewenangan operasional berikut:

| Kewenangan Administratif | Tujuan & Cakupan Operasional |
|---|---|
| Menjeda / Mengaktifkan Kembali Exchange (Pause / Unpause) | Langkah mitigasi darurat untuk menghentikan penempatan order dan eksekusi match baru sementara waktu (fungsi pembatalan order tetap terbuka sepenuhnya bagi pengguna). |
| Mendaftarkan Operator dan Relayer | Mendaftarkan alamat operator dan relayer secara on-chain. |
| Mengatur Tier Diskon, Biaya Listing, dan Oxly Live | Menyesuaikan parameter komersial ekosistem agar tetap kompetitif terhadap dinamika pasar. |
| Mengatur Anggaran dan Parameter Biaya OXG | Menyelaraskan alokasi kapasitas dan tarif kompensasi OXG dengan fluktuasi biaya gas jaringan. |
| Mengelola Minter Alokasi EGF dan Future Airdrop | Mengatur otorisasi mint token dalam batas kuota tetap serta aturan distribusi yang ditetapkan pada Bab 9. |

Seluruh perubahan parameter operasional diumumkan secara terbuka kepada publik sebelum diberlakukan. Sebaliknya, seluruh alokasi rilis berjadwal (vesting schedule) bersifat **permanen dan tidak dapat diubah, dipercepat, maupun dialihkan oleh owner**.

## 15.3 Praktik Keamanan dan Audit (Security Practices)

Untuk memastikan ketahanan infrastruktur secara menyeluruh, Oxly menerapkan protokol pengujian keamanan berlapis:

* **Peninjauan Kode dan Pengujian Otomatis:** Audit dan peninjauan kode menyeluruh terhadap kontrak exchange, mekanisme listing, kontrak token OXLY, serta sistem utilitas OXG—di mana setiap temuan telah diperbaiki dan dilindungi oleh rangkaian pengujian otomatis (automated test suite).
* **Simulasi Skenario Serangan Eksplisit:** Pengujian ketahanan kontrak secara spesifik terhadap berbagai vektor eksploitasi DeFi, meliputi manipulasi flash-staking, pengurasan kapasitas melalui celah delegasi, penggunaan ulang ID order (replay attacks), ketidakcocokan token fee-on-transfer, serta gangguan pengiriman pembayaran native.
* **Program Bug Bounty Publik:** Penyelenggaraan program bug bounty terbuka bagi peneliti keamanan independen untuk mengidentifikasi dan melaporkan potensi kerentanan secara berkelanjutan.
