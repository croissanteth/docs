---
description: >-
  Thanks to the unique features of web3, we are able to offer a built-in refund
  mechanism, within a specific timeframe of the membership.
---

# ⏪ REFUNDS

If, for any reason you are not satisfied with the content produced by the Chef's, and it is not more than halfway through your membership, it can be "burnt" and the funds will automatically be refunded to your address!

This interface allows any BakeryNFT owner to update elements of the NFT they manage.

The functions that make this possible are listed below, and can be used as reference on the Etherscan Write contract page for the [Bakery NFTs on Ethereum](https://etherscan.io/address/0x61Cc42C66BA9Df72bF6DA89Fcd57215965f74005#writeProxyContract) and the [BakeryNFTs on Optimistic Ethereum](https://optimistic.etherscan.io/address/0x73fc36bA5684655807F60a6437463cC527f50027#code).

![](<../../.gitbook/assets/1 (6).png>)

### `expireAndRefundFor`

In the block explorer, you'll find "`expireAndRefundFor`". The "`_keyOwner (address)"` field is where you enter the wallet address of the person with the key/ membership you would like to make expire. The `amount` field is the amount of the refund, based on the currency it is priced in. By inputting 0, there will be no refund.

A lock manager can invoke this function to expire a key and perform and refund based on the amount specified.

![](<../../.gitbook/assets/image (8) (1).png>)

```
function expireAndRefundFor(
  address _keyOwner,
  uint amount
) external;
```

By updating this field, the key owner will still technically have the NFT, but it will be expired, thus ending the membership and all of its goodness.

### `cancelAndRefund`

Allows a key manager to expire and get a refund for their key, based on the cancellation terms.

```
function cancelAndRefund(uint _tokenId) external;
```

### updateRefundPenalty

Allow a Lock manager to change the refund penalty. The first param is the duration of the free trial in seconds, and the second is the penalty in basis-points.

```
function updateRefundPenalty(
  uint _freeTrialLength,
  uint _refundPenaltyBasisPoints
) external;
```

Let us know if you have any questions on [Discord](https://discord.gg/bakerydao)!
