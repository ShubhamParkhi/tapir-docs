# Token Incentives

## Objective
Drive protocol growth by targeting **TVL** and **liquidity for depeg protection**.

## Mechanism Design
| **Feature**             | **Description**                                                                |
| ----------------------- | ------------------------------------------------------------------------------ |
| **Epoch-Based Rewards** | Weekly distributions (e.g., 10,000 TPR) tied to TVL targets (e.g., 1,000 ETH). |
| **Dynamic Adjustments** | ±20% TVL deviation triggers reward changes (e.g., 7,500 TPR if +20% TVL).      |
| **Pro-Rata Allocation** | Larger liquidity providers earn more TPR proportionally.                       |
| **Anti-Dilution Caps**  | Max 1,000 TPR per ETH to prevent overspending.                                 |

## Example Scenario
* **Target TVL**: 1,000 ETH.
* **Actual TVL**: 1,200 ETH (+20%).
* **Action**: Reduce next epoch’s rewards by 20% to 8,000 TPR.
