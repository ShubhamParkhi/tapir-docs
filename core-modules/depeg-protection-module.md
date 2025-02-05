# Depeg Protection Module

## **Purpose**

Tapir’s Depeg Protection Module lets you **protect your assets** (like ETH) from losses caused by slashing or hacks—while still earning rewards. Think of it as buying insurance for your crypto, but instead of paying cash, you use your _productive assets_ (which keep generating yield!).

## **How It Works**

**1. Split Your Assets**

* Deposit asset into a Tapir pool.
* For every 1 token you deposit, you get two tokens:
  * **DP Token (Insurance)**: Protects you if the asset’s value drops.
  * **YB Token (Risk Taker)**: Earns extra rewards but absorbs losses if things go wrong.

_Example_: Alice deposits 100 `wtETH` → gets 50 DP + 50 YB.

***

**2. Trade or Hold**

* **Want Safety?** Sell YB tokens to buy more DP. Now you’re fully protected!
* **Chase Higher Rewards?** Buy YB tokens (they’re cheaper) and earn premiums from DP sellers.

_Example_: Bob buys Alice’s YB tokens. If no slashing happens, Bob profits.

***

**3. Wait for the Pool to Expire**

* Each pool lasts a fixed time (e.g., 90 days).
* After expiry, Tapir checks if a depeg (like a slashing event) occurred.

***

**4. Redeem Your Tokens**

* **No Depeg**:
  * Trade **1 DP + 1 YB → 1 token** (you get back your full value).
  * _Alice redeems 50 DP + 50 YB → 100 `wtETH`_.
* **Depeg Happens**:
  * **DP Holders**: Get back 100% of their asset (protected!).
  * **YB Holders**: Lose value proportional to the depeg.
    * _Example_: 10% depeg → YB holders lose 10%, DP stays safe.

⚠️ **Caveat**: If the depeg is **over 50%**, DP protection may adjust (rare edge case).

***

## **Why It’s Better Than Traditional Insurance**

* **No Dead Money**: Your assets stay staked and earn rewards the whole time.
* **You Set the Price**: DP/YB tokens trade freely on a built-in market (AMM), so risk pricing is fair and transparent.
* **Flexible Timeframes**: Choose protection for 30 days, 90 days, etc.

***

## **Who Uses This?**

* **Safety-First Users**: Buy DP tokens to sleep well at night.
* **Risk-Takers**: Buy YB tokens to earn extra rewards.
* **Liquidity Providers**: Earn fees by supplying DP/YB to the AMM.

***

## **Think of it like this**:

* **DP** = Umbrella (keeps you dry in rain).
* **YB** = Betting it won’t rain (cheaper to buy, but you get soaked if it does).

\
