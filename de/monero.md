---
title: Monero
description: Monero is a privacy focused blockchain and cryptocurrency.
published: true
date: 2021-05-22T08:22:55.843Z
tags: monero
editor: markdown
dateCreated: 2021-04-09T15:14:07.339Z
---

## Summary{#summary}

Monero is the leading privacy oriented blockchain and cryptocurrency. Monero hides the sender, receiver, and amount of every single transaction, so you'll only know who sent you XMR if they discuss it with you. Users of the network aren't able to see transaction information, but the blockchain can still verify it, so Monero is still secure. Other privacy coins like [Dash](https://www.dash.org/) and [Zcash](https://z.cash/) give users the option to make transactions private, but Monero ensures that every transaction is private, unless directed otherwise.

Monero blocks are visualized on [TxStreet](https://www.txstreet.com) as orange buses with the Monero logo, the block number, and the transaction fee associated.

- [Live Stats](/en/monero/live-stats)
{.links-list}

## What is Monero?{#monero}

**Monero (XMR)** is a blockchain and private cryptocurrency created with the goal of solving [Bitcoin's](/en/bitcoin) biggest problems and creating a truly untraceable and fungible currency. To achieve a more level playing field in mining and become more resistant to powerful miners taking a large percentage of the network, Monero tweaked with Bitcoin's [Proof-of-Work](/en/glossary/consensus-algorithms/#pow) [consensus algorithm](/en/glossary/consensus-algorithms) and came up with **RandomX** (formerly known as CryptoNote), which is an ASIC-resistant and CPU-friendly PoW algorithm. In hopes of scaling their blockchain in real time, Monero developers implemented a dynamic block size. The block size limit is calculated by nodes of the network and is twice the median block size of the last 100 blocks, with one new block being mined every two minutes. If a miner wants to increase the block size, they may do so at any time, but they face a penalty. This ensures that an increase to the block size is only made when the fees within the block outweigh the cost of creating a larger block. Fees on the Monero blockchain are measured in Nanoneros/Byte, and one Nanonero is equal to .000000001 XMR, so the Nanonero makes for the equivalent of Bitcoin's Satoshis and [Ethereum's](/en/ethereum) [Gwei](/en/ethereum/#gas-gwei).

To achieve true privacy in a decentralized network, Monero nodes each hold a copy of an obfuscated public ledger, which means that the sender, receiver, and amount of every transaction on it are hidden. To be able to send and receive XMR privately, the Monero team had to create or improve upon multiple concepts; [Ring signatures](#ring-signature) make it impossible for outside observers to see the sender; One-time [stealth addresses](#stealth-address) are used to hide the receiver, and [Ring CT](#ring-ct) is used to hide the amount of each transaction. Transactions on Monero are made up of an equal amount of inputs and outputs. When someone sends XMR to a public address, outputs are created that only that the intended recipient can receive and spend as their own, and their actual wallet address is never shown on the blockchain. Users can however give out a viewkey that allows the recipient(s) to look up a wallet balance, but without any access.

## Monero's History{#monero-history}

Nine days after receiving the first Bitcoin transaction, [Hal Finney](https://en.wikipedia.org/wiki/Hal_Finney_(computer_scientist)) tweeted that he wanted to add more anonymity to Bitcoin. This sparked an interest in private currencies and by the end of 2012, Cryptonote was presented with the intention of making an untraceable and unlinkable cryptocurrency. In 2014, [Bytecoin](https://bytecoin.org/) had launched on top of CryptoNote as both a private and untraceable cryptocurrency and at launch, 80% of the coins that would ever be mined were planned to be circulating. This, among some questions surrounding the technology led to a group of developers to fork from Bytecoin with their own project, BitMonero (later shortened to Monero).

## Ring Signature{#ring-signature}

When someone sends Monero, their output is included in a **ring signature**, which is a ring of random decoy outputs from previous transactions on the blockchain combined with the sender's output to hide the actual sender. To any third party trying to view the transaction, it would be impossible to differentiate which of the outputs in the ring is the actual sender.

## Key Image{#key-image}

To prevent double spending on the Monero blockchain, each output has one [**key image**](https://www.getmonero.org/resources/moneropedia/keyimage.html), which can be thought of as a fingerprint. When transactions are being confirmed, the key image of that transaction's output is looked up to ensure it has never been used before. If it has been used, the transaction will fail, and the attempted double-spend will not go through.

## Stealth Address{#stealth-address}

[**Stealth addresses**](https://www.getmonero.org/resources/moneropedia/stealthaddress.html) are one-time public keys created with every transaction that are linked to a user's private key. These one-time keys are not publicly associated with any private key, meaning the ability to link wallets and addresses together is gone, hiding the identity of the receiver. The sender's wallet, if need be, has the ability to prove that transactions were sent without giving up any identifying information.

## Ring CT (Confidential Transactions){#ring-ct}

When Monero is transacted in any way, a [**Ring CT (Confidential Transactions)**](https://www.getmonero.org/resources/moneropedia/ringCT.html) output is created and attached to the transaction to hide the amount within. Ring CT outputs are generated and attached to every Monero transaction except for the block reward given to miners.
