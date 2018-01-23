---
layout: default
---

### [](#recovering-lost-bitcoin-balance)Recovering your lost Bitcoin balance

In order to recover your lost Bitcoin balance you will need to use the 12 word [mnemonic code](setting-up-bitcoin-wallet.html#mnemonic-code) saved *before* your wallet is lost, either in the unencrypted 12 word format or in the encrypted form.

Here are the exact steps you should take when you forget your wallet's passcode or your phone is lost or stolen:

1. If you still have access to your phone then first of all you should erase all current app data in your phone's settings. If you don't know how to erase app data then simply reinstall the application from scratch. If you no longer have access to your phone then install the app once again on a new phone.

2. Open a fresh installation of the application and select the option to "Restore existing Bitcoin wallet" instead of creating a new one. Enter your mnemonic code as well as new wallet password. This is it, no further action is required.

<!-- 3.? If your previous phone had been stolen, you may wish to transfer your balance to a new wallet to ensure that your wallet balance is only accessible from your new device. To do this... -->

*Important note: restored wallets will appear empty at first as it needs some time to catch up with network.*

If you did not save your mnemonic code then there is nothing that can be done to recover your balance. Bitcoin is decentralised, meaning there is no third party that can recover lost wallet balances for you if you did not take proper precautions beforehand.

### [](#wallet-restored-but-balance-zero)When your wallet is restored but the balance is still zero

If you don't see a balance restored for a long time then first of all you should make sure your device has no connectivity issues. Normally a well-connected device displays syncing progress and shows a *Bitcoin wallet is online* message once syncing is complete.

When your device is well connected and synced but you still see a zero balance with no transaction history, this means that your restored mnemonic must contain a typo somewhere.

In order to discover and eliminate a typo you can compare your saved mnemonic code with a [list of all possible valid words](english-bip32.json). An in-page search may be used on to check if every word from your mnemonic is also present in the list. If one or more of your words are not present then simply fix any typos and try again.

Please take care to enter your mnemonic code very carefully when restoring your wallet. Any text is considered valid so even a single typo will be accepted, resulting in you restoring a completely different wallet.

Next: [Reimbursing funds locked in a lost payment channel](http://lightning-wallet.com/reimbursing-funds-locked-in-a-lost-payment-channel.html#reimbursing-funds-locked-in-a-lost-payment-channel)
