# System Workflow

#### 1. **Pool Creation**

* **Factory Contracts**: Automatically generate new Depeg Pools and associated tokens.
* **Time-Bound Design**: Each pool has an expiry date, ensuring structured risk periods.

#### 2. **User Interaction**

* **Deposit & Split**: Users deposit asset into a pool, receiving DP/YB or PT/YT tokens.
* **Trading**: Adjust risk exposure by swapping tokens on AMMs.
* **Liquidity Provisioning**: Supply tokens to AMMs to earn fees.

#### 3. **Depeg Resolution**

* **Expiry Check**: After a pool expires, the protocol checks if the asset’s value dropped below its initial price.
* **Redemption**:
  * **No Depeg**: Redeem 1 DP + 1 YB → 1 Token.
  * **Depeg Event**: DP holders receive compensation proportional to the loss (e.g., +10% for a 10% depeg).

#### 4. **Yield Distribution**

* Rebasing assets automatically distributes yields to holders.
* Fixed yields for Principal Token holders are paid from protocol revenues.
