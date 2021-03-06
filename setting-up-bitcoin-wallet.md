---
layout: default
---

### [](#setting-up-bitcoin-wallet)Setting up a Bitcoin wallet

Upon opening the app for the first time you will be prompted to create a new Bitcoin wallet which alows you to send and receive regular Bitcoin transactions. Wallet data is always stored and encrypted on your device so you will have to use a password of your choice to keep your wallet secure.

Every new Bitcoin wallet is generated randomly, so it's not tied to your device in any specific way. This is particularly important as it means that simply reinstalling the app and creating another Bitcoin wallet won't restore your previous balance - you will get a completely new wallet instead!

There is, however, a simple way to preserve your balance across app reinstalls and even across different devices: <strong><font color="red">you need to write down a mnemonic code once Bitcoin wallet is created</font></strong>.

### [](#mnemonic-code)Mnemonic code

Keeping your mnemonic code secure is very important. It is essentially a secret phrase comprising of 12 random words which is automatically generated by the application when a new wallet is created. Please remember: whoever knows your mnemonic code also fully controls your bitcoin so it should be kept private and secure at all times.

Also, <strong><font color="red">only the mnemonic code can get your Bitcoin wallet back in case you lose your device, forget your wallet passcode or simply uninstall the app by accident</font></strong>, it's that important! One of the following actions should be taken once a new wallet is created to protect you from losing your balance:

- Either write down your mnemonic code on a piece of paper and store it in a very secure place.
- Or use a built-in "Encrypt and export" option which lets you store a mnemonic code in encrypted form using your wallet's chosen passcode as a decryption key.

### [](#summary)Summary

In general there are two different pieces of private data associated with your wallet: the mnemonic code and your wallet passcode. 

Your passcode is required to send coins from within the app and the mnemonic code is the only way to restore your balance in emergency situations such as lost/stolen device, forgotten passcode, uninstalled app etc.

### [](#how-bitcoin-wallet-displays-balance)How balances are displayed

Bitcoin is only allowed to be spent if the incoming transactions have been confirmed and as such it displays a balance in a way which may seem strange at first. Let's imagine the wallet is empty and you have an incoming 1 BTC transaction. Here is how your balance will be displayed:

1. While the 1 BTC incoming transaction is unconfirmed: `0 BTC + 1`
2. Once the 1 BTC incoming transaction gets a confirmation: `1 BTC`

Now let's imagine you've decided to spend 0.1 BTC, here's how a balance will be looking:

1. While the 0.1 BTC outgoing transaction is unconfirmed: `0 BTC + 0.9`
2. Once the 0.1 BTC outgoing transaction gets a confirmation: `0.9 BTC`

Consider a real-world example in order to understand this: you buy a snack costing $1 but you only have a single $10 bill. At the start you have $10 viewed from every possible angle. After you order the snack you hand over your $10 bill. From the perspective of your wallet you have zero dollars now, but you know in a few seconds the shopkeeper will give you back $9 in change. 

This situation is very similar in Bitcoin where an unconfirmed transaction may be viewed as a period of time between you handing over your $10 bill and getting $9 back.

Next: [Using Lightning wallet](http://lightning-wallet.com/using-lightning-wallet.html#using-lightning-wallet)
