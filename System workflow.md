---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# System Workflow

1. **Deposit & Restaking:**
   * Users deposit ETH → mint `tETH` → wrap to `wtETH`.
   * Protocol delegates ETH to restaking networks (e.g., Eigenlayer).
2. **Module Interaction:**
   * `wtETH` is split into DP/YB or PT/IT tokens.
   * AMMs facilitate token swaps for risk/yield customization.
3. **Redemption:**
   * After pool expiry, tokens are redeemed based on resolver outcomes.
