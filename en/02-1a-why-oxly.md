# 1A Why Oxly

## 1A.1 Why Trade on Oxly

1. ****Full Self-Custody**.** Oxly never holds user assets. In spot markets, assets remain in the user's own wallet, and only the funds for active orders are locked, in isolation, in the Oxly escrow smart contract. In futures markets, margin is deposited into the Oxly futures vault smart contract—not an exchange wallet—with balances and positions recorded on a verifiable on-chain ledger and withdrawals that always require the user's cryptographic signature. This architecture removes the risk of exchange-wallet hacks, freezes, and misuse of funds. Users can cancel orders at any time and recover their escrowed funds in the same transaction, even while the protocol is paused.
2. ****Activity-Based OXLY Incentives**.** Users earn OXLY directly from the 150,000,000 OXLY Fair Launch airdrop through trading volume, content about Oxly, and referrals. All volume on OXLY trading pairs counts double.
3. ****Direct Multi-Network Access, No Registration**.** Trading takes place directly on BNB Smart Chain, Ethereum, and Solana using the wallets and assets users already hold—no bridging, centralized deposits, account creation, or KYC.
4. ****Guaranteed Execution Price and Anti-MEV Protection**.** Users set their own limit price. The protocol's smart contract guarantees that an order is never executed at a worse price than its limit, protecting traders from the slippage manipulation and sandwich attacks common on AMMs. Order matching is performed by operators under price-time priority rather than mempool ordering, eliminating the opening for front-running.
5. ****Trading Without Holding a Gas Token**.** On BNB Smart Chain, Oxly Gas (OXG) covers the full gas cost of placing and cancelling orders, so users can start trading without first acquiring BNB.
6. ****Early Access to New Token Markets**.** Through permissionless listing, new projects can launch their tokens on Oxly early and trade on an order book market from day one.
7. ****Spot and Perpetual Futures in One Platform**.** Spot trading across three major networks alongside USDT-margined perpetual futures with up to 1000x leverage, cross and isolated margin, and Take Profit / Stop Loss (TP/SL) risk management, all in one integrated platform.
8. ****Competitive Fees, Capped in the Contract**.** Standard fees are 0.1% maker and 0.1% taker, with a maximum fee of 1% permanently locked in the smart contract. OXLY stakers in Oxly Gas Staking receive trading fee discounts of 5% to 100% on BNB Smart Chain.
9. ****Cross-Device Connectivity**.** Native iOS and Android apps with an integrated self-custody wallet, plus QR-code authentication for secure access to the web interface.
10. ****On-Chain Transparency and Auditability**.** Every step of the activity cycle—order creation, matching, and cancellation—is recorded as a public transaction that can be independently verified on a block explorer.

## 1A.2 Why Hold OXLY

### OXLY value drivers

1. ****Broad Utility Demand**.** OXLY is required across the platform: Oxly Gas Staking (gas-free OXG and 5%–100% fee discounts), Oxly Staking (up to 24% APY), token listing fees (50,000 OXLY), and Oxly Live broadcast slots (15,000 OXLY). Because listing and broadcast fees are denominated in OXLY, token demand does not shrink as the price rises. With a limited initial supply coming from the community airdrop (Section 12.3), every OXLY that is staked or spent leaves market circulation—driving demand higher while tightening circulating supply as the user base grows.
2. ****Buyback and Burn from All Network Activity**.** 80% of total spot trading fee revenue on BNB Smart Chain, Ethereum, and Solana is allocated to buying back OXLY on the open market, which is then burned permanently. In addition, 50% of every listing fee, part of each Live Developer fee, and all OXG shortfall fees are also burned, and every burn transaction is published together with its transaction hash.
3. ****Community Growth Through Social Campaigns**.** The Fair Launch airdrop distributes OXLY rewards to participants who actively publish and promote Oxly on X (Twitter). Each post reaches the participant's followers, continually drawing in new participants and widening the holder base. This growing exposure also opens the door to new investors who acquire OXLY on the open market (Section 13.6).
4. ****Value Expansion as the Ecosystem Grows**.** Every developer who lists a token or takes part in an Oxly Live broadcast brings a new community into the ecosystem. Rising trading volume, listing activity, and live sessions continuously drive OXLY purchases, staking, and burns.
5. ****Limited and Deflationary Supply**.** Maximum supply is fixed at 1,000,000,000 OXLY with no pre-mint. Rewards that are never claimed are never minted, while every burn is permanent, so the effective supply cap keeps shrinking and burns offset new emissions on a steadily declining schedule.
6. ****Community-Owned**.** No presale, no private round, and no venture capital. Almost all early holders are users who earned OXLY through real contribution to the ecosystem, while the team allocation is locked under a six-year vesting schedule.

### Growth Potential (Illustrative; full model and assumptions in Section 12 and Appendix G)

OXLY value dynamics are determined by the ratio between the tokens absorbed from market circulation and the new supply entering circulation. Supply absorption does not depend on burns alone; it is supported by five main channels:

| Absorption Channel | Mechanism | Base Case Projection, Month 12 |
|---|---|---|
| **Long-Term Staking** | Oxly Staking (APY yield) and Oxly Gas Staking (OXG generation and trading fee discounts) | ±48,000,000 OXLY locked |
| **Long-Term Holders** | Airdrop participants and investors who choose to hold OXLY | ±24,000,000 OXLY (assuming 55% of the airdrop is not sold; part of it staked) |
| **Listing and Oxly Live Fees** | 50,000 OXLY per listing and 15,000 OXLY per Live Developer session, acquired from the market | ±3,200,000 OXLY |
| **Buyback & Burn** | 80% of spot trading fees from all three networks; every $1,000,000 of daily volume generates ±$584,000 per year | ±$430,000 accumulated buyback funds |
| **New Investor Accumulation** | Capital inflow from new buyers on the open market | ±$308,000 per month |

In the base case, these mechanisms hold roughly half of all released OXLY out of free circulation (free float ±48%). At the same time, scheduled emission declines gradually from 69,000,000 OXLY in the first year to below 14,000,000 OXLY per year from year seven onward.

Together, this structure creates positive demand pressure on OXLY that strengthens as platform adoption grows. Nevertheless, the market price is determined entirely by supply and demand and can move both up and down. Holder benefits are described further in Section 8.2.

## 1A.3 Why List on Oxly

* **Permissionless Listing** — No exchange gatekeepers, negotiations, or waiting lists. The entire review process is automated.
* **Low, Transparent Fees** — The listing fee is a fixed OXLY amount published in advance (currently 50,000 OXLY), uniform across all three networks.
* **Order Book Market from Day One** — Tokens trade immediately on a full order book with limit orders, rather than relying solely on an AMM liquidity pool.
* **Capital Efficiency with Limited Liquidity** — Orders placed around the market price absorb trading volume with minimal price impact (Section 7.3).
* **Full Control of Liquidity** — Developers can provide liquidity on one or both sides of the market, set precise price levels, and change or withdraw liquidity at any time with no impermanent loss.
* **Three Major Networks** — List directly on BNB Smart Chain, Ethereum, or Solana according to the token's native ecosystem—no bridging or wrapping required.
* **Transparent Automated Audit** — Contract security checks—honeypot detection, transfer tax, and token authorities—run automatically, and the results are recorded on-chain as a safety indicator for traders.
* **Direct Exposure Through Oxly Live** — Live Developer sessions reach the active trading community directly, and the 100 viewers with the longest engagement receive OXLY rewards (Section 7.4).
* **Market Data Aggregator Integration** — TradingView charting, a public API, and CoinGecko- and CoinMarketCap-compatible endpoints ensure broad visibility and tracking of the token's market data.
