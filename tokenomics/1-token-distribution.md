# Token Distribution

### Overview  

The Tapir token (TPR) is distributed across six categories to balance liquidity, growth, and long-term alignment.  

### Allocation Details  
| **Category**              | **Allocation** | **Lockup/Vesting**           | **Purpose**                                                               |
| ------------------------- | -------------- | ---------------------------- | ------------------------------------------------------------------------- |
| **Token Public Sale**     | 30%            | Immediate unlock             | Open sales to the public via platforms (e.g., exchanges, launchpads).     |
| **Token Presale**         | 10%            | Locked (terms vary)          | Early investor access with tailored lockups to prevent market flooding.   |
| **Protocol Partnerships** | 10%            | 2-year linear vest           | Strategic partners receive tokens to ensure commitment and collaboration. |
| **Core Team & Advisors**  | 20%            | 1-year cliff + 1-year linear | Align team incentives with protocol success.                              |
| **Incentives**            | 20%            | 1-year lock                  | Rewards for liquidity providers, stakers, and early contributors.         |
| **Reserve**               | 10%            | Treasury-held                | Emergency funds, strategic initiatives, or future protocol upgrades.      |

### Pie Chart Visualization  

![](https://i.imgur.com/n401fjc.png)  

### Technical Implementation

- **Public/Presale**: Tokens minted upon purchase and transferred to buyer wallets.  
- **Partnerships/Team**: Tokens held in escrow with vesting logic enforced by timelock contracts.  
- **Incentives**: Rewards distributed via claimable contracts with built-in lockups.  