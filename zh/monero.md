---
title: Monero
description: Monero is a privacy focused blockchain and cryptocurrency.
published: true
date: 2021-05-11T07:41:03.164Z
tags: monero
editor: markdown
dateCreated: 2021-04-09T15:14:07.339Z
---

## Summary{#summary}

Monero is the leading privacy oriented blockchain and cryptocurrency. To maintain full privacy on their blockchain Monero hides the sender, receiver, and amount of every single transaction, preventing any link to a single person, so you'll only know who sent you Monero if they discuss it with you. Despite users of the network not being able to see vital transaction information, the blockchain can still verify this hidden information, so Monero is still secure. To maintain full privacy on their blockchain Monero hides the sender, receiver, and amount of every single transaction, preventing any link to a single person, so you'll only know who sent you Monero if they discuss it with you. Despite users of the network not being able to see vital transaction information, the blockchain can still verify this hidden information, so Monero is still secure.

Monero blocks are visualized on [TxStreet](https://www.txstreet.com) as orange buses with the Monero logo, the block number, and the transaction fee associated.

[Live Stats](/en/monero/live-stats)

## What is Monero?{#monero}

**Monero (XMR)** is a private blockchain created with the goal of solving [Bitcoin's](/en/bitcoin) biggest problems and creating a truly private and untraceable currency. To achieve a more level playing field in mining, Monero has been tweaking with Bitcoin's [Proof-of-Work](/en/blockchain/consensus-algorithms/#proof-of-work) [consensus algorithm](/en/blockchain/consensus-algorithms) throughout its development and currently uses **RandomX** (formerly known as CryptoNote), which makes the network more decentralized by being resistant to mining from powerful mining rigs called ASICs. To achieve true privacy, Monero nodes hold a copy of an obfuscated public ledger, which means that the sender, receiver, and amount of every transaction are hidden. Monero also utilizes some mechanisms to further ensure the privacy of transactions; [Ring signatures](#ring-signature) make it impossible for outside observers to see the sender: One-time [stealth addresses](#stealth-address) are used to hide the receiver, and [Ring CT](#ring-ct) is used to hide the amount of each transaction. Other privacy coins like [Dash](https://www.dash.org/) and [Zcash](https://z.cash/) give users the option to make transactions private, but Monero ensures that every transaction is private, other than the block rewards paid out to miners.


## Monero's History{#monero-history}

Nine days after receiving the first Bitcoin transaction, [Hal Finney](https://en.wikipedia.org/wiki/Hal_Finney_(computer_scientist)) tweeted that he wanted to add more anonymity to Bitcoin. This sparked an interest in private currencies and by the end of 2012, Cryptonote was presented with the intention of making an untraceable and unlinkable cryptocurrency. In 2014, [Bytecoin](https://bytecoin.org/) had launched on top of CryptoNote as both a private and untraceable cryptocurrency and at launch, 80% of the coins that would ever be mined were planned to be circulating. This, among some questions surrounding the technology led to a group of developers to fork from Bytecoin with their own project, BitMonero (later shortened to Monero).

## Ring Signature{#ring-signature}

When someone sends Monero, their output is included in a **ring signature**, which is a ring of random decoy outputs from previous transactions on the blockchain combined with the sender's output to hide the actual sender. To any third party trying to view the transaction, it would be impossible to differentiate which of the outputs in the ring is the actual sender.

## Key Image{#key-image}

To prevent double spending on the Monero blockchain, each output has one **key image**, which can be thought of as a fingerprint. When transactions are being confirmed, the key image of that transaction's output is looked up to ensure it has never been used before. If it has been used, the transaction will fail, and the attempted double-spend will not go through.

## Stealth Address{#stealth-address}

**Stealth addresses** are one-time public keys created with every transaction that are linked to a user's private key. These one-time keys are not publicly associated with any private key, meaning the ability to link wallets and addresses together is gone, hiding the identity of the receiver. The sender's wallet, if need be, has the ability to prove that transactions were sent without giving up any identifying information.

## Ring CT (Confidential Transactions){#ring-ct}

When Monero is transacted in any way, a **Ring CT (Confidential Transactions)** output is created and attached to the transaction to hide the amount within. Ring CT outputs are generated and attached to every Monero transaction except for the block reward given to miners.
