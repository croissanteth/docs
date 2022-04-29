---
description: This function can optionally be called by the owner of a specific BakeryNFT.
---

# ⏱ LEND TIME

Another unique feature of the BakeryNFT allows it to be shared... This works by instead transferring time for the membership, rather than the actual token when called. Owners of Pastry NFTs can delegate their time to friends, family, or anyone with a Ethereum address through this.

To share time for your membership, visit the Etherscan write smart contract pages for Pastry NFTs on Ethereum or Pastry NFTs on Optimism.

### `shareKey`

This function can be called to transfer some of the time on a membership and do a "partial" transfer.

```
function shareKey(
  address _to,
  uint _tokenId,
  uint _timeShared
) external;
```
