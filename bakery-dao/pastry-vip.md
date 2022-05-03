# 🎇 PASTRY VIP

### Pastry VIP

With the VIP Pastry NFTs, things get just a slight bit different, but certainly not in a bad way. The VIP NFT tokens are the most exclusive bunch of pastries. They have voting rights in the ecosystem, share revenue generated from all of the content, and have unlimited access to the BakeryDAO.

They also come with their own unique pastry, having individual rarities and components to explore and discover!

![Pastry VIP NFTs](<../.gitbook/assets/image (15) (1).png>)

Holders of these tokens will generate yield in time from the memberships, which they can send to their friends, sell on the secondary market, lend, or do many other things with! These NFTs do not come with an expiration timestamp, but they are deemed valid as memberships via the smart contract we mentioned previously called [ERC721BalanceOfHook](https://github.com/unlock-protocol/unlock/blob/master/smart-contracts/contracts/hooks/ERC721BalanceOfHook.sol).

The magic all happens in this one line of code where it calls the `getHasValidKey` function on the relevant smart contract.

```
const hasValidKey = await lockContract.getHasValidKey(userAddress)
```

In addition to all of this, the Bakery plans to award these token holders with their own BakeryDAO ENS subdomain. This will later be used on the [https://pastry.xyz/](https://pastry.xyz) website where you will have specific permissions only when connected with a valid Ethereum wallet. These can be permissions such as drafting your own post, editing an existing research report, and much more to be announced on a later date...

There will only be 2,222 BakeryDAO tokens. They are **not** live yet, but once they are they will be only for the finest of pastries. The Bakery plans to allocate the majority of the supply to the best subscribers of the pastry NFTs, who have proved their dedication to the BakeryDAO since the very beginning.
