---
description: >-
  Thanks to the unique features of web3, we are able to offer a built-in refund
  mechanism, within a specific timeframe of the membership.
---

# ⏪ REFUNDS

If, for any reason you are not satisfied with the content produced by the Chef's, and it is not more than halfway through your membership, it can be "burnt" and the funds will automatically be refunded to your address!

This interface allows any Pastry NFT owner to update elements of the NFT they manage.

The functions that make this possible are listed below, and can be used as reference on the Etherscan Write contract page for the Pastry[ NFTs on Ethereum](https://etherscan.io/address/0x61Cc42C66BA9Df72bF6DA89Fcd57215965f74005#writeProxyContract), the Pastry [NFTs on Optimistic Ethereum](https://optimistic.etherscan.io/address/0x73fc36bA5684655807F60a6437463cC527f50027#code), and the Pastry [NFTs on Polygon](https://app.unlock-protocol.com/checkout?redirectUri=https://pastry.xyz\&paywallConfig=%7B%0A%20%20%22pessimistic%22%3A%20%22false%22%2C%0A%20%20%22locks%22%3A%20%7B%0A%20%20%20%20%220x253Ff450fa62e8c7916Ce5Ea08e312681c5C7485%22%3A%20%7B%0A%20%20%20%20%20%20%22network%22%3A%20137%2C%0A%20%20%20%20%20%20%22name%22%3A%20%22PASTRY%22%0A%20%20%20%20%7D%0A%20%20%7D%2C%0A%20%20%22icon%22%3A%20%22https%3A%2F%2Fbakery.fyi%2Fwp-content%2Fuploads%2F2022%2F03%2FUnlock-WordMark.png%22%2C%0A%20%20%22callToAction%22%3A%20%7B%0A%20%20%20%20%22default%22%3A%20%22This%20membership%20comes%20with%20a%20unique%20pastry%20NFT%2C%20with%20many%20capabilities.%22%2C%0A%20%20%20%20%22expired%22%3A%20%22Oh%20no!%20Your%20Croissant%20is%20expired.%20You%27ll%20need%20to%20renew%20it%20to%20use%20it%20again.%22%0A%20%20%7D%0A%7D).

![Etherscan Pastry NFT Smart Contract Page](<../../.gitbook/assets/1 (6).png>)

### `expireAndRefundFor`

In the block explorer, you'll find "`expireAndRefundFor`". The "`_keyOwner (address)"` field is where you enter the wallet address of the person with the key/ membership you would like to make expire. The `amount` field is the amount of the refund, based on the currency it is priced in. By inputting 0, there will be no refund.

A Pastry NFT manager can invoke this function to expire a key and perform and refund based on the amount specified.

![expireAndRefundFor Function](<../../.gitbook/assets/image (8) (1).png>)

```
function expireAndRefundFor(
  address _keyOwner,
  uint amount
) external;
```

By updating this field, the Pastry NFT owner will still technically have the NFT, but it will be expired, thus ending the membership and all of its goodness.

### `cancelAndRefund`

Allows a Pastry NFT manager to expire and get a refund for their key, based on the cancellation terms.

```
function cancelAndRefund(uint _tokenId) external;
```

### updateRefundPenalty

Allow a Pastry NFT manager to change the refund penalty. The first param is the duration of the free trial in seconds, and the second is the penalty in basis-points.

```
function updateRefundPenalty(
  uint _freeTrialLength,
  uint _refundPenaltyBasisPoints
) external;
```

Let us know if you have any questions on [Discord](https://discord.gg/bakerydao)!
