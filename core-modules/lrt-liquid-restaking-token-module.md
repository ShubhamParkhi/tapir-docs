---
hidden: true
---

# LRT (Liquid Restaking Token) Module

#### **Purpose**

The LRT Module serves as the foundational layer of Tapir Protocol, enabling users to pool ETH and mint Liquid Restaking Tokens (`tETH`). These tokens represent restaked ETH across multiple networks (e.g., Eigenlayer, Nektar) and automatically accrue staking rewards.

#### **Key Features**

* **Rebasing Mechanism:** `tETH` balances adjust dynamically to reflect accrued yields.
* **Wrapped Token (`wtETH`):** A non-rebasing ERC-20 wrapper for `tETH`, designed for use in Depeg Protection and Fixed Yield modules.
* **Capital Allocation:** Pooled ETH is delegated to restaking networks to maximize yield generation.

#### **Components**

| Component            | Description                                                                |
| -------------------- | -------------------------------------------------------------------------- |
| **`tETH`**           | Native rebasing token representing restaked ETH.                           |
| **`wtETH`**          | Wrapped, non-rebasing ERC-20 token for stable value representation.        |
| **Beacon Oracle**    | Fetches validator balances from Ethereum’s beacon chain to update `tETH`.  |
| **Pooling Contract** | Manages ETH deposits/withdrawals, mints/burns `tETH`, and allocates funds. |

#### **Workflow**

1. **Deposit:** Users deposit ETH to mint `tETH`.
2. **Wrapping:** `tETH` can be wrapped into `wtETH` for stable value retention.
3. **Restaking:** Protocol delegates ETH to restaking networks to generate yields.
4. **Withdrawal:** Users burn `tETH`/`wtETH` to redeem ETH (subject to unlock periods).

#### **User Actions**

* **Mint `tETH`:** Deposit ETH into the pooling contract.
* **Wrap/Unwrap:** Convert between `tETH` and `wtETH`.

***

\
