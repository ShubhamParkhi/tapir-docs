---
hidden: true
---

# Fixed Yield Module

#### **Purpose**

Enables users to lock in fixed yields or speculate on variable rates through leveraged positions.

#### **Key Features**

* **Yield Tokenization:** Splits `wtETH` into Principal Tokens (PT) and Interest Tokens (IT).
* **Native Integration:** No reliance on third-party protocols for fixed-rate products.
* **Leverage Opportunities:** Users can amplify exposure to variable yields via IT tokens.

#### **Components**

| Component          | Description                                                     |
| ------------------ | --------------------------------------------------------------- |
| **PT\_wtETH**      | Principal Token: Represents fixed yield.                        |
| **IT\_wtETH**      | Interest Token: Represents variable yield.                      |
| **Yield Factory**  | Deploys epoch-specific PT/IT pools (e.g., `PT_wtETH_0624`).     |
| **Yield Resolver** | Calculates final yields at expiry based on `wtETH` performance. |

#### **Workflow (Lifecycle)**

1. **Pool Initiation:**
   * Factory deploys a Fixed Yield Pool with a set duration (e.g., 30 days).
   * Users split `wtETH` into PT/IT tokens (1:1 ratio).
2. **Active Phase:**
   * Users trade PT/IT tokens to lock in fixed yields or speculate on variable rates.
3. **Resolution:**
   * At expiry, the Yield Resolver calculates accrued yield.
   * **Redemption:** PT holders receive fixed yield; IT holders earn variable yield.

#### **User Strategies**

* **Fixed Income:** Hold PT tokens for predictable returns.
* **Leveraged Yield:** Buy IT tokens to amplify exposure to restaking yields.

***

\
