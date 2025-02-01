# Token Uses & Mechanisms

Governance

* **Voting Rights**: Token holders decide on treasury allocations, protocol upgrades, and partnerships.

#### Protocol Fees

| **Fee Type**       | **Rate** | **Mechanism**                                                      |
| ------------------ | -------- | ------------------------------------------------------------------ |
| **Withdrawal Fee** | 0.5%     | Applied when users withdraw ETH via `withdraw()`.                  |
| **Success Fee**    | 1%       | Charged on `rebase()`; 1% of rewards diverted to the DAO treasury. |

#### Burn Mechanism

1. **Fee Collection**: 50% of protocol fees swapped to TPR via DEX.
2. **Burn Execution**: TPR tokens sent to a dead address.
3. **Impact**: Deflationary pressure increases token scarcity.
