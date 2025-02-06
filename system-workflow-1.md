# System Workflow

### 1. **Pool Creation**

* **Factory Contracts**: Automatically deploy new Depeg Pools and their associated DP/YB tokens.
* **Time-Bound Design**: Each pool has a predefined expiry date (e.g., 90 days), ensuring structured risk periods and predictable resolution.

***

### 2. **User Interaction**

#### **Deposit & Split**

* Users deposit asset into a Depeg Pool.
* For every 1 asset deposited, they receive **0.5 DP** (Depeg Protected) asset and **0.5 YB** (Yield Boosted) asset.

#### **Trading**

* Adjust risk exposure by swapping DP and YB tokens on the integrated **Depeg AMM**:
  * **Risk-Averse Users**: Sell YB to buy more DP, maximizing protection.
  * **Yield Seekers**: Buy discounted YB to amplify potential returns.

#### **Liquidity Provisioning**

* Users supply DP/YB tokens to the AMM to earn trading fees.

***

### 3. **Depeg Resolution**

#### **Expiry Check**

* After the pool expires, the protocol checks if the asset price dropped below its initial value (depeg event).

#### **Redemption**

* **No Depeg**:
  * Redeem **1 DP + 1 YB → 1 token** (full value).
  * Example: Alice redeems 100 DP + 100 YB → 100 token.
* **Depeg Event**:
  * **DP Holders**: Fully protected against losses (redeem 1 DP → 1 token).
  * **YB Holders**: Absorb all losses (redeem 1 YB → token value adjusted for depeg).

***

### 4. **Yield Distribution**

* **Rebasing**: Automatically distributes rewards to holders (e.g., staking yields from Eigenlayer).
* **YB Holders**: Earn premiums from DP buyers via AMM swaps, enhancing their effective yield.

***

### **Key Advantages**

* **Full Protection for DP Holders**: Zero loss on depeg events (up to 50% depeg).
* **Dynamic Risk Pricing**: AMM-driven markets ensure fair pricing of DP/YB tokens.
* **Non-Custodial Safety**: Users retain control of assets at all times.

***

\
