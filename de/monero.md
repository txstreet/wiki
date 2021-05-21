---
title: Monero
description: Monero is a privacy focused blockchain and cryptocurrency.
published: true
date: 2021-05-21T16:38:53.890Z
tags: monero
editor: markdown
dateCreated: 2021-04-09T15:14:07.339Z
---

## Summary{#summary}

Monero is the leading privacy oriented blockchain and cryptocurrency. To maintain full privacy on their blockchain Monero hides the sender, receiver, and amount of every single transaction, preventing any link to a single person, so you'll only know who sent you Monero if they discuss it with you. Despite users of the network not being able to see vital transaction information, the blockchain can still verify this hidden information, so Monero is still secure.

Monero blocks are visualized on [TxStreet](https://www.txstreet.com) as orange buses with the Monero logo, the block number, and the transaction fee associated.

[Live Stats](/en/monero/live-stats)

## What is Monero?{#monero}

**Monero (XMR)** is a private blockchain created with the goal of solving [Bitcoin's](/en/bitcoin) biggest problems and creating a truly private and untraceable currency. To achieve a more level playing field in mining, Monero has been tweaking with Bitcoin's [Proof-of-Work](/en/glossary/consensus-algorithms/#pow) [consensus algorithm](/en/glossary/consensus-algorithms) throughout its development and currently uses **RandomX** (formerly known as CryptoNote), which makes the network more decentralized by being resistant to mining from powerful mining rigs called ASICs. In hopes of scaling their blockchain in real time, Monero developers implemented a dynamic block size. The block size limit is calculated by nodes of the network and is twice the median block size of the last 100 blocks. Miners face a penalty when trying to increase the block size, ensuring that an increase is only made when the fees within the block outweigh the cost of creating a larger block. Fees on the Monero blockchain are measured in Nanoneros/Byte, and one Nanonero is equal to .000000001 Monero, so the Nanonero makes for the equivalent of Bitcoin's Satoshis and [Ethereum's](/en/ethereum) [Gwei](/en/ethereum/#gas-gwei).

To achieve true privacy, Monero nodes hold a copy of an obfuscated public ledger, which means that the sender, receiver, and amount of every transaction are hidden. Monero also utilizes some mechanisms to further ensure the privacy of transactions; [Ring signatures](#ring-signature) make it impossible for outside observers to see the sender; One-time [stealth addresses](#stealth-address) are used to hide the receiver, and [Ring CT](#ring-ct) is used to hide the amount of each transaction. Other privacy coins like [Dash](https://www.dash.org/) and [Zcash](https://z.cash/) give users the option to make transactions private, but Monero ensures that every transaction is private, other than the block rewards paid out to miners. Users on Monero have the option of giving out a viewkey, which enables others to view their balance, but without any access or privileges.

For a simplified explanation of the basics created by the team at Monero, click [here](https://www.getmonero.org/media/Monero%20-%20The%20Essentials.m4v)


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
