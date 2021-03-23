---
title: Blockchain
description:
published: true
date: 2021-03-15T13:33:02.522Z
tags: ethereum, bitcoin, bitcoin-cash
editor: markdown
dateCreated: 2021-03-15T13:33:02.522Z
---

## Summary

The blockchain is the complete "database" of every transaction that has ever occurred for a cryptocurrency. Every full node (which is the downloaded software) has an identical copy of this database. New transactions are added to this database through "blocks", which are created by miners. When a block is created, it includes a reference of the previous block that was created. The previous block includes a reference of the block before that, and so on. This was how the term "blockchain" was coined.

On TxStreet.com, when a block is mined, the traffic light will turn green and a bus/block will leave for the blockchain.

## Genesis Block

A genesis block is the very first block of a blockchain, and is the only block of each blockchain that has no prior block to reference, so its "previous hash" value is set to 0. The hash of the genesis block is added to each new transaction in the new block, creating a unique hash for the new block. This process is repeated to lengthen this chain of blocks, creating what we know as blockchain, thus making the genesis block a starting point and essential for any blockchain.

The hash for Bitcoin's genesis block is **000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f** and can be looked up on any Bitcoin block explorer.

## Distributed Ledger

Distributed ledgers perform the same actions as ledgers (books used to record transactions between peers) but with no centralized entity recording transactions. This means that multiple entities, each with their own computing system, each hold a copy of the ledger. If for instance someone has an idea to change or improve the ledger, they can propose an update, and everyone who holds a copy of the ledger will have the opportunity to vote on it. After an agreement is made regarding the update, a recording is made to the ledger before saving to each computing system with a copy of it. This process is repeated and results in a fully functional distributed ledger, also known as a blockchain. 
