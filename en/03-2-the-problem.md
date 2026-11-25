# 2 The Problem

## 2.1 Custodial Risk on Centralized Exchanges

Centralized exchanges (CEXs) offer deep order book liquidity and fast execution, but they require users to deposit assets into wallets fully controlled by the exchange operator. This concentration of custody creates a single point of failure that has become the primary target of hacks in the crypto industry:

* **February 2025 · Bybit: $1.5 Billion** — A cold wallet breach resulted in the theft of $1.5 billion in ETH [1].
* **Full Year 2025 · Industry Total: $2.7 Billion** — A record total value of crypto assets lost to hacks over the year [2].
* **29 October 2026 · Binance: $6.3 Billion** — The largest security incident on record; it affected client assets and forced the suspension of deposits and withdrawals [3][4].

In every one of these incidents, users had no direct control over the recovery of their assets. Decisions on freezes, losses, and compensation rested entirely with the exchange operator. Users also cannot verify in real time that their balances are fully backed by reserves. "Not your keys, not your coins" is not just a community slogan—it reflects a real structural risk.

{% hint style="info" %}
**Oxly's Architectural Solution:** The Oxly protocol removes the centralized wallet that attracts attackers. All user funds stay in each user's self-custodial wallet or are locked, in isolation, in the escrow smart contract for active orders, and can be withdrawn at any time simply by cancelling the related order.
{% endhint %}

## 2.2 Structural Limitations of Liquidity Pool (AMM) DEXs for Traders

Most decentralized trading today runs on Automated Market Makers (AMMs). While AMMs enable permissionless trading, their architecture has fundamental limitations for active and institutional traders:

* **No Native Limit Orders.** Traders cannot place an order at a specific price and wait for the market to fill it.
* **Prices Set by the Pool Curve.** Execution prices are determined by the liquidity ratio inside the pool rather than by direct agreement between traders. As a result, large trades are prone to significant slippage.
* **No Order Book Transparency.** Traders cannot observe market depth at each price level or execute traditional market making strategies with precision.
* **Exposure to Front-Running and MEV.** Swaps broadcast to the public mempool are prime targets for Maximal Extractable Value (MEV) extraction, including sandwich attacks that worsen users' execution prices.

## 2.3 Gas Fees as an Onboarding Barrier

Every on-chain interaction requires the network's native token. A new user who receives a token cannot trade it until they hold BNB, ETH, or SOL to pay for transactions. On an order book, this gas cost recurs with every order placement and cancellation, which discourages active trading and market making.

## 2.4 Token Distribution Favoring Insiders

Many exchange tokens launch with presale, venture capital, and team allocations that dominate supply. The gradual unlocking of these allocations creates persistent selling pressure. In addition, there is often no mechanism that directly ties the platform's operating revenue to the value of its token.

## 2.5 Limited Listing Options for New Projects

* **Centralized Exchanges (CEX):** The exchange decides which tokens may list. The process requires manual approval, takes a long time, and carries fees that usually exceed the means of early-stage projects.
* **AMM-Based DEXs:** Although permissionless, trading only happens against a liquidity pool. To keep price impact low, projects must lock large amounts of capital in a two-asset pair, exposing that capital to impermanent loss.
* **Conventional Order Book Exchanges:** Order book protocols that allow self-listing remain rare. On most platforms, opening a new market still depends on manual review and addition by the exchange's internal team.
