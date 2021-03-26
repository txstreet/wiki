---
title: Mining
description: Mining is the process of miners validating transactions for reward.
published: true
date: 2021-03-24T03:48:47.998Z
tags:
editor: markdown
dateCreated: 2021-03-20T22:50:14.998Z
---

## Summary{#summary}

Mining is the process of miners validating transactions occurring on a specific [Proof-of-Work](#proof-of-work) blockchain and adding them to blocks, which are verified when they take up a designated amount of space. Miners do this with expensive computer-like hardware that try to solve calculations as fast as possible. When miners succesfully create blocks, they get approval from other users of the network, and then they are rewarded when the block is added to the blockchain, making the chain longer and more secure. These blocks, the contents inside them, the miner who verified them, and almost all other information accrued during the mining process can be looked up on a [block explorer](/en/blockchain/blockexplorer) designated for the blockchain where a block was mined.

## What is Mining?{#what-is-mining?}

**Mining** is a process put in place to get the native currency of a blockchain in circulation, and to increase security. It is included in the consensus algorithm known as Proof-of-Work, which is what the first decentralized cryptocurrency, Bitcoin, uses.

For mining to begin, users must first transact with the native currency in some way, thus creating and broadcasting a transaction throughout the network. These pending transactions are pooled together in what is known as the [mempool](/en/blockchain/mempool). Once there are some transactions waiting in the mempool, [miners](#miners) using [ASICs](#asics) group them together, verifying them by running them through a hash function (functions that deliver the same result each time the same input is used), compressing them into hashes (256-bit alphanumeric strings that can be thought of as a digital fingerprints for verification), and putting them into files called blocks until they reach a designated size (1 MB in the case of Bitcoin). Those hashes are hashed some more while being organized into a [merkle tree](#merkle-trees), the top of which is known as the root hash or merkle root. This, along with the hash of the previous block, a [coinbase transaction](#coinbase-transactions), and [nonce](#nonce) are added to the block's header and then collectively put through a hash function. If the resulting hash does not meet the requirements of the target hash (a designated value that, in Bitcoin's case, requires the block hash to be equal to or below it) for that block then the miner tries again, this time inputting a different nonce, resulting in a different hash. As miners make computations increasingly faster, their [hash rate](#hash-rate) will increase, lowering the mining [difficulty](#difficulty) and increasing their odds of coming out with a correct solution faster.

If a miner is the first to come up with a hash that meets the requirements of the target hash, he puts the block forth to be verified by the other nodes of the network. If they agree that the hash and block are valid, they add a timestamp to the block, the miner is rewarded in the native currency via [block reward](#block-rewards-and-the-halving), and the block is sealed and immediately added onto the previous block in the blockchain, where the information inside can never be changed but can be tracked forever. After this is complete, miners repeat the process for the next block, in hopes of being the first with the correct hash.

## Miners{#miners}

**Miner** refers to a type of node on a blockchain known as a miner node. Miners can run a full node and choose to work alone as a **solo miner**, or pool together their computational power with other nodes and work as a **pool miner**. Solo miners could potentially take years to mine one block if their hash rate can't compete with that of a pool miner's, although one block as a solo miner would more than pay for the operating costs during that elapsed time. Pool miners tend to see block rewards far more often, however their reward is distributed amongst the pool proportional to each miner's power presented. This results in small amounts of coins compared to the full block reward, but is still considered a viable option to many, as they never see themselves having enough computing power alone to run a successful solo mining operation. The issue with pool mining is that if users continue to join large pools, it gives them a larger computational power and share of the network, therefore counterproductive to decentralization and increasing the potential of a [51% attack](#51-attack).

## ASICs{#asics}

**ASICs** are application-specific integrated circuits, meaning they are built and ran for one purpose only. In blockchain, it's common to use ASIC miners which are typically built to mine coins from specific blockchains, so a Bitcoin ASIC miner would not work on Ethereum when it was Proof-of-Work and vice-verse.

## Merkle Trees{#merkle-trees}

**Merkle trees** are ways of reorganizing and refining digital information, and in blockchain they are put in block headers to help distinguish and verify the transactions within in a secure and space-saving way. To create a merkle tree, miners repeatedly run hashes through a hash function until there is only one hash left, known as the **merkle root**, or root hash. All trees have leaves and branches, and merkle trees are no different; Individually hashed units are **merkle leaves**, and units hashed together are **merkle branches**.

## Coinbase Transactions{#coinbase-transactions}

**Coinbase transactions** are special types of transactions that can only be created by miners. They are almost always the first transaction added to new blocks and they enable miners to receive their reward for successfully verifying transactions and adding blocks.

## Nonce{#nonce}

A **Nonce** is a number or value that can only be used once. In blockchain, miners use computational power and calculations to rapidly guess the nonce at the same time that it's being put through a hash function with the rest of the information in a block header. If guessed correctly, the result is a final hash that meets the requirements of the target hash, thus making the nonce the last piece of information each miner must figure out.

## Hash Rate{#hash-rate}

The **hash rate** is a unit of measurement that represents the number of computations miners complete in one second. The term is also used to calculate and represent the overall hash rate of networks as a whole and can be used to calculate how efficient a particular miner is.

## Difficulty{#difficulty}

**Difficulty**, in this case, is a blockchain statistic used to determine how hard it will be to find a hash lower than the target hash for a specific block. **Difficulty adjustments** occur every set amount of blocks, based on the amount of time it took to mine the previous same amount of blocks. For example, Bitcoin has a difficulty adjustment every 2016 blocks based on how long it took to find the most recent 2016 blocks.

## Block Rewards and The Halving{#block-rewards-and-the-halving}

**The Halving** is when the **block reward**, or what miners are issued for being the first miner to successfully create a block, is cut in half. It is coded into the network and automatically takes place every time a set number of blocks have been mined. For bitcoin, halving events happen every 210,000 blocks. Because one block is mined roughly every ten minutes, this takes around four years. Bitcoin's initial block reward was 50 BTC per block, although now it sits at 6.25 BTC per block.