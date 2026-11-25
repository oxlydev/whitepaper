# 4 Arsitektur Sistem

## 4.1 Desain Multi-Chain

| Jaringan | Kontrak exchange | Peran |
|---|---|---|
| **BNB Smart Chain** | EVM (Solidity) | Chain utama: token OXLY, tokenomics, vesting, airdrop, staking, trading tanpa gas OXG, diskon fee, registri listing |
| **Ethereum** | EVM (Solidity) | Market spot untuk aset Ethereum |
| **Solana** | Program Solana | Market spot untuk aset Solana (SPL) |

Seluruh ekonomi token berada di BNB Smart Chain. Fee yang diperoleh di Ethereum dan Solana dibawa ke BNB Smart Chain dan masuk ke buyback & burn OXLY yang sama, sehingga pertumbuhan di chain mana pun menambah permintaan OXLY.

## 4.2 Komponen

<figure><img src=".gitbook/assets/id-figure-03.svg" alt="figure"><figcaption><p></p></figcaption></figure>

| Komponen | Tanggung Jawab Utama |
|---|---|
| **Smart Contract Exchange** | Bertindak sebagai sumber kebenaran utama (single source of truth). Menyimpan data order, mengunci aset di dalam escrow, serta memvalidasi dan menyelesaikan setiap pencocokan (matching) maupun pembatalan order. |
| **Indexer** | Memindai setiap event dari smart contract secara real-time untuk menyusun data order book, riwayat transaksi, grafik candlestick, dan pembaruan saldo. |
| **Matching Engine** | Mengidentifikasi dan mencocokkan order yang beririsan (crossing orders) berdasarkan prioritas harga dan waktu pemasangan (price-time priority). |
| **Operator** | Mengirimkan eksekusi pencocokan order ke smart contract (Bab 14). |
| **Relayer** | Mengirimkan transaksi penempatan dan pembatalan order yang biayanya ditanggung menggunakan OXG pada jaringan BNB Smart Chain (Bab 6). |
| **API** | Menyediakan antarmuka REST, WebSocket, dan GraphQL untuk kebutuhan aplikasi klien, trader, bot trading, serta agregator data pasar. |
| **Aplikasi Web** | Antarmuka terpadu yang mencakup terminal trading, manajemen portofolio, staking, klaim airdrop, portal listing, Oxly Live, dan portal pengembang (developer). |
| **Aplikasi Mobile** | Aplikasi native untuk iOS dan Android yang dilengkapi dompet self-custody terintegrasi. |

{% hint style="info" %}
Smart contract protokol merupakan sumber kebenaran tunggal (single source of truth), di mana seluruh saldo dompet diverifikasi langsung dari blockchain tanpa bergantung pada server Oxly. Bahkan jika infrastruktur off-chain berhenti beroperasi sepenuhnya, aset pengguna tetap terlindungi di dalam smart contract dan setiap order tetap dapat dibatalkan secara mandiri melalui interaksi langsung on-chain.
{% endhint %}

## 4.3 Rangkaian Kontrak

| Kontrak | Jaringan | Fungsi Utama |
|---|---|---|
| **Perdagangan** |   |   |
| Oxly | BSC Ethereum Solana | Exchange order book: penempatan order, escrow, matching, dan fee |
| **Token & Distribusi** |   |   |
| OxlyToken | BSC | Token OXLY: kuota per alokasi, otorisasi minter, dan burn |
| OxlyVesting | BSC | Jadwal rilis Core Contributors, Foundation & Operations, dan Operational Cost |
| OxlyAirdrop | BSC | Klaim airdrop kumulatif dengan kuota tetap per sesi |
| **Staking & Utilitas Gas** |   |   |
| OxlyStaking | BSC | Reward staking OXLY berbasis APY |
| OxlyGasStaking | BSC | Staking untuk kapasitas OXG dan tier diskon biaya trading |
| OxlyRelayer | BSC | Penempatan dan pembatalan order tanpa biaya gas |
| **Produk Ekosistem** |   |   |
| ListingManager | BSC | Listing token berbayar untuk jaringan mana pun |

*Kontrak **Oxly** berjalan di BNB Smart Chain dan Ethereum, dengan program padanan di Solana. Seluruh kontrak token, distribusi, staking, dan produk ekosistem berada di BNB Smart Chain.*
