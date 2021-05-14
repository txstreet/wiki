---
title: Mining
description: Mining is the process of miners validating transactions for reward.
published: true
date: 2021-05-14T20:27:44.576Z
tags: bitcoin, bitcoin-cash, blockchain, monero
editor: markdown
dateCreated: 2021-05-14T03:15:53.132Z
---

## Summary{#summary} 

Mining is the process in which transactions from the mempool are added to a block in a proof-of-work blockchain. This is done by miners, who are people running mining software on their computer. Miners are incentivized to do this because for each new block they mine, they get to collect/create a block reward (which is also how new bitcoins are added into circulation), and transaction fees.

On TxStreet.com, mining is visualized by the traffic lights, which turn green whenever a miner finds a block, and otherwise stay red when miners are working.

## What is Mining?{#what-is-mining?}

[What Is Bitcoin Mining? (Load YouTube Video)](https://www.youtube.com/watch?v=qFOeFXwCuLw)

In order to find a block, your computer performs many trial and error calculations every second in order to find a solution to a complex math problem (a number that can be linked to the previous block's solution with a hashing algorithm). When a new block is created, it includes a new math problem (or reference number) that miners must use to find the next block. For this reason, it is impossible to skip ahead and do work for future blocks, because you always need the reference number from the previous block.

Bitcoin mining is a very competitive industry, because no matter how many miners are working towards finding the next block, a new block will only be found every 10 minutes on average. This is enforced through the network difficulty, which automatically changes the number of zeros required to be in the start of the block's solution to the math problem. 

## Mining Operations{#mining}

Miners can run a full node and choose to work alone as a **solo miner**, or pool together their computational power with other nodes and work as a **pool miner**. Solo miners could potentially take years to mine one block if they can't compete with pool miners, although one block as a solo miner would more than pay for the operating costs during that elapsed time. Pool miners see block rewards far more often, however their reward is distributed amongst the pool proportional to power presented. This results in small amounts of coins compared to the full block reward, but is still considered a viable option to many, as they never see themselves having enough computing power alone to run a successful solo mining operation. 

The issue with pool mining is that if users continue to join large pools, it gives them a larger computational power and share of the network, therefore counterproductive to decentralization and increasing the potential of a [51% attack](#51-attack).

## Block Rewards and The Halving{#block-rewards-and-the-halving}

**The Halving** is when the **block reward**, or what miners are issued for being the first miner to successfully create a block, is cut in half. It is coded into the network and automatically takes place every time a set number of blocks have been mined. For bitcoin, halving events happen every 210,000 blocks, around four years. Bitcoin's initial block reward was 50 BTC per block, although now it sits at 6.25 BTC per block. In 2024 it will be cut in half to 3.125 BTC per block.

## Miner-Extractable Value (MEV){#mev}

**Miner-Extractable Value (MEV)** is a measure of the profit a miner can make by including, excluding, or reorganizing transactions in a block. Miners have the full choice in deciding which transactions to include from the mempool into blocks, and they typically organize them by highest transaction fee. 

Although the term was coined 'Miner'-Extractable Value, it doesn't necessarily have to apply to miners; One of the more common forms of MEV today is when arbitrage bots take advantage of **arbitrage opportunities**, which are discrepancies in a coin's price between exchanges. In the instance of an arbitrage opportunity, the arbitrage bot will purchase a coin on the exchange with a lower rate and quickly sell it on the exchange with a higher rate, earning themselves profit and causing liquidity providers impermanent loss in the process. Another popular form of MEV is frontrunning. When a frontrunning bot sees a trader's large transaction, they copy the transaction and pay a higher gas price to get their own transaction processed first. Doing so exposes the original trader to a high price slippage, and puts the frontrunner in profit upon completion of the original user's trade. These strategies of trying to extract more MEV than ever before, along with gas price bidding wars performed by arbitrage bots, are contributing to higher gas prices on the [Ethereum](/en/ethereum) network than ever before and exploiting those that use a DEX, effectively creating the MEV crisis.
