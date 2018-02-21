---
layout: default
---

### [](#using-lightning-wallet)Using Lightning wallet

Once a Bitcoin wallet is created, you can then start using a Lightning wallet by opening a payment channel with a peer of your choice and using that channel to send payments across the Lightning network.

### [](#payment-channel)What is a payment channel?

Technically speaking, a payment channel is a multisig lockbox on a Bitcoin blockchain which is mutually controlled by you and a peer of your choice. A certain amount of bitcoin is locked into the channel and you can use those coins to send and receive Lightning payments.

You can close a payment channel and get the rest of your locked coins back to your Bitcoin wallet at any time, either by agreeing with a peer on a mutual closing transaction (which occurs quickly) or via forced channel closing if your peer does not respond or becomes uncooperative.

### [](#forced-channel-closing)Forced channel closure

Both you and your peer always have the option available to forcefully close an opened payment channel, without the other's permission. This will refund your channel balance back into your Bitcoin wallet after a delay of 144 blocks (approximately 24 hours).

For more information on the ways in which payment channels can be closed, watch [this video](https://www.youtube.com/watch?v=H-WJPjAp5u8).

### [](#stuck-payments)Stuck payments

An outgoing Lightning payment may get stuck due to a buggy or malicious node along the payment route. If this happens you will have to wait until it expires, which may take quite a number of Bitcoin blocks. Once it expires the payment will fail and the in-flight funds will be returned back to your Lightning wallet.

### [](#receiving-lightning-funds)Receiving Lightning funds

In order to receive Lightning payments, some conditions must be met:

1. Nothing can be received immediately after creating a new payment channel, as 'room' for incoming funds has to be made by spending some funds first. *A payment channel can be thought of as a full bottle of water: in order to pour something in one first has to pour something out*.

2. Each channel implicitly contains a reserve which is unspendable and typically takes about 1% of the channel's capacity. You must spend that reserve before receiving is allowed. *Unspendable channel reserve is the reason you see a negative receive limit when a new channel is full. It indicates how much you need to spend before anything can be received through the channel*.

3. **Every payment request is disposable**, they can't be fulfilled multiple times. So you will need to issue a new individual payment request for every incoming payment you wish to receive.

4. Your Lightning wallet needs to be online in order to receive funds.

### [](#commit-transaction-fee)Commit transaction fee

Sending each Lightning payment creates a valid Bitcoin transaction which is not broadcast to the network and is kept off-chain. In fact, it never even leaves your device unless a forced channel closing happens. This *commit transaction* must have an appropriate fee for Bitcoin network to accept it in a timely manner.

As a consequence an actual amount available for spending in a payment channel will always be slightly less than the full amount as it always needs to contain enough funds for a current on-chain Bitcoin *commit transaction fee*.

Next: [Recovering lost Bitcoin balance](http://lightning-wallet.com/recovering-lost-bitcoin-balance.html#recovering-lost-bitcoin-balance)
