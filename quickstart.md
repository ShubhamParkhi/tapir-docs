# Architecture

### **Overview**

Tapir Protocol is a modular Liquid Restaking Token (LRT) ecosystem designed to enable **tunable risk and yield strategies** for decentralized finance (DeFi) participants. Built on Ethereum, the protocol combines native restaking mechanics with customizable modules for depeg protection and fixed yield, allowing users to tailor their exposure to slashing risks, yield volatility, and leverage.

The architecture is divided into three core modules, supported by a tokenized system (`tETH` and `wtETH`) and governed by factory contracts for pool creation. Below is a detailed breakdown of the protocol's components, workflows, and interactions.

### **Core Modules**

#### **1. LRT Module**

**Purpose:**

* Pool user funds and mint Liquid Restaking Tokens (`tETH`).
* Allocate pooled ETH to restaking networks (e.g., Eigenlayer, Nektar).

**Components:**

* **Rebasing Token (`tETH`):**
  * Automatically adjusts balances to reflect accrued restaking yields.
* **Wrapped Token (`wtETH`):**
  * Non-rebasing ERC-20 wrapper for `tETH`, used in Depeg Protection and Fixed Yield modules.
* **Beacon Oracle:**
  * Reports validator balances from the Ethereum beacon chain to calculate `tETH` rebasing.
* **Pooling Smart Contract:**
  * Handles deposits/withdrawals, mints/burns `tETH`, and allocates funds to restaking strategies.

**Workflow:**

1. Users deposit ETH to mint `tETH`.
2. `tETH` can be wrapped into `wtETH` for use in other modules.
3. Protocol delegates pooled ETH to restaking networks to generate yield.

***

#### **2. Depeg Protection Module**

**Purpose:**

* Allow users to hedge against slashing risks (depeg events) or amplify yields by underwriting protection.

**Components:**

* **Factory Contract:**
  * Deploys epoch-specific Depeg Pools (e.g., `DP_wtETH_0624`, `YB_wtETH_0624`).
* **Depeg Tokens:**
  * **DP\_wtETH (Depeg Protected):** Redeemable 1:1 for `wtETH` if no slashing occurs.
  * **YB\_wtETH (Yield Boosted):** Absorbs depeg losses but earns premiums from DP sellers.
* **Depeg AMM:**
  * StableSwap-style DEX for swapping DP/YB tokens.
  * Implements time-based price shifts and trading boundaries.
* **Depeg Resolver:**
  * Determines if a depeg occurred by comparing `wtETH` share prices at pool initiation vs. expiry.

**Lifecycle:**

1. **Pool Initiation:**
   * Factory creates a Depeg Pool with a fixed duration (e.g., 90 days).
   * Users split `wtETH` into DP/YB tokens (1:1 ratio).
2. **Active Phase:**
   * Users trade DP/YB tokens on the AMM to hedge or boost yields.
3. **Resolution:**
   * After expiry, the Depeg Resolver checks for slashing events.
   * DP holders redeem full value if no depeg; YB holders absorb losses proportionally.

***

#### **3. Fixed Yield Module**

**Purpose:**

* Enable fixed-income strategies or leveraged yield positions.

**Components:**

* **Factory Contract:**
  * Deploys epoch-specific Fixed Yield Pools (e.g., `PT_wtETH_0624`, `IT_wtETH_0624`).
* **Fixed Yield Tokens:**
  * **PT\_wtETH (Principal Token):** Represents fixed yield.
  * **IT\_wtETH (Interest Token):** Represents variable yield.
* **Yield Resolver:**
  * Calculates final yields at expiry based on `wtETH` performance.

**Lifecycle:**

1. **Pool Initiation:**
   * Factory creates a Fixed Yield Pool with a set duration.
   * Users split `wtETH` into PT/IT tokens (1:1 ratio).
2. **Active Phase:**
   * Users trade PT/IT tokens to lock in fixed yields or speculate on variable rates.
3. **Resolution:**
   * At expiry, PT/IT tokens are redeemed for `wtETH` based on accrued yield.
