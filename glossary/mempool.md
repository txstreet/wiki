---
title: Mempool
description: The mempool is a list of transactions currently waited to be confirmed.
published: true
date: 2021-03-24T04:54:20.651Z
tags: ethereum, bitcoin, bitcoin-cash, blockchain, monero
editor: markdown
dateCreated: 2021-03-15T13:42:07.942Z
---

## Summary{#summary}

The mempool is a list or "pool" of transactions currently waiting to be confirmed on the BTC/BCH/ETH network. These transactions are stored in each node's memory until they are confirmed and stored in a block on the blockchain. Each node is responsible for maintaining it's own mempool, which means some nodes may have a slightly different list of transactions in their mempool than others. However, the list is more or less the same across the network. When a block is found by a miner, they choose transactions from the mempool to include in the block. They can choose any number of transactions as long as the total size of the transactions included is less than the block size limit (or total weight less is than the weight limit on BTC). Miners are incentivized to pick transactions with the highest fee attached, because they get to claim these fees along with the block reward.

On TxStreet.com, the mempool is visualized with people. Each person represents one transaction in the mempool waiting to get to the blockchain.
