---
description: This function can optionally be called by the owner of a specific BakeryNFT.
cover: ../../.gitbook/assets/bakerydaoyt.png
coverY: 0
---

# 📥 How to lend my membership?

Another unique feature of the BakeryNFT allows it to be shared... This works by instead transferring time for the membership, rather than the actual token when called. Owners of BakeryNFTs can delegate their time to friends, family, or anyone with a Ethereum address through this.

To share time for your membership, visit the Etherscan write smart contract pages for [BakeryNFTs on Ethereum](https://etherscan.io/address/0x61Cc42C66BA9Df72bF6DA89Fcd57215965f74005#writeProxyContract) or [BakeryNFTs on Optimism](https://optimistic.etherscan.io/address/0x73fc36bA5684655807F60a6437463cC527f50027#code).

### `shareKey`

This function can be called to transfer some of the time on a membership and do a "partial" transfer.

```javascript
function shareKey(
  address _to,
  uint _tokenId,
  uint _timeShared
) external;
```
