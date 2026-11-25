# A–F Lampiran

## A. Glosarium

| Istilah | Arti |
|---|---|
| Ask / Bid | Order jual / order beli |
| Base / Quote | Aset yang diperdagangkan / aset untuk harga (mis. OXLY / USDT) |
| Escrow | Dana yang ditahan kontrak untuk order terbuka |
| Maker / Taker | Order yang lebih dulu / yang belakangan dalam suatu match |
| Operator · Relayer | Pengirim match ke kontrak · pengirim order tanpa gas yang membayar gasnya |
| OXG | Kapasitas gas yang terisi ulang dari Oxly Gas Staking, tidak bisa ditransfer |
| EGF · TGE | Ecosystem Growth Fund · Token Generation Event (25 Nov 2026 00:00 UTC) |
| Free float | OXLY beredar yang tidak tertahan di staking atau treasury |
| Bulan kontrak | 365/12 hari |

## B. Rumus

| | Nama | Rumus |
|---|---|---|
| **APY** | ****APY Staking****<br>*Bab 10.1* | APY = min(24%, (40.000.000 OXLY) ÷ (Total Stake)) |
| **OXG** | ****Rate OXG****<br>*Bab 6.2* | capPerOxly = min(baseRate, dailyBudget ÷ totalActiveStake) |
| **REC** | ****Pemulihan OXG****<br>*per jam* | Pemulihan = (Kapasitas OXG) ÷ 24 |
| **SF** | ****Biaya Kekurangan OXG****<br>*feePerGas ≤ maxFeePerGas* | Fee = max(0, Biaya Gas − OXG Tersedia) × feePerGas |
| **LD** | ****Reward Live Developer****<br>*per penonton pemenang* | Reward = (15.000 OXLY × 90%) ÷ 100 = 135 OXLY |
| **LK** | ****Reward Live Komunitas****<br>*untuk host utama* | Reward = Penonton Valid × 10 OXLY × Pengali Tier |
| **BB** | ****Buyback Tahunan****<br>*Bab 12.4* | BB = Volume Spot Harian × 365 × 0,2% × 80% |
| **SB** | ****Supply Beredar****<br>*Bab 11.3* | Supply Beredar = totalMinted − totalBurned |

## C. Pengukuran Gas (BNB Smart Chain)

| Operasi | Gas | Dibayar oleh |
|---|---:|---|
| placeAskToken (biasa / pertama) | 157.842 / 192.042 | Trader |
| placeBid quote token (biasa / pertama) | 177.845 / 212.045 | Trader |
| placeAskNative · placeBid quote BNB | 154.296 · 138.068 | Trader |
| cancelOrder (open / partial) | 61.555 / 66.306 | Trader |
| matchOrders (penuh tanpa fee / dengan fee / sebagian) | 142.508 / 184.756 / 172.720 | Operator |
| Relay ask / bid · relay cancel | 225.824 / 235.861 · 113.112 | Relayer (trader memakai OXG) |
| Gas Staking: stake pertama · delegasi 1 hari | 132.862 · 265.054 | Staker |
| ListingManager: submit · approve | 215.997 · 142.046 | Proyek · operator listing |

## D. Tenggat Klaim Airdrop

| Sesi | Sesi Berakhir (UTC) | Tenggat Klaim (UTC) |
|---|---|---|
| Sesi 1 | 24 Feb 2027, 06:00 | **25 Mei 2027, 06:00** |
| Sesi 2–8 | Ditetapkan pada pengumuman masing-masing sesi | 90 hari setelah sesi berakhir |

## E. Alamat Kontrak

{% hint style="info" %}
Alamat kontrak resmi di BNB Smart Chain, Ethereum, dan Solana dipublikasikan di portal developer Oxly. **Selalu verifikasi alamat di portal resmi sebelum berinteraksi dengan kontrak.**
{% endhint %}

## F. Referensi

1. TechCrunch, “Crypto exchange Bybit says it was hacked and lost around $1.4 billion”, 21 Feb 2025.<br>[https://techcrunch.com/2025/02/21/crypto-exchange-bybit-says-it-was-hacked-and-lost-around-1-4-billion](https://techcrunch.com/2025/02/21/crypto-exchange-bybit-says-it-was-hacked-and-lost-around-1-4-billion)
2. TechCrunch, “Hackers stole over $2.7 billion in crypto in 2025, data shows”, 23 Des 2025.<br>[https://techcrunch.com/2025/12/23/hackers-stole-over-2-7-billion-in-crypto-in-2025-data-shows/](https://techcrunch.com/2025/12/23/hackers-stole-over-2-7-billion-in-crypto-in-2025-data-shows/)
3. CNBC, “$6.3 billion Binance hack is largest crypto theft on record”, 29 Okt 2026.<br>[https://www.cnbc.com/2026/10/29/circle-tether-freeze-funds-impacted-by-potential-binance-security-issue.html](https://www.cnbc.com/2026/10/29/circle-tether-freeze-funds-impacted-by-potential-binance-security-issue.html)
4. Bloomberg, “Binance Suspends Deposits, Withdrawals After $6.3 Billion Hack Shakes Industry”, 29 Okt 2026.<br>[https://www.bloomberg.com/news/articles/2026-10-29/binance-founder-says-possible-hack-of-exchange-bitcoin-falls](https://www.bloomberg.com/news/articles/2026-10-29/binance-founder-says-possible-hack-of-exchange-bitcoin-falls)
5. KuCoin News (data DefiLlama), “BNB Chain leads public chains with 4.86 million 24-hour active addresses”, Nov 2026.<br>[https://www.kucoin.com/news/flash/bnb-chain-leads-public-chains-with-4-86-million-24-hour-active-addresses](https://www.kucoin.com/news/flash/bnb-chain-leads-public-chains-with-4-86-million-24-hour-active-addresses)
6. Altrady (data DefiLlama), “Solana vs Ethereum DEX Volume: Monthly Data 2024–2026”.<br>[https://www.altrady.com/blog/crypto-trading-strategies/solana-volume-overtakes-ethereum-2026](https://www.altrady.com/blog/crypto-trading-strategies/solana-volume-overtakes-ethereum-2026)
7. Coin Edition (data CoinGecko), “Ethereum, BNB Chain and Solana Capture Three Quarters of Global DEX Volume”, 2026.<br>[https://coinedition.com/ethereum-bnb-chain-and-solana-capture-three-quarters-of-global-dex-volume/](https://coinedition.com/ethereum-bnb-chain-and-solana-capture-three-quarters-of-global-dex-volume/)
8. DefiLlama, “DEX Volume by Chain”.<br>[https://defillama.com/dexs/chains](https://defillama.com/dexs/chains)
9. BscScan, “BNB Smart Chain Gas Tracker” (0,05 gwei, 18 Nov 2026).<br>[https://bscscan.com/gastracker](https://bscscan.com/gastracker)
10. CoinMarketCap, “BNB price analysis” (BNB ≈ $557,55, 22 Nov 2026).<br>[https://coinmarketcap.com/cmc-ai/bnb/price-analysis/](https://coinmarketcap.com/cmc-ai/bnb/price-analysis/)
