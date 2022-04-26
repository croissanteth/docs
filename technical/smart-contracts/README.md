---
description: >-
  An overview of the BakeryDAO smart contracts and their purposes within the
  greater pastry ecosystem.
cover: ../../.gitbook/assets/bakerynft.png
coverY: 0
---

# 🧠 Smart Contracts

Although it seems like it's just an innocent little croissant GIF, it is actually a lot more than that on the back-end. We can't just go running and diving in head first without getting at least somewhat familiar with the Bakery...

![BakeryDAO Ecosystem](../../.gitbook/assets/boards.png)

Underneath the surface, the [BakeryDAO](https://bakery.fyi) consists of more than six main contracts (at the time of this writing). Some of them leverage [Unlock Protocol](https://unlock-protocol.com) for expiring NFTs which act as memberships on the blockchain. In the future there will be many more including governance contracts, as well as even a Bakery ERC-20 token to add on top of these.

The main smart contracts in our case are responsible for keeping track of Bakery NFT ownership by address. These are named:

Unlock.sol -  a factory contract for deploying memberships with many customization parameters

[PublicLock.sol](publiclock.sol.md) - the BakeryNFTs, which we use for token-gating special research pages on the website, and more!

[Pastry.sol](pastry.sol.md) (coming soon) - VIP BakeryDAO members, unlimited subscription to the BakeryDAO, limited supply

**Then there are some miscellaneous contracts we use, that are equally exciting:**

****[SDaoRegistrar.sol](https://github.com/sismo-core/ens-sdao) (coming soon) - kick start your own ENS subdomain DAO with this awesome contract!

[KeyPurchaser.sol](https://github.com/unlock-protocol/unlock/blob/master/smart-contract-extensions/contracts/KeyPurchaserFactory.sol) - used to approve specific addresses to spend a certain amount of x token at x time, useful for credit card purchases, and recurring members.

[ERC721BalanceOfHook.sol](https://github.com/unlock-protocol/unlock/blob/master/smart-contracts/contracts/hooks/ERC721BalanceOfHook.sol) - can be used to determine whether or not an address should be deemed a member based on any custom ERC-721.

Now that we have a basic understanding of what we're dealing with, let's get our hands dirty in some of the important smart contracts that are listed here...

{% content-ref url="publiclock.sol.md" %}
[publiclock.sol.md](publiclock.sol.md)
{% endcontent-ref %}

{% content-ref url="pastry.sol.md" %}
[pastry.sol.md](pastry.sol.md)
{% endcontent-ref %}

