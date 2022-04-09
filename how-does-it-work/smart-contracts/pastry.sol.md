---
description: >-
  The BakeryDAO VIP members contract, which offers a limited supply of custom
  pastries which have unlimited access to the platform(s).
cover: ../../.gitbook/assets/bakerydaoyt.png
coverY: 0
---

# 🧁 Pastry.sol

The [pastry.sol](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721) smart contract is the implementation of a standard ERC-721, with a few packs of punches added in functionality later down the line. This is what is used for the BakeryDAO unlimited access NFTs.

![Cloud Croissant](../../.gitbook/assets/croissantt.webp)

See [Open Zeppelin documentation](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721) for technical details of the smart contracts and all of their internal capabilities.

**`constructor(string name_, string symbol_)`public**

Initializes the contract by setting a `name` and a `symbol` to the token collection.

**`balanceOf(address owner) → uint256`public**

See [`IERC721.balanceOf`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-balanceOf-address-).

**`ownerOf(uint256 tokenId) → address`public**

See [`IERC721.ownerOf`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-ownerOf-uint256-).

**`name() → string`public**

See [`IERC721Metadata.name`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Metadata-name--).

**`symbol() → string`public**

See [`IERC721Metadata.symbol`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Metadata-symbol--).

**`tokenURI(uint256 tokenId) → string`public**

See [`IERC721Metadata.tokenURI`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Metadata-tokenURI-uint256-).

**`baseURI() → string`public**

Returns the base URI set via [`_setBaseURI`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-\_setBaseURI-string-). This will be automatically added as a prefix in [`tokenURI`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-tokenURI-uint256-) to each token’s URI, or to the token ID if no specific URI is set for that token ID.

**`tokenOfOwnerByIndex(address owner, uint256 index) → uint256`public**

See [`IERC721Enumerable.tokenOfOwnerByIndex`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Enumerable-tokenOfOwnerByIndex-address-uint256-).

**`totalSupply() → uint256`public**

See [`IERC721Enumerable.totalSupply`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Enumerable-totalSupply--).

**`tokenByIndex(uint256 index) → uint256`public**

See [`IERC721Enumerable.tokenByIndex`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Enumerable-tokenByIndex-uint256-).

**`approve(address to, uint256 tokenId)`public**

See [`IERC721.approve`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-approve-address-uint256-).

**`getApproved(uint256 tokenId) → address`public**

See [`IERC721.getApproved`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-getApproved-uint256-).

**`setApprovalForAll(address operator, bool approved)`public**

See [`IERC721.setApprovalForAll`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-setApprovalForAll-address-bool-).

**`isApprovedForAll(address owner, address operator) → bool`public**

See [`IERC721.isApprovedForAll`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-isApprovedForAll-address-address-).

**`transferFrom(address from, address to, uint256 tokenId)`public**

See [`IERC721.transferFrom`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-transferFrom-address-address-uint256-).

**`safeTransferFrom(address from, address to, uint256 tokenId)`public**

See [`IERC721.safeTransferFrom`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-safeTransferFrom-address-address-uint256-bytes-).

**`safeTransferFrom(address from, address to, uint256 tokenId, bytes _data)`public**

See [`IERC721.safeTransferFrom`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-safeTransferFrom-address-address-uint256-bytes-).

**`_safeTransfer(address from, address to, uint256 tokenId, bytes _data)`internal**

Safely transfers `tokenId` token from `from` to `to`, checking first that contract recipients are aware of the ERC721 protocol to prevent tokens from being forever locked.

`_data` is additional data, it has no specified format and it is sent in call to `to`.

This internal function is equivalent to [`safeTransferFrom`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-safeTransferFrom-address-address-uint256-bytes-), and can be used to e.g. implement alternative mechanisms to perform token transfer, such as signature-based.

**Requirements:**

* `from` cannot be the zero address.
* `to` cannot be the zero address.
* `tokenId` token must exist and be owned by `from`.
* If `to` refers to a smart contract, it must implement [`IERC721Receiver.onERC721Received`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Receiver-onERC721Received-address-address-uint256-bytes-), which is called upon a safe transfer.

Emits a [`Transfer`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-Transfer-address-address-uint256-) event.

**`_exists(uint256 tokenId) → bool`internal**

Returns whether `tokenId` exists.

Tokens can be managed by their owner or approved accounts via [`approve`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-approve-address-uint256-) or [`setApprovalForAll`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-setApprovalForAll-address-bool-).

Tokens start existing when they are minted (`_mint`), and stop existing when they are burned (`_burn`).

**`_isApprovedOrOwner(address spender, uint256 tokenId) → bool`internal**

Returns whether `spender` is allowed to manage `tokenId`.

Requirements:

* `tokenId` must exist.

**`_safeMint(address to, uint256 tokenId)`internal**

Safely mints `tokenId` and transfers it to `to`.

Requirements: d\* - `tokenId` must not exist. - If `to` refers to a smart contract, it must implement [`IERC721Receiver.onERC721Received`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Receiver-onERC721Received-address-address-uint256-bytes-), which is called upon a safe transfer.

Emits a [`Transfer`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-Transfer-address-address-uint256-) event.

**`_safeMint(address to, uint256 tokenId, bytes _data)`internal**

Same as [`_safeMint`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-\_safeMint-address-uint256-), with an additional `data` parameter which is forwarded in [`IERC721Receiver.onERC721Received`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721Receiver-onERC721Received-address-address-uint256-bytes-) to contract recipients.

**`_mint(address to, uint256 tokenId)`internal**

Mints `tokenId` and transfers it to `to`.

Requirements:

* `tokenId` must not exist.
* `to` cannot be the zero address.

Emits a [`Transfer`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-Transfer-address-address-uint256-) event.

**`_burn(uint256 tokenId)`internal**

Destroys `tokenId`. The approval is cleared when the token is burned.

Requirements:

* `tokenId` must exist.

Emits a [`Transfer`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-Transfer-address-address-uint256-) event.

**`_transfer(address from, address to, uint256 tokenId)`internal**

Transfers `tokenId` from `from` to `to`. As opposed to [`transferFrom`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-transferFrom-address-address-uint256-), this imposes no restrictions on msg.sender.

Requirements:

* `to` cannot be the zero address.
* `tokenId` token must be owned by `from`.

Emits a [`Transfer`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-Transfer-address-address-uint256-) event.

**`_setTokenURI(uint256 tokenId, string _tokenURI)`internal**

Sets `_tokenURI` as the tokenURI of `tokenId`.

Requirements:

* `tokenId` must exist.

**`_setBaseURI(string baseURI_)`internal**

Internal function to set the base URI for all token IDs. It is automatically added as a prefix to the value returned in [`tokenURI`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-tokenURI-uint256-), or to the token ID if [`tokenURI`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#ERC721-tokenURI-uint256-) is empty.

**`_approve(address to, uint256 tokenId)`internal**

Approve `to` to operate on `tokenId`

Emits an [`Approval`](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721#IERC721-Approval-address-address-uint256-) event.

**`_beforeTokenTransfer(address from, address to, uint256 tokenId)`internal**

Hook that is called before any token transfer. This includes minting and burning.

Calling conditions:

* When `from` and `to` are both non-zero, `from`'s `tokenId` will be transferred to `to`.
* When `from` is zero, `tokenId` will be minted for `to`.
* When `to` is zero, `from`'s `tokenId` will be burned.
* `from` cannot be the zero address.
* `to` cannot be the zero address.

To learn more about hooks, head to [Using Hooks](https://docs.openzeppelin.com/contracts/3.x/extending-contracts#using-hooks).
