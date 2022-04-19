---
description: >-
  Looking for how to begin on your journey with the BakeryDAO? You're in the
  right place. The following is an in-depth startup guide to the pastry
  ecosystem.
cover: .gitbook/assets/bakerynft.png
coverY: 0
---

# 🔥 Getting Started

## BakeryDAO <a href="#bakerydao" id="bakerydao"></a>

The Bakery is a decentralized community powered by web 3.0. Pastry NFTs act as "platform-less" memberships on the blockchain, granting members access to more than seven different applications for the Bakery. Using cryptographic signatures + a bit of web3 magic, we provide exclusive DeFi research.

Thanks to the simplicity of "Sign In With Ethereum," we are able to do all of this in a UX that is unmatched! Check out an example on our website below:

![](<.gitbook/assets/disgif (1).gif>)

Holders of Bakery NFTs are the owners of the ecosystem, able to vote on a growing number of parameters as the protocol decentralizes. In the future, these NFTs may even entitle some users to a portion of revenue generated.

Pastries are able to contribute to the research provided in the Bakery, create their own profile, build up their reputation, and benefit from their effort.&#x20;

**There are two "tiers" for memberships**.&#x20;

Pastry NFTs are 30-Day membership NFTs, that expire and may be renewed whenever. These are an ERC-721 just like any other NFT, with an added expirationDuration() value we use to determine whether users are valid members or not. Pastry NFTs are deployed on Ethereum, Optimism, and Polygon.

They have an unlimited supply, are available on demand, but must be renewed in order to be a valid pastry!

![](<.gitbook/assets/Untitled design (3).png>)

Next, we have the Pastry VIP NFTs. These are non-expiring, exclusive pastry NFTs that are the rarest of them all!

![](<.gitbook/assets/Untitled design (2).png>)

![](.gitbook/assets/IMG\_8438.PNG)

The goal with this is to build up a powerful group of researchers, builders, and thought leaders with the help of digital ownership and crypto-economic incentives!

Our community will be inclined to share content and help research, while the Chef's will be incentivized to create their best work. **It's a powerful combination.**

So far, the Bakery NFTs are currently integrated with:

| MAINNET                                                | OPTIMISM                                       | POLYGON                                       |
| ------------------------------------------------------ | ---------------------------------------------- | --------------------------------------------- |
| [https://pastry.xyz/](https://pastry.xyz)              | [https://pastry.xyz/](https://pastry.xyz)      | [https://pastry.xyz](https://pastry.xyz)      |
| [discord](https://discord.gg/bakerydao)                | [discord](https://discord.gg/bakerydao)        | [discord](https://discord.gg/bakerydao)       |
| [discourse](https://bake.community)                    | (coming soon)                                  | (coming soon)                                 |
| [newsletter](https://bakerydao.me/newsletter/)         | [newsletter](https://bakerydao.me/newsletter/) | [newsletter](https://bakerydao.me/newsletter) |
| [telegram](https://alpha.guild.xyz/bakerydao-telegram) | (coming soon)                                  | (coming soon)                                 |
| [shopify](https://shop.pastry.xyz)                     | [shopify](https://shop.pastry.xyz)             | (coming soon)                                 |
| snapshot                                               | snapshot                                       | (coming soon)                                 |
| land                                                   | land                                           | (coming soon)                                 |
| notion                                                 | notion                                         | (coming soon)                                 |

#### **Deployments** <a href="#deployments" id="deployments"></a>

|                            |                                                             ADDRESS                                                            |
| :------------------------: | :----------------------------------------------------------------------------------------------------------------------------: |
|    **MAINNET (30-DAY)**    |      [0x61Cc42C66BA9Df72bF6DA89Fcd57215965f74005](https://etherscan.io/address/0x61Cc42C66BA9Df72bF6DA89Fcd57215965f74005)     |
|    **OPTIMISM (30-DAY)**   | [0x73fc36bA5684655807F60a6437463cC527f50027](https://optimistic.etherscan.io/token/0x73fc36bA5684655807F60a6437463cC527f50027) |
|    **POLYGON (30-DAY)**    |    [0x253Ff450fa62e8c7916Ce5Ea08e312681c5C7485](https://polygonscan.com/address/0x253Ff450fa62e8c7916Ce5Ea08e312681c5C7485)    |
| **BAKERY DAO (NO EXPIRY)** |                                                       **TO BE ANNOUNCED**                                                      |

Each application that we integrate our NFTs with needs to know whether or not a user has a valid NFT to grant them access to locked content. For the applications to know this, they simply read a keccak256 signature from the relevant Ethereum address once connected to see if they have the token, and grant access if so. This process is completely secure, takes seconds to do, and does not incur gas fees!

![](.gitbook/assets/chrome\_2V4pgEEMnY.png)

#### **The best part about all of this?** <a href="#features" id="features"></a>

* You don't need a bank account to get started
* We don't need to ask for your name, address, social security number, or any other private details
* You don't need to purchase with a credit card (although you certainly still can if you'd like to)
* You **** can **own your content** (send the time of your membership to your mom, or lend it on the secondary market)
* You can get instantaneous memberships bound to no platform
* There are no third-party processing fees
* Infinite number of future integrations to await

**NFTs are far more than art, and we hope that the Bakery DAO serves as a great example for that fact.**

The BakeryDAO effectively token-gates special research content (and alpha) on certain pages across the website, secret discord channels, community-powered forums, newsletters, videos, Shopify, LAND in Decentraland, airdrops, and much more behind NFTs. This is in hopes to gather the best researchers, builders, and doers in DeFi.

### TRY IT NOW!

{% embed url="https://codepen.io/croissantt/pen/mdqWBPB" %}

Do you think you have what it takes?

![30-DAY SUBSCRIPTION](<.gitbook/assets/30-DAY BLUE.gif>)

## Not so fast, anon!

Let's have a look at the mechanics of the ecosystem and its features, so we can have a better idea of how it all works...
