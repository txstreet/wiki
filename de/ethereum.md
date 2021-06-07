---
title: Ethereum
description: Ethereum is a blockchain, cryptocurrency, and software platform where smart contracts and Dapps are built and used.
published: true
date: 2021-05-17T16:44:19.538Z
tags: ethereum
editor: markdown
dateCreated: 2021-03-12T16:43:49.060Z
---

## Summary{#summary}

Ethereum is a decentralized software platform created so that users could create their own applications, protocols, currencies, and more on the blockchain. It uses the same fundamentals to circulate currency as Bitcoin does, but is slowly making the switch to a different set of fundamentals for Ethereum 2.0, which has the potential to compete with the likes of Visa and Mastercard in transactions per second.

Ethereum blocks are visualized on [TxStreet](https://www.txstreet.com) as blue buses with the Ethereum logo, the block number, and the gas price associated.

- [houses](/ethereum/houses)
- [Live stats](/ethereum/live-stats)
{.links-list}

## What is Ethereum?{#ethereum}

**Ethereum (ETH)** is a blockchain-based software platform with its own cryptocurrency (ether), and its own programming language (solidity), although it supports various programming languages for developers. By using the Ethereum Virtual Machine (EVM), users can create their own cryptocurrency or decentralized project. Any cryptocurrency created on Ethereum is referred to as an ERC-20, including many popular projects like [Chainlink](https://chain.link/), [Maker](https://makerdao.com/en/), [Uniswap](https://uniswap.org/), and more.

Ethereum's blockchain currently uses a [Proof-of-Work](/en/blockchain/consensus-algorithms) [consensus-algorithm](/en/blockchain/consensus-algorithms) to process blocks and distribute ETH, although they are actively making the switch to [Proof-of-Stake](#proof-of-stake) for [Ethereum 2.0](#ethereum-2). This means that while Ethereum uses miners like [Bitcoin](#bitcoin) does for now, they will soon use validators that stake, or put forth ETH to create blocks and be rewarded in ETH. The reason for this switch is to make Ethereum scalable as the amount of users increases, and some things to look forward to are Ethereum being more energy efficient, more decentralized, having reduce hardware requirements, introducing shard chains, and achieving lower gas prices (which have had a recent surge, in part due to the [MEV crisis](/en/glossary/mining/#mev)).

## What are Gas and Gwei?{#gas-gwei}

Ether, the currency, has many denominations but the most commonly known is **Gwei** for its use in simplifying transaction fees, known on the Ethereum blockchain as **gas fees**. Gas is used to pay back miners for computing power costs, and everything on the Ethereum blockchain or using the EVM requires some amount of gas (larger smart contracts costing more). One Gwei is worth 0.000000001 ETH, so instead of saying that your gas costs 0.000000004 ETH, you could say that your **gas price** is 4 Gwei. Gas price is determined by miners and the amount of computing power required from them to process smart contracts and transactions, but users can adjust the gas price to get their transaction confirmed faster or slower depending on how long they want to wait. Miners are more likely to pick transactions with higher gas prices, since they keep those fees. During heavy network congestion gas has been known to get extremely expensive, like in February of 2021 when the average gas price was nearly $40.

## Ethereum's History{#ethereum-history}

Ethereum was proposed in 2013 by developer/programmer/writer Vitalik Buterin after trying to add a scripting language for application development to Bitcoin failed. Ethereum's [whitepaper](#whitepaper), which can be found [here](https://docs.google.com/viewerng/viewer?url=http://cryptoverze.com/wp-content/uploads/2018/11/Ethereum-ETH-whitepaper.pdf&hl=en), details how blockchain technology could be used for far more than just money, including but not limited to [non-fungible assets](#nfts), decentralized exchanges, and digital identities and reputations.

The formal work to build Ethereum began in 2014 with software development. [Gavin Wood](https://en.wikipedia.org/wiki/Gavin_Wood), whom would later go on to create [Polkadot](https://polkadot.network/), designed the EVM which allowed for smart contracts to be executed on the blockchain, and for applications to be built on top of Ethereum, like Vitalik had envisioned. Funding for development ran from July to August of 2014, where those that supported the project bought ETH, paying with BTC.

In June of 2016, Ethereum suffered an attack where a hacker stole $50 million. A hard fork occurred as a result, those that wanted to erase the attack from history would do so and stay under the name "Ethereum", while those that were fine with the attack being in the blockchain's history kept it and went under the name "Ethereum Classic".

## EIP 1559{#eip-1559}

**Ethereum Improvement Proposal (EIP) 1559** is part of the **London [hard fork](/glossary/forks)** and is set to take place on July 14, 2021, along with EIPs 3198, 3529, 3541, and 3554 as a step towards ETH 2.0. EIP 1559 in particular has grown to be quite controversial among miners, as it imposes a change to the fee structure of the Ethereum network. As it currently stands, fees go to the miners, but in the proposed changes there would be a base fee set by an algorithm in accordance to adjusting block sizes (also part of the London hard fork) and an option for users to tip miners. The base fee for each transaction would be burned, or removed from the total supply, putting some deflationary pressure on ETH. With fees making up a large percentage of the profits miners make, the proposal has faced some backlash and leaves open the possibility for a new version of Ethereum if miners don't get on board.


## Ethereum 2.0{#ethereum-2}

The goal of **Ethereum 2.0** is to increase the security, sustainability, and throughput, or transactions per second, of the network from tens to thousands by moving from a PoW blockchain to a PoS blockchain with sharding. The [genesis block](#genesis-block) of the Beacon Chain (Ethereum's new PoS blockchain, where eventually Ethereum will merge marking the launch of Ethereum 2.0) was mined on December 1st, 2020, and as of writing, it's prepped to launch some time in 2022. 