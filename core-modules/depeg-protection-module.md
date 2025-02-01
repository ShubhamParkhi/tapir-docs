# Depeg Protection Module

#### **Purpose**

Allows users to hedge against slashing risks (depeg events) or amplify yields by underwriting protection.

#### **Key Features**

* **Capital Efficiency:** Protection is denominated in `wtETH`, ensuring no idle collateral.
* **Dynamic Pricing:** DP/YB tokens trade on an AMM with time-based price adjustments.
* **Epoch-Based Pools:** Protection is offered in fixed-duration pools (e.g., 90-day epochs).

#### **Components**

| Component          | Description                                                                         |
| ------------------ | ----------------------------------------------------------------------------------- |
| **DP\_wtETH**      | Depeg Protected Token: Redeemable 1:1 for `wtETH` if no depeg occurs.               |
| **YB\_wtETH**      | Yield Boosted Token: Absorbs depeg losses but earns premiums from DP sellers.       |
| **Depeg Factory**  | Deploys epoch-specific DP/YB pools (e.g., `DP_wtETH_0624`).                         |
| **Depeg AMM**      | StableSwap-style DEX for swapping DP/YB tokens with price boundaries.               |
| **Depeg Resolver** | Determines depeg status by comparing `wtETH` share prices at initiation vs. expiry. |

#### **Workflow (Lifecycle)**

1. **Pool Initiation:**
   * Factory deploys a new Depeg Pool with a fixed duration (e.g., 90 days).
   * Users split `wtETH` into DP/YB tokens (1:1 ratio).
2. **Active Phase:**
   * Users trade DP/YB tokens on the AMM to hedge or boost yields.
   * Liquidity providers earn fees by adding DP/YB to the AMM.
3. **Resolution:**
   * After expiry, the Depeg Resolver checks for slashing events.
   * **No Depeg:** DP holders redeem 1:1 for `wtETH`; YB holders retain full yield.
   * **Depeg:** YB holders absorb losses (e.g., 10% depeg → YB loses 20%, DP retains full value).

#### **User Strategies**

* **Risk-Averse:** Buy DP tokens to hedge against slashing.
* **Yield Seekers:** Sell DP tokens to earn premiums via YB tokens.
