# 🔌 LOGGING IN

Until now, it was often quite complicated for applications (both web and native) to prompt the user for their wallet address, in order to identify them. As there exists many types of wallets (browser extensions, mobile applications, or even fully "hosted" web apps), it means that asking the user to connect their wallet requires the implementation of multiple API and approaches. Dealing with "injected" objects in the DOM is not trivial and limited to web applications…

The Pastry NFT is proud to be using an implementation of the [Sign-In With Ethereum](https://docs.unlock-protocol.com/unlock/developers/sign-in-with-ethereum) ([EIP4361](https://eips.ethereum.org/EIPS/eip-4361)) specification!

The Pastry NFTs have the unique features in that they can be renewed by approving a contract to spend x amount over y time. If the user approves $200 USDC to be spent over any amount of time, the KeyPurchaser.sol contract will grant them time on their Pastry NFT every time it gets close to expiration with keeper bots.

![](<../../.gitbook/assets/image (6).png>)

The Bakery verification flow is similar to the frequently used **OAuth** & **OpenId Connect** flows, which is made specifically so that other applications who only need to _know_ of the user's address do not have to worry about handling web3 providers, but can still identity users. This makes it trivial for different applications to build "authentication" URLs with a **redirect scheme** that allows even native applications to easily identify a user's address.
