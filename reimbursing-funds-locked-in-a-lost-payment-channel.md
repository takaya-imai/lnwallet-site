---
layout: default
---

### [](#reimbursing-funds-locked-in-a-lost-payment-channel)Reimbursing funds locked in a lost payment channel

A phone with an open payment channel may get lost or destroyed at any moment. To fully recover your balance in this scenario there are two things you must do: 

1. To recover your Bitcoin balance, use your [mnemonic code](setting-up-bitcoin-wallet.html#mnemonic-code) to restore your wallet onto a new phone.
2. To recover funds locked in a [payment channel](using-lightning-wallet.html#payment-channel) you must have made sure to backup your payment channel with an Olympus server *before* losing access your phone.

Lightning Wallet will take these measures for you by default: once a new payment channel is created, its static parameters are automatically encrypted and sent to an [Olympus server](what-does-olympus-server-do#what-does-olympus-server-do). This operation is only carried out once, and no personally identifying information is transferred.

Thanks to your encrypted Olympus server backup, after your Bitcoin balance is restored on a new phone with your mnemonic code you can simply issue a 'lost channel funds recovery request' in the app by selecting:

`App Menu → Wallet settings → Recover channel funds`

After a few seconds your remaining balance from a lost payment channel is refunded to your Bitcoin wallet. Please note that following conditions must be met for this to work:

- Olympus server does not store your data for free so saving static channel parameters requires one [storage token](storage-tokens.html#storage-tokens).
- The peer on the other side of the lost channel must be online and well-behaving in order to receive your recovery request and initiate a remote [forced channel closure](using-lightning-wallet.html#forced-channel-closing).
