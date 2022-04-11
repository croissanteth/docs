---
description: The "Unlock.sol" contract and how its used for the Bakery
cover: ../../.gitbook/assets/bakerynft.png
coverY: 0
---

# 🔓 Unlock.sol

![](../../.gitbook/assets/unlock-word-mark.svg)

This is the Unlock "factory" contract **(**[**Unlock.sol**](https://github.com/unlock-protocol/unlock/blob/master/smart-contracts/contracts/Unlock.sol)**),** which has several key roles for the characteristics of the Bakery NFTs. It has control over the following:

* **Deploying Locks**: Locks are deployed through the Unlock smart contract. This is important because the Locks will actually invoke the Unlock smart contract when keys are sold and the Unlock smart contract will check that the invoking lock has been deployed through it.
* **Keeping Track of the Unlock Discount Tokens**. Unlock Discount Tokens are ERC20 tokens which implement the Unlock network referral program to let users of the protocol govern it. The Discount Tokens are granted when keys (NFTs) are purchased.

### DEPLOYMENTS

| NETWORKS |                                                              ADDRESS                                                             |
| :------: | :------------------------------------------------------------------------------------------------------------------------------: |
|  MAINNET |       [0x3d5409cce1d45233de1d4ebdee74b8e004abdd13](https://etherscan.io/address/0x3d5409cce1d45233de1d4ebdee74b8e004abdd13)      |
| OPTIMISM | [0x99b1348a9129ac49c6de7F11245773dE2f51fB0c](https://optimistic.etherscan.io/address/0x99b1348a9129ac49c6de7F11245773dE2f51fB0c) |

Next, we'll cover **PublicLock.sol**, which is where it gets even more interesting...
