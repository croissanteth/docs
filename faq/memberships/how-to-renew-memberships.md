---
description: Thanks to Unlock Protocol and KeyPurchaser.sol, this is actually possible!
cover: ../../.gitbook/assets/bakerydaoyt.png
coverY: 0
---

# 🗞 How to renew memberships?

The BakeryNFTs have the unique features in that they can be renewed by approving a contract to spend x amount over y time. If the user approves $200 USDC to be spent over any amount of time, the KeyPurchaser.sol contract will grant them time on their BakeryNFT every time it gets close to expiration with keeper bots.

1. The user will need to approve the BakeryNFT to spend the total amount of the memberships from their balance on the ERC20 contract (eg. subscribing to a membership with 12 monthly payments of 5 USDC requires the user to pre-approve a total debit of 60 USDC from its wallet over a year).
2. The user will _need_ perform the “first” purchase on the lock to enable the recurring purchases. At that point (or any other “explicit” purchase by the user) the price AND duration are stored for this user as a “proof” that they agreed to this price/duration (we may in fact store a price/second). Everything else remains the same in that function. (eg. first purchase is a one-off payment of 5 USDc for 1 month)
3. Once this first purchase expires (or is nearly expired - within 5% of expiration date), _anyone_ can call the `renewMembershipFor` function for this user’s key. The function will verify that the price and duration are unchanged from purchase above (or the transaction will fail) and that the ERC20 approval is still sufficient (or the transaction will fail). The `renewMembershipFor` function should use the token id as argument as well as he referrer address (this address will receive Unlock Discount Tokens). This function will first verify that the current membership is nearly expired, and that the price/duration are unchanged. It will then perform the same behavior as a purchase by withdrawing from the key owner’s ERC20 balance and update the duration, as well as callback the Unlock contract to mint UDT. Note: the `onPurchase` hook should be called, as well as the gas refund mechanism. If the transaction succeed, the gas refund is triggered for the `msg.sender`.

###
