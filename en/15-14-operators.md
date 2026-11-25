# 14 Operators

Order matching is executed by **operators run by Oxly**, which operate the matching engine infrastructure and submit matches to the smart contract. Operator addresses are registered on-chain through owner multisig authorization and are published on the developer portal. The contract limits what an operator can do, whoever runs it.

### Operator Permissions & Guardrails

| Authorized Actions | Strict Prohibitions |
|---|---|
| Submit match transactions between two crossing orders. | Move funds to anyone other than the two trading parties and the fee recipient. |
| Cancel orders on behalf of the system (with a full refund to the trader). | Execute a trade at a worse price than the trader's limit price. |
| — | Withdraw, hold, or redirect funds stored in the escrow contract. |
