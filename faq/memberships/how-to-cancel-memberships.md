---
cover: ../../.gitbook/assets/bakerydaoyt.png
coverY: 0
---

# ❌ How to cancel memberships?

This interface allows any BakeryNFT owner to update elements of the NFT they manage.

![Etherscan Write Contract](../../.gitbook/assets/writee.png)

In the block explorer, you'll find "`expireAndRefundFor`". The "`_keyOwner (address)"` field is where you enter the wallet address of the person with the key/ membership you would like to make expire. The `amount` field is the amount of the refund, based on the currency it is priced in. By inputting 0, there will be no refund.

![BakeryNFT Expire Function](../../.gitbook/assets/expireee.png)

By updating this field, the key owner will still technically have the NFT, but it will be expired, thus ending the membership and all of its goodness.