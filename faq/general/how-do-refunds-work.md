---
description: >-
  Thanks to the unique features of web3, we are able to offer a built-in refund
  mechanism, within a specific timeframe of the membership.
cover: ../../.gitbook/assets/bakerynft.png
coverY: 0
---

# 🤬 How do refunds work?

If, for any reason you are not satisfied with the content produced by the Chef's, and it is not more than halfway through your membership, it can be "burnt" and the funds will automatically be refunded to your address!

The functions that make this possible are listed below, and can be used as reference on the Etherscan Write contract page for the [Bakery NFTs on Ethereum](https://etherscan.io/address/0x61Cc42C66BA9Df72bF6DA89Fcd57215965f74005#writeProxyContract) and the [BakeryNFTs on Optimistic Ethereum](https://optimistic.etherscan.io/address/0x73fc36bA5684655807F60a6437463cC527f50027#code).

### `expireAndRefundFor`

A lock manager can invoke this function to expire a key and perform and refund based on the amount specified.

```javascript
function expireAndRefundFor(
  address _keyOwner,
  uint amount
) external;
```

### `cancelAndRefund`

Allows a key manager to expire and get a refund for their key, based on the cancellation terms.

```javascript
function cancelAndRefund(uint _tokenId) external;
```

### `updateRefundPenalty`

Allow a Lock manager to change the refund penalty. The first param is the duration of the free trial in seconds, and the second is the penalty in basis-points.

```javascript
function updateRefundPenalty(
  uint _freeTrialLength,
  uint _refundPenaltyBasisPoints
) external;
```

Let us know if you have any questions on [Discord](https://discord.gg/bakerydao)!
