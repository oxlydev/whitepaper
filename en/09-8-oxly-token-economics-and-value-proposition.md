# 8 OXLY Token Economics and Value Proposition

## 8.1 Core Token Parameters

### Key Metrics

* **Maximum Supply: 1,000,000,000** — OXLY (fixed, permanent cap)
* **Initial Circulating Supply at TGE: ≈ 0** — OXLY (no pre-mint)
* **Presale & Venture Capital Allocation: 0%** — No private funding round
* **Ecosystem & Community Allocation: 65%** — Of total supply

### Token Technical Specifications

| Parameter | Protocol Specification |
|---|---|
| Name & Ticker | Oxly / **OXLY** |
| Contract Standard | BEP-20 on BNB Smart Chain · 18 decimals · Supports EIP-2612 gas-free approvals (`permit`) |
| Minting Model | On-demand minting per allocation, strictly controlled by smart contracts that enforce quota caps and vesting schedules |
| Burn Mechanism | Anyone may permanently burn their own OXLY; every burn automatically reduces `totalSupply()` and is accumulated in the `totalBurned` variable |

### Fair Launch Manifesto

{% hint style="info" %}
**No presale. No VCs. Fixed supply. Community-owned. Market-priced.**<br>No presale allocation. No venture capital investors. A fixed maximum supply. Owned by the community. Valuation determined entirely by the market.
{% endhint %}

## 8.2 OXLY Ecosystem Utility

| Utility Category | How OXLY Is Used |
|---|---|
| **Trading Fee Discounts** | Staking OXLY in Oxly Gas Staking provides spot trading fee discounts of 5% to 100% on BNB Smart Chain. |
| **Gas-Free Trading** | Staking OXLY in Oxly Gas Staking generates OXG capacity to execute trades on BNB Smart Chain without BNB; OXG capacity can also be delegated to trading bots or secondary wallets. |
| **Staking Yield** | Users earn rewards of up to 24% APY through the Oxly Staking contract with no lock-up. |
| **Listing Payment** | The only currency accepted for token listing submissions on all three networks, at a fee of 50,000 OXLY. |
| **Oxly Live Currency** | Used for Live Developer broadcast fees (15,000 OXLY), digital gifts, and incentive payouts to valid viewers and hosts. |
| **Gas Shortfall Compensation (OXG Shortfall)** | Serves as automatic payment when OXG capacity is insufficient at order placement; all OXLY paid this way is burned permanently. |
| **Airdrop Distribution** | Used for allocations to Fairlaunch participants. |

## 8.3 Ten Structural Token Advantages

1. ****Zero Insider Allocation**.** No presale, no private funding round, and no special allocation for venture capital investors.
2. ****Permanent Maximum Supply Cap**.** Total supply is permanently capped at 1,000,000,000 OXLY, enforced by the smart contract as the absolute sum of all allocation quotas.
3. ****No Pre-Mint (Realization-Based Minting)**.** Circulating supply increases only when an allocation is actually distributed or claimed, removing the risk of an idle treasury that could be dumped on the market.
4. ****Strict On-Chain Quota Segregation**.** Each allocation has its own quota cap and mint counter in the contract, ensuring that ecosystem sub-allocations can never be mixed or shifted between pools.
5. ****Unbreakable Team Vesting Lock**.** Minter contracts for scheduled allocations are permanently locked (immutable), so vesting schedules cannot be accelerated or modified by anyone, including the contract owner.
6. ****Revenue-Backed Deflation**.** 80% of spot trading fee revenue across all three networks is allocated to buyback & burn, reinforced by burning 50% of listing fees, part of Live Developer fees, and 100% of OXG shortfall payments.
7. ****Natural Decline of the Effective Supply Cap**.** Rewards or airdrop allocations not claimed before their deadline are never minted, so the effective maximum supply can only move below the 1 billion cap.
8. ****Organic Demand Across Every Product Line**.** Spot trading, listing submissions, OXG capacity, and the Oxly Live ecosystem all directly drive demand for, or lock-up of, OXLY.
9. ****Fair, Merit-Based Distribution**.** The largest share of initial distribution goes directly to active users based on real contribution through trading, social participation, and referrals.
10. ****Comprehensive On-Chain Transparency**.** Minting per allocation, total tokens burned (`totalBurned`), and circulating supply (`totalSupply`) can be verified directly from the smart contract, and every burn is published with its transaction hash.
