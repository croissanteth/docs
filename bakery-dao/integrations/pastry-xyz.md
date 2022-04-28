# 🍰 PASTRY XYZ

The Bakery DAO website, [https://pastry.xyz/](https://pastry.xyz) is the premier product of the Bakery DAO. Using the unique features of NFTs, we have created a token gated research hub where only the best alpha is accessible to the community (Pastry NFT holders).

Sounds simple on the surface, right?&#x20;

Let's dive into the underlying functions to see what's going on under the hood:

When a user enters the [https://pastry.xyz/](https://pastry.xyz) website, they will see the following page:

![](../../.gitbook/assets/56D28D86-5FB0-41F7-A420-883DFF1E00F3.jpeg)

Users who are not yet members are able to freely browse the content under "Home" "Blog", "About", and "Pricing".

However, if you wish view more in depth alpha, you will need to obtain access to the **Research** column.

Under the research column, a brief introduction of the article is shown. However, it is not shown in its entirety.

![](../../.gitbook/assets/9519CF86-D555-455C-8A33-E2E7CB09D4E1.jpeg)

When someone who is not a member goes to click on one of these articles, they will be prompted verify their Bakery NFT membership.

![](../../.gitbook/assets/1D7AACF0-A217-4084-8C34-550018BDEA9B.jpeg)

Behind the scenes, this content is hidden behind a "Lock". A lock is a smart contract deployed on the Ethereum blockchain which defines terms of a membership.

Each lock contract is an [ERC-721](https://eips.ethereum.org/EIPS/eip-721) compliant contract capable of creating and managing NFTs (non-fungible tokens we call "Keys"), as well as restricting access based on the user's possession (or lack of) one of these keys.
