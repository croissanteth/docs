---
description: >-
  A fully-customizable checkout url that anyone can generate and get rewarded
  instantly for attracting new members to the BakeryDAO.
cover: ../.gitbook/assets/bakerynft.png
coverY: 0
---

# 🛒 Purchase Links

![](<../.gitbook/assets/image (9) (1) (1) (1).png>)

Our checkout can easily be integrated and configured in the way the user sees fit, and they can users even generate their own 'referral' links to advertise content locked behind the BakeryNFTs, and get a small percent of each purchase through their URL.

The `paywallConfig` is a JSON object which includes a set of customizations for your experience. It includes the following elements:

* `locks` : _required object_, a list of lock objects (see below).
* `icon`: _optional string_, the URL for a icon to display in the top left corner of the modal.
* `callToAction`: _optional object_, a list of messages shown based on the state of the checkout modal (see below).
* `metadataInputs`: _optional array_, a set of input fields as explained there.
* `persistentCheckout`: _optional boolean_: `true` \_\_if the modal cannot be closed, defaults to `false` when embedded. When closed, the user will be redirected to the `redirect` query param when using a purchase address (see above).
* `useDelegatedProvider`: _optional boolean._ To be announced.
* `network`: _optional integer._ defaults to `1`. See below.
* `referrer`: _optional string_. The address which will receive UDT tokens (if the transaction is applicable)
* `messageToSign`: _optional string_. If supplied, the user is prompted to sign this message using their wallet. If using a checkout URL, a `signature` query param is then appended to the `redirectUri` (see above). If using the embedded paywall, the `unlockProtocol.authenticated` includes the `signature` attribute.
* `pessimistic`: _optional boolean._ defaults to `false`_._ By default, to reduce friction, we do not require users to wait for the transaction to be mined before offering them to be redirected. By setting this to `true`, users will need to wait for the transaction to have been mined in order to proceed to the next step.

**An example of how this can be customized:**

```
{
    "pessimistic": true,
    "locks": {
        "0x61Cc42C66BA9Df72bF6DA89Fcd57215965f74005": {
           "network": 1,
           "name": "BakeryNFT"
        }
    },
    "icon": "https://bakery.fyi/wp-content/uploads/2022/01/1-5.png",
    "callToAction": {
        "default": "Are you ready to join the BakeryDAO?"
    },
    "metadataInputs": [
        {
            "name": "Name",
            "type": "text",
            "required": true
        }
    ]
}
```

Here are some of our generated URL's (thrown through a url shortener to look prettier), which each serve as paywalls to the BakeryNFT, but have different behaviors including the redirect link, metadata inputs (for newsletter), and logos to display.

|                  WEBSITE                  |                  NEWSLETTER                  |                  DISCORD                 |
| :---------------------------------------: | :------------------------------------------: | :--------------------------------------: |
| [https://pastry.xyz/](https://pastry.xyz) | [SUBSCRIBE](https://bakerydao.me/newsletter) | [CHAT NOW](https://bakerydao.me/discord) |
