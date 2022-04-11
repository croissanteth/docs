---
description: >-
  A light-weight interface for customizing input, specific parameters on NFT
  purchase, and other cool features...
cover: ../.gitbook/assets/bakerydaoyt.png
coverY: 0
---

# 🎁 Paywall

![](../.gitbook/assets/chrome\_HP53N9iOdr.png)

The paywall is a web application that provides a user interface allowing people to purchase keys to given locks and subsequently trigger certain behavior based on visitors having keys at the time of page visit. It can be embedded on any web page or inside web views.

It currently supports Wallet Connect, Coinbase, Metamask, Trust Wallet, and even user-generated accounts who purchase via credit card.

The paywall has a pretty basic configuration but can be customized for more advanced use cases as well.

## The paywallConfig object

The `paywallConfig` is a JSON object which includes a set of customizations for your experience. It includes the following elements:

* `locks` : _required object_, a list of lock objects (see below).
* `icon`: _optional string_, the URL for an icon to display in the top left corner of the modal.
* `callToAction`: _optional object_, a list of messages shown based on the state of the checkout modal (see below).
* `metadataInputs`: _optional array_, a set of input fields as explained there.
* `persistentCheckout`: _optional boolean_: `true` \_\_if the modal cannot be closed, defaults to `false` when embedded. When closed, the user will be redirected to the `redirect` query param when using a purchase address (see above).
* `useDelegatedProvider`: _optional boolean._ To be announced.
* `network`: _optional integer._ defaults to `1`. See below.
* `referrer`: _optional string_. The address which will receive UDT tokens (if the transaction is applicable)
* `messageToSign`: _optional string_. If supplied, the user is prompted to sign this message using their wallet. If using a checkout URL, a `signature` query param is then appended to the `redirectUri` (see above). If using the embedded paywall, the `unlockProtocol.authenticated` includes the `signature` attribute.
* `pessimistic`: _optional boolean._ defaults to `false`_._ By default, to reduce friction, we do not require users to wait for the transaction to be mined before offering them to be redirected. By setting this to `true`, users will need to wait for the transaction to have been mined in order to proceed to the next step.

#### Locks

The locks object is a list of objects indexed by the lock address, where each object can include the following:

* `network`: _recommended integer_. See below.
* `name`: _optional string_. name of the lock to display.

#### Calls to action

The `callToAction` object lets you customize the messages displayed on the checkout UI. They are all optional strings:

* `default` : displayed by default
* `expired` : displayed when the user had a membership previously that expired
* `metadata`: displayed when the user is prompted for metadata

In some cases, we may arbitrarily set a referral address in the JSON config object to define some things we want done upon purchase of a specific membership. In normal transactions, the gas refund is sent to msg.sender. However, it can be customized to include any address for referrals, introducing a whole bunch of interesting use cases.

For example; metadata inputs can be generated and requested upon purchase of the Bakery NFT through a specific link.

The BakeryDAO uses this to customize our checkout flow on the newsletter, prompting users to enter their email address before they are able to purchase or sign up.

![](../.gitbook/assets/chrome\_T7UA0OUXy9.png)

The input here is secured cryptographically using keccak256 to convert inputs into a unique 32 byte hash. From there, the data is only accessible to the contract owner for purposes of sending out the newsletter.

To wrap all of this together, I'll now explain to you what is called "Optimistic Unlocking," something I believe increases user experience ten-fold. This feature improves the customer experience by immediately emitting the `unlocked` event when a transaction is sent, as long as the transaction is likely enough to eventually succeed.

This means that the content is instantaneously available for viewing, and users won't have to wait for the transaction to be mined!
