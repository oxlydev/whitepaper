# 4 System Architecture

## 4.1 Multi-Chain Design

| Network | Exchange contract | Role |
|---|---|---|
| **BNB Smart Chain** | EVM (Solidity) | Home chain: OXLY token, tokenomics, vesting, airdrop, staking, gas-free trading with OXG, fee discounts, listing registry |
| **Ethereum** | EVM (Solidity) | Spot markets for Ethereum assets |
| **Solana** | Solana program | Spot markets for Solana (SPL) assets |

The entire token economy lives on BNB Smart Chain. Fees earned on Ethereum and Solana are brought to BNB Smart Chain and feed the same OXLY buyback & burn, so growth on any chain adds to OXLY demand.

## 4.2 Components

<figure><img src=".gitbook/assets/en-figure-03.svg" alt="figure"><figcaption><p></p></figcaption></figure>

| Component | Core Responsibility |
|---|---|
| **Exchange Smart Contract** | Serves as the single source of truth. Stores order data, locks assets in escrow, and validates and settles every match and cancellation. |
| **Indexer** | Reads every smart contract event in real time to build order book data, trade history, candlestick charts, and balance updates. |
| **Matching Engine** | Identifies and pairs crossing orders under price-time priority. |
| **Operator** | Submits matched orders to the smart contract (Section 14). |
| **Relayer** | Submits order placement and cancellation transactions whose gas is covered by OXG on BNB Smart Chain (Section 6). |
| **API** | Provides REST, WebSocket, and GraphQL interfaces for client applications, traders, trading bots, and market data aggregators. |
| **Web Application** | A unified interface covering the trading terminal, portfolio management, staking, airdrop claims, the listing portal, Oxly Live, and the developer portal. |
| **Mobile Application** | Native iOS and Android apps with an integrated self-custody wallet. |

{% hint style="info" %}
The protocol's smart contracts are the single source of truth: every wallet balance is verified directly on the blockchain without relying on Oxly servers. Even if the off-chain infrastructure stopped entirely, user assets would remain protected in the smart contracts, and every order could still be cancelled independently through direct on-chain interaction.
{% endhint %}

## 4.3 Contract Suite

| Contract | Network | Core Function |
|---|---|---|
| **Trading** |   |   |
| Oxly | BSC Ethereum Solana | Order book exchange: order placement, escrow, matching, and fees |
| **Token & Distribution** |   |   |
| OxlyToken | BSC | OXLY token: per-allocation quotas, minter authorization, and burn |
| OxlyVesting | BSC | Release schedules for Core Contributors, Foundation & Operations, and Operational Cost |
| OxlyAirdrop | BSC | Cumulative airdrop claims with a fixed quota per session |
| **Staking & Gas Utility** |   |   |
| OxlyStaking | BSC | APY-based OXLY staking rewards |
| OxlyGasStaking | BSC | Staking for OXG capacity and trading fee discount tiers |
| OxlyRelayer | BSC | Gas-free order placement and cancellation |
| **Ecosystem Products** |   |   |
| ListingManager | BSC | Paid token listings for any network |

*The **Oxly** contract runs on BNB Smart Chain and Ethereum, with an equivalent program on Solana. All token, distribution, staking, and ecosystem product contracts are deployed on BNB Smart Chain.*
