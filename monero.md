---
title: Monero                                     
description: Monero is a privacy focused blockchain and cryptocurrency.                                        
published: true                                       
date: 2021-04-03T02:42:51.998Z                        
tags: monero                   
editor: markdown                                   
dateCreated: 2021-03-30T15:30:03.998Z 
---

## Summary{#summary}

Monero is the leading privacy oriented blockchain and cryptocurrency. To maintain full privacy on their blockchain Monero hides the sender, receiver, and amount of every single transaction, preventing any link to a single person, so you'll only know who sent you Monero if they discuss it with you. Despite users of the network not being able to see vital transaction information, the blockchain can still verify this hidden information, so Monero is still secure.

## Monero{#monero}

**Monero** was created as a fork of Bytecoin (the first private cryptocurrency) with the goal of solving [Bitcoin's](#bitcoin) biggest problems and creating a truly private and untraceable currency. To achieve a more level playing field in mining, Monero established a slightly different [Proof-of-Work](#proof-of-work) algorithm than Bitcoin's. To achieve true privacy, Monero users hold a copy of an obfuscated public ledger, which means that the sender, receiver, and amount of every transaction are hidden. Monero also utilizes some mechanisms to further ensure the blockchain's privacy; [Ring signatures](#ring-signature) make it impossible for outside observers to see the sender: One-time [stealth addresses](#stealth-address) are used to hide the receiver, and [Ring CT](#ring-ct) is used to hide the amount of each transaction. Other privacy coins like [Dash](https://www.dash.org/) and [Zcash](https://z.cash/) give you the option to make your transactions private, but Monero ensures that every transaction is private.

## Ring Signature{#ring-signature}

When someone sends Monero, their output is included in a **ring signature**, which is a ring of random decoy outputs from previous transactions on the blockchain combined with the sender's output to hide the actual sender. If the sender chooses a ring signature of "5", then a ring consisting of the sender's output and four random outputs is created. To any third party trying to view the transaction, it would be impossible to differentiate which of the five outputs in the ring is the actual sender. 

## Key Image{#key-image}

To prevent double spending on the Monero blockchain, each output has one **key image**, which can be thought of as a fingerprint. When miners are confirming transactions, they look up the key image of that transaction's output to make sure it has never been used before. If it has been used, the transaction will fail, and the attempted double-spend will not go through.

## Stealth Address{#stealth-address}

**Stealth addresses** are one-time public keys created with every transaction that are linked to a user's private key. These one-time keys are not publicly associated with any private key, meaning the ability to link wallets and addresses together is gone, hiding the identity of the receiver. The sender's wallet, if need be, has the ability to prove that transactions were sent without giving up any identifying information.

## Ring CT{#ring-ct}

When newly created Monero is transferred for the first time, **Ring CT (Confidential Transactions)** outputs are created. These are outputs that mask the amount of monero in a transaction, and because they are created and attached when the Monero is first transferred, the amount is hidden forever.
