---
title: Gnosis
description: 
published: true
date: Mar-04-2021 05:21:29
tags: ethereum, gnosis
editor: markdown
dateCreated: Mar-04-2021 05:21:29
---

![Gnosis](https://txstreet.com/static/img/singles/house_logos/gnosis.png)

## Summary{#summary}

Gnosis Protocol v2 is a fully permissionless trading protocol that runs sophisticated batch auctions to allow users to get better on-chain prices and MEV protection for their trades. The protocol leverages an open competition of solvers to find the most optimal settlement solution for each batch. Within each batch, solvers can match traders directly without external liquidity via the Coincidence of Wants phenomena.  Additionally, if there is not enough liquidity inside a batch, solvers can tap into all available on-chain liquidity to facilitate the trading. 

CowSwap (https://cowswap.exchange/#/swap) is the first trading interface built on top of Gnosis Protocol v2. It allows you to buy and sell tokens using gas-less orders that are settled peer-to-peer among it's users or into any on-chain liquidity source or , while providing MEV protection.


## Config{#config}

Below is a json config file used by TxStreet, including a list of contracts.
[gnosis.json](/ethereum/houses/gnosis.json)
