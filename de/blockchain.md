---
title: Blockchain
description:
published: true
date: 2021-03-26T06:51:49.318Z
tags: ethereum, bitcoin, bitcoin-cash
editor: markdown
dateCreated: 2021-03-15T13:33:02.522Z
---

## Summary{#summary}

The blockchain is the complete "database" of every transaction that has ever occurred for a cryptocurrency. Every full node (which is the downloaded software) has an identical copy of this database. New transactions are added to this database through "blocks", which are created by miners. When a block is created, it includes a reference of the previous block that was created. The previous block includes a reference of the block before that, and so on. This was how the term "blockchain" was coined.

On TxStreet.com, when a block is mined, the traffic light will turn green and a bus/block will leave for the blockchain.

## Genesis Block{#genesis-block}

A **genesis block** is the very first block of a blockchain, and is the only block of each blockchain that has no prior block to reference, so its "previous hash" value is set to 0. The hash of the genesis block is added to each new transaction in the new block, helping to create a unique hash for the new block. This process is repeated to lengthen this chain of blocks, creating what we know as blockchain.

The hash for Bitcoin's genesis block is **000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f** and can be looked up on any Bitcoin block explorer.

## Distributed Ledger{#distributed-ledger}

**Distributed ledgers** perform the same actions as ledgers (books used to record transactions between peers) but with no centralized entity recording transactions. This means that multiple entities, each with their own computing system, each hold a copy of the ledger. If for instance someone has an idea to change or improve the ledger, they can propose an update, and everyone who holds a copy of the ledger will have the opportunity to vote on it. After an agreement is made regarding the update, a recording is made to the ledger before being savedto each computing system with a copy of it. This process is repeated and results in a fully functional distributed ledger, also known as a blockchain.

## Smart Contract{#smart-contract}

**Smart contracts** are self-executing contracts with the terms of agreement written into the lines of code. Both the agreement and code are stored on a blockchain, where the code ensures the execution when conditions are met, and the blockchain ensures the transactions can be tracked and are irreversible. This technology is what makes agreements and transactions between anonymous parties possible without the use of a central authority or middleman.

## Oracle{#oracle}

**Oracles** are devices or entities that verify and send information between smart contracts and real-world systems. There are many types of oracles, and more are coming out as the ways of collecting and distributing information are constantly evolving. **Inbound oracles** supply off-chain data to smart contracts. **Outbound oracles** supply on-chain data to real world systems. **Software oracles** source information from online and typically include things like asset prices and temperatures. **Hardware oracles** send data from the real-world to smart contracts as a result of an occurrence, like a bar code being scanned. **Consensus based oracles** query multiple oracles and send information when certain requirements are met, like all of the oracles having matching information.

## Confirmations{#confirmations}

In blockchain, **confirmations** are a measure of how many blocks have been created since a transaction was put on a blockchain. More blocks mean a transaction is more secure and harder to reverse. Exchanges will usually have a set number of confirmations required, and users can decide on how many they think are necessary when sending peer-to-peer. Larger transactions typically have more confirmations to ensure the funds can't be lost or double spent. If someone was looking to do harm to a transaction with 20 confirmations, the user would have to decrypt the one block including the transaction along with the 20 after, and any other blocks that were created since.

## Private Keys, Public Keys, and Wallet Addresses{#keys-and-addresses}

When creating an exchange account or wallet, users will come across their **public keys** and **private keys**. Public keys allow users to send messages and transactions by encrypting them to be unreadable or unobtainable without a specific private key. Private keys are not meant to be shared with anyone, and if lost could result in lost access to wallets. Although the public and private keys do all the work, when users want to send or receive cryptocurrency, they are either asked for a **wallet address** or shown their own. Wallet addresses are essentially compressed public keys or QR codes that make it easier for people to send cryptocurrency, because typing in a public key would be inefficient. Here's an example of a public key compared to a wallet address:

Public key: 3048 0241 00C9 18FA CF8D EB2D EFD5 FD37 89B9 E069 EA97 FC20 5E35 F577 EE31 C4FB C6E4 4811 7D86 BC8F BAFA 362F 922B F01B 2F40 C744 2654 C0DD 2881 D673 CA2B 4003 C266 E2CD CB02 0301 0001

Wallet address: 1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2



## Decentralized Autonomous Organization (DAO){#dao}

**Decentralized autonomous organizations**, or **DAOs**, are organizations represented by rules encoded as open-source computer programs that are directly controlled by the holders of the token, typically in the form of a vote. DAOs are meant to have no central decision-making power, and to run autonomously, with the only input needed being that of the users.
