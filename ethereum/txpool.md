---
title: TxPool
description: 
published: true
date: 2021-03-11T16:45:47.299Z
tags: ethereum
editor: markdown
---

# TxPool
The Txpool is a list or "pool" of transactions waiting to be confirmed on the Ethereum Network. These transactions are stored in each node's memory until they are confirmed and stored in a block on the blockchain. Each node is responsible for maintaining it's own txpool, which means some nodes may have a slightly different list of transactions in their txpool than others. However, the list is more or less the same across the network. When a block is found by a miner, they choose transactions from the txpool to include in the block. They can choose any number of transactions as long as the total gasUsed of the transactions included is less than the block gas limit. Miners are incentivized to pick transactions with the highest fee attached, because they get to claim these fees along with the block reward.

On TxStreet.com, the txpool is visualized with people. Each person represents one transaction in the mempool waiting to get to the blockchain.