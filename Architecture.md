# Architecture

## **Overview**

Tapir Protocol’s architecture is designed to balance risk management, yield optimization, and capital efficiency. It combines modular components, automated market makers (AMMs), and time-bound pools to create a flexible ecosystem where users retain control over their risk exposure while earning yields.

## **Core Modules**

### **Depeg Protection Module**

This module allows users to hedge against asset devaluations (e.g., slashing, hacks) while retaining yield. Key elements include:

* **Token Splitting**: Users split 1 underlying asset into 0.5 DP (Depeg Protected Asset) and 0.5 YB (Yield Boosted Asset).
* **Depeg Pools**: Time-bound pools (e.g., 90 days) where DP/YB tokens are traded.
* **AMM Integration**: A decentralized exchange for swapping DP and YB tokens, with liquidity providers earning fees.

**Example**:

* Alice splits 100 `sUSDe` into 50 DP and 50 YB. She sells YB to buy more DP, reducing her risk.
* Bob buys YB to amplify his returns, betting no depeg will occur.

***

### **Automated Market Makers (AMMs)**

* **DP/YB AMM**: Facilitates swaps between protection and yield tokens. Uses a stableswap curve to minimize slippage.
* **PT/YT AMM**: Allows trading fixed and variable yield tokens.

