---
layout: default
---

### [](#using-lightning-wallet)Using Lightning wallet

Once Bitcoin wallet is created you can also start using a Lightning wallet by opening a payment channel with a peer of your choice and using it to send payments across a Lightning network.

### [](#payment-channel)Payment channel

Technically speaking it is a multisig lockbox on a Bitcoin blockchain which is mutually controlled by you and a peer of your choice. It is designed in such a way that once a certain amount of coins is locked in there you can use those coins to send and receive Lightning payments. 

You can close a payment channel and get the rest of your locked coins back to your Bitcoin wallet at any time, either by agreeing with a peer on a mutual closing transaction or via forced channel closing if your peer becomes uncooperative.

### [](#forced-channel-closing)Forced channel closing

This is an option which is always available to both you and your peer once a new payment channel is open. No matter what happens a channel can always be closed without peer's permission with the rest of channel balance refunded back to your Bitcoin wallet.

That said, a refunding Bitcoin transaction created by forced channel closing is encumbered in a time lock of 144 Bitcoin blocks so closing a channel uncooperatively will take about one day of waiting before your channel coins are sent back to your Bitcoin wallet.

You may also want to watch [this video](https://www.youtube.com/watch?v=H-WJPjAp5u8) which covers all the ways a payment channel could be closed.

### [](#stuck-payments)Stuck payments  

An outgoing Lightning payment may get stuck due to a buggy or malicious node along a payment route. In such a case you would have to wait until it expires which may take quite a number of Bitcoin blocks. Once expiry happens a payment will be failed and you will get an in-flight funds back to your Lightning wallet.

### [](#receiving-lightning-funds)Receiving Lightning funds  

...is tricky as there are some conditions: 

1. Nothing can be received once a fresh channel is created since a room for incoming funds should be first made by spending. *A payment channel can be thought of as a full bottle of water: in order to pour something in one first has to pour something out*.

2. Each channel implicitly contains a reserve which is unspendable off-chain and typically takes about 1% of channel capacity. One has to spend that reserve before receiving is allowed. *Unspendable channel reserve is the reason you see a negative receive limit when a new channel is full. It indicates how much you need to spend before anything could be received*.

3. Every payment request is disposable, it can't be fulfilled multiple times. So one would have to issue a payment request per each incoming payment.

4. Lightning wallet needs to be online in order to receive funds.


### [](#commit-transaction-fee)Commit transaction fee

Sending each Lightning payment creates a valid Bitcoin transaction which is kept off-chain, in fact it never even leaves your device unless a forced channel closing happens. This *commit transaction* must have an appropriate fee for Bitcoin network to accept it in a timely manner.

As a consequence an actual amount available for spending in a payment channel will always be slightly less than a nominal amount because it always needs to contain enough funds for a current Bitcoin *commit transaction fee*.

Next: [Recovering lost Bitcoin balance](http://lightning-wallet.com/recovering-lost-bitcoin-balance.html#recovering-lost-bitcoin-balance)
