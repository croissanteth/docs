---
description: Some of the BakeryNFTs expire... Let's have a look at how that works...
cover: ../../.gitbook/assets/bakerynft.png
coverY: 0
---

# 📅 How does expiry work?

**Some pastries go bad!**

The BakeryNFTs are just like any other ERC-721, but with an added expirationDuration parameter. This is determined by the creator of the contract upon creation, and it is used as reference for future purchases of the membership.

### `keyExpirationTimestampFor`

This function that returns the expiration timestamp for the token owned by one address. It returns 0 if the user does not own a key and a timestamp from the past if the membership has expired.

```javascript
function keyExpirationTimestampFor(
  address _keyOwner
) external view returns (uint timestamp);
```
