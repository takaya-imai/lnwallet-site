---
layout: default
---

### [](#storage-tokens)Storage tokens

These are special cryptographic entities provided by Olympus server in exchange for a Lightning payment. You can think of them as single-use tickets which are used to anonymously store data such as [lightning channel backups](reimbursing-funds-locked-in-a-lost-payment-channel.html#reimbursing-funds-locked-in-a-lost-payment-channel) and [scheduled Bitcoin transactions](what-does-olympus-server-do.html#what-does-olympus-server-do) on Olympus server.

A Lightning payment of 2000 Satoshi is automatically made by the wallet in exchange for 50 storage tokens when your first [payment channel](using-lightning-wallet.html#payment-channel) is created. Once obtained these tokens are stored by the wallet and arespent  gradually and automatically when needed.

### [](#reasons-for-storage-tokens-to-exist)Reasons for storage tokens to exist

- Storage tokens help to pay for the maintenance of a public Olympus server. Accepting micropayments for some useful API calls seems like a good idea but having a Lightning payment for each invidividual API call is overkill.

- Lightning Wallet aims to be as private as possible, so no registration or user accounts are required. However, simply allowing anonymous users to store any amount of data on a server is an obvious attack vector.

Storage tokens solve both of these issues beautifully: a single Lightning micropayment gives you an access to 50 API calls. Technically speaking, storage tokens are [blind signatures](https://en.wikipedia.org/wiki/Blind_signature) which posess an [unlinkability property](https://tools.ietf.org/id/draft-hansen-privacy-terminology-00.html#unlinkability), meaning every API call made by your wallet is anonymous and private.

You are free to stop using storage tokens at any moment by [setting up your own Olympus server](what-does-olympus-server-do.html#setting-up-your-own-server), which would use a free public key-based authentication instead of paid storage tokens.
