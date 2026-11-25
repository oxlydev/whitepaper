# A–F Appendices

## A. Glossary

| Term | Meaning |
|---|---|
| Ask / Bid | Sell order / buy order |
| Base / Quote | The asset being traded / the asset used for pricing (e.g. OXLY / USDT) |
| Escrow | Funds held by the contract for open orders |
| Maker / Taker | The earlier / the later order in a match |
| Operator · Relayer | Submits matches to the contract · submits gas-free orders and pays their gas |
| OXG | Regenerating, non-transferable gas capacity from Oxly Gas Staking |
| EGF · TGE | Ecosystem Growth Fund · Token Generation Event (28 Nov 2026 00:00 UTC) |
| Free float | Circulating OXLY not held in staking or the treasury |
| Contract month | 365/12 days |

## B. Formulas

| | Name | Formula |
|---|---|---|
| **APY** | ****Staking APY****<br>*Section 10.1* | APY = min(24%, (40,000,000 OXLY) ÷ (Total Stake)) |
| **OXG** | ****OXG Rate****<br>*Section 6.2* | capPerOxly = min(baseRate, dailyBudget ÷ totalActiveStake) |
| **REC** | ****OXG Recovery****<br>*per hour* | Recovery = (OXG Capacity) ÷ 24 |
| **SF** | ****OXG Shortfall Fee****<br>*feePerGas ≤ maxFeePerGas* | Fee = max(0, Gas Cost − Available OXG) × feePerGas |
| **LD** | ****Live Developer Reward****<br>*per winning viewer* | Reward = (15,000 OXLY × 90%) ÷ 100 = 135 OXLY |
| **LC** | ****Live Community Reward****<br>*for the main host* | Reward = Valid Viewers × 10 OXLY × Tier Multiplier |
| **BB** | ****Annual Buyback****<br>*Section 12.4* | BB = Daily Spot Volume × 365 × 0.2% × 80% |
| **CS** | ****Circulating Supply****<br>*Section 11.3* | Circulating Supply = totalMinted − totalBurned |

## C. Gas Measurements (BNB Smart Chain)

| Operation | Gas | Paid by |
|---|---:|---|
| placeAskToken (regular / first) | 157,842 / 192,042 | Trader |
| placeBid quote token (regular / first) | 177,845 / 212,045 | Trader |
| placeAskNative · placeBid quote BNB | 154,296 · 138,068 | Trader |
| cancelOrder (open / partial) | 61,555 / 66,306 | Trader |
| matchOrders (full without fee / with fee / partial) | 142,508 / 184,756 / 172,720 | Operator |
| Relay ask / bid · relay cancel | 225,824 / 235,861 · 113,112 | Relayer (trader uses OXG) |
| Gas Staking: first stake · 1-day delegation | 132,862 · 265,054 | Staker |
| ListingManager: submit · approve | 215,997 · 142,046 | Project · listing operator |

## D. Airdrop Claim Deadlines

| Session | Session Ends (UTC) | Claim Deadline (UTC) |
|---|---|---|
| Session 1 | 27 Feb 2027, 06:00 | **28 May 2027, 06:00** |
| Sessions 2–8 | Set in each session's announcement | 90 days after the session ends |

## E. Contract Addresses

{% hint style="info" %}
Official contract addresses on BNB Smart Chain, Ethereum, and Solana are published on the Oxly developer portal. **Always verify addresses on the official portal before interacting with any contract.**
{% endhint %}

## F. References

1. TechCrunch, “Crypto exchange Bybit says it was hacked and lost around $1.4 billion”, 21 Feb 2025.<br>[https://techcrunch.com/2025/02/21/crypto-exchange-bybit-says-it-was-hacked-and-lost-around-1-4-billion](https://techcrunch.com/2025/02/21/crypto-exchange-bybit-says-it-was-hacked-and-lost-around-1-4-billion)
2. TechCrunch, “Hackers stole over $2.7 billion in crypto in 2025, data shows”, 23 Dec 2025.<br>[https://techcrunch.com/2025/12/23/hackers-stole-over-2-7-billion-in-crypto-in-2025-data-shows/](https://techcrunch.com/2025/12/23/hackers-stole-over-2-7-billion-in-crypto-in-2025-data-shows/)
3. CNBC, “$6.3 billion Binance hack is largest crypto theft on record”, 29 Oct 2026.<br>[https://www.cnbc.com/2026/10/29/circle-tether-freeze-funds-impacted-by-potential-binance-security-issue.html](https://www.cnbc.com/2026/10/29/circle-tether-freeze-funds-impacted-by-potential-binance-security-issue.html)
4. Bloomberg, “Binance Suspends Deposits, Withdrawals After $6.3 Billion Hack Shakes Industry”, 29 Oct 2026.<br>[https://www.bloomberg.com/news/articles/2026-10-29/binance-founder-says-possible-hack-of-exchange-bitcoin-falls](https://www.bloomberg.com/news/articles/2026-10-29/binance-founder-says-possible-hack-of-exchange-bitcoin-falls)
5. KuCoin News (DefiLlama data), “BNB Chain leads public chains with 4.86 million 24-hour active addresses”, Nov 2026.<br>[https://www.kucoin.com/news/flash/bnb-chain-leads-public-chains-with-4-86-million-24-hour-active-addresses](https://www.kucoin.com/news/flash/bnb-chain-leads-public-chains-with-4-86-million-24-hour-active-addresses)
6. Altrady (DefiLlama data), “Solana vs Ethereum DEX Volume: Monthly Data 2024–2026”.<br>[https://www.altrady.com/blog/crypto-trading-strategies/solana-volume-overtakes-ethereum-2026](https://www.altrady.com/blog/crypto-trading-strategies/solana-volume-overtakes-ethereum-2026)
7. Coin Edition (CoinGecko data), “Ethereum, BNB Chain and Solana Capture Three Quarters of Global DEX Volume”, 2026.<br>[https://coinedition.com/ethereum-bnb-chain-and-solana-capture-three-quarters-of-global-dex-volume/](https://coinedition.com/ethereum-bnb-chain-and-solana-capture-three-quarters-of-global-dex-volume/)
8. DefiLlama, “DEX Volume by Chain”.<br>[https://defillama.com/dexs/chains](https://defillama.com/dexs/chains)
9. BscScan, “BNB Smart Chain Gas Tracker” (0.05 gwei, 18 Nov 2026).<br>[https://bscscan.com/gastracker](https://bscscan.com/gastracker)
10. CoinMarketCap, “BNB price analysis” (BNB ≈ $557.55, 22 Nov 2026).<br>[https://coinmarketcap.com/cmc-ai/bnb/price-analysis/](https://coinmarketcap.com/cmc-ai/bnb/price-analysis/)
