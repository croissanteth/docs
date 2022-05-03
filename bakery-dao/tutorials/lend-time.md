---
description: >-
  This function can optionally be called by the owner of a specific Pastry NFT.
  It transfers time of the NFT membership to the address specified, functioning
  as a "mini membership" for the recipient.
---

# ⏱ LEND TIME

Want to get your friend in on some of the latest alpha, but don't want to sell your NFT? No problem! The Pastry NFT is capable of being shared... This works by instead transferring time for the membership, rather than the actual token when called. Owners of Pastry NFTs can delegate their time to friends, family, or anyone with a Ethereum address through this.

To share time for your membership, visit the Etherscan write smart contract pages for Pastry NFTs on Ethereum, Optimism, or Polygon.

### `shareKey`

This function can be called to transfer some of the time on a membership and do a "partial" transfer.

```
function shareKey(
  address _to,
  uint _tokenId,
  uint _timeShared
) external;
```

**NOTE: this feature is only possible with the expiring 30-day membership NFTs**
