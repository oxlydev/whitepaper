# 15 Security & Governance

## 15.1 Contract-Enforced Guarantees

Oxly's smart contract architecture is designed with permanent, code-level guardrails that protect user assets from any abuse of authority:

* **Absolute Escrow Protection:** User escrow funds cannot be accessed or withdrawn by anyone, including the protocol owner. The owner's rescue function is strictly limited to recovering tokens sent to the contract address by mistake and never touches user escrow balances.
* **Unconditional Order Cancellation:** Users can always cancel their orders, including while the exchange is paused.
* **Hard Fee Cap:** Transaction fees are permanently capped in the contract at a maximum of 1% per side (maker or taker).
* **Immutable Supply Discipline:** Per-allocation quotas, the fixed supply cap, and the permanent lock on scheduled minter contracts (immutable vesting) are enforced entirely by smart contract code.
* **Relayer Execution Limits:** Every gas-free order requires the user's EIP-712 cryptographic signature, including an expiration deadline and a maximum fee cap.
* **Wrapped Native Fallback:** If a recipient rejects or fails to receive a native token transfer (such as BNB or ETH), the contract automatically converts and delivers the funds in wrapped form (WBNB or WETH), preventing transaction failure or locked funds (denial-of-service).

## 15.2 Owner Role & Multisig Governance

Administrative control of the protocol smart contracts is held by a **multisig** wallet. Within the boundaries permitted by the contract code, the owner has the following operational powers:

| Administrative Power | Purpose & Scope |
|---|---|
| Pause / Unpause the Exchange | An emergency measure to temporarily halt new order placement and match execution (order cancellation remains fully available to users). |
| Register Operators and Relayers | Registers the operator and relayer addresses on-chain. |
| Set Discount Tiers, Listing Fees, and Oxly Live Fees | Adjusts the ecosystem's commercial parameters to stay competitive with market conditions. |
| Set OXG Budget and Fee Parameters | Aligns OXG capacity allocation and compensation rates with fluctuations in network gas costs. |
| Manage EGF and Future Airdrop Minters | Controls token minting authorization within fixed quota caps and the distribution rules set out in Section 9. |

All operational parameter changes are announced publicly before they take effect. By contrast, all scheduled release allocations (vesting schedules) are **permanent and cannot be changed, accelerated, or redirected by the owner**.

## 15.3 Security Practices

To ensure end-to-end infrastructure resilience, Oxly applies layered security testing:

* **Code Review and Automated Testing:** Comprehensive audits and code reviews of the exchange contracts, listing mechanism, OXLY token contract, and OXG utility system—with every finding fixed and covered by an automated test suite.
* **Explicit Attack Scenario Simulation:** Contracts are tested specifically against DeFi exploit vectors, including flash-staking manipulation, capacity draining through delegation, order ID replay attacks, fee-on-transfer token mismatches, and disruption of native payment delivery.
* **Public Bug Bounty Program:** An open bug bounty program invites independent security researchers to continuously identify and report potential vulnerabilities.
