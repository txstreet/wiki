---
title: Rollups
description: Rollups are a type of Layer 2 scaling solution.
published: true
date: 2021-06-12T00:35:18.209Z
tags:
editor: markdown
dateCreated: 2021-06-12T00:30:48.979Z
---

## What are Rollups{#rollups}

Rollups are currently the key layer 2 scaling solution for the [Ethereum](/en/ethereum) network, and it appears that they will continue carrying the weight of scaling the network until [Ethereum 2](/en/ethereum/#ethereum-2) rolls out sharding. The other layer 2 scaling solutions like Plasma and Channels move both data and computation off-chain (full layer 2), and although Rollups also move computation off-chain, they keep some data per transaction on-chain, along with **state storage** (hybrid layer 2). This data is kept on chain to verify via consensus that any given piece of data is available, resulting in less data availability issues. State storage is the data (like account balances) that is inside of the Rollup, and it needs to be kept on-chain in the form of a smart contract so that the two can interact as information is processed. Rollups work by updating the smart contract kept on-chain in a fashion very similar to [mining](/en/glossary/mining), but instead of pushing blocks to a blockchain, you push batches to a **state root** (the entire state of the system), which updates the layer 1 blockchain (in this case Ethereum).

## Types of Rollups{#rollup-types}

There are two types of Rollups: **Optimistic Rollups** that use **fraud proofs**, and **ZK Rollups** that use **validity proofs**. In fraud proofs, someone can discover an error in the end result of a state root and fix it by publishing a proof to the chain, showing how the end result was computed incorrectly. In validity proofs, every batch includes a cryptographic proof known as a **ZK-SNARK**, which is a short non-interactive zero-knowledge proof, or a way to verify computations quickly without any interaction between a prover and verifier. ZK SNARKS are commonly found in privacy coin protocols as a way to enhance privacy while maintaining accuracy of information.

A table from Vitalik Buterin's [An Incomplete Guide to Rollups](https://vitalik.ca/general/2021/01/05/rollup.html) can be seen below, highlighting the tradeoffs between Optimistic and ZK Rollups.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Property</th>
<th>Optimistic Rollups</th>
<th>ZK Rollups</th>
</tr>
</thead>
<tr class="odd">
<td>Fixed gas cost per batch</td>
<td><strong>~40,000</strong> (a lightweight transaction that mainly just changes the value of the state root)</td>
<td>~500,000 (verification of a ZK-SNARK is quite computationally intensive)</td>
</tr>
<tr class="even">
<td>Withdrawal period</td>
<td>~1 week (withdrawals need to be delayed to give time for someone to publish a fraud proof and cancel the withdrawal if it is fraudulent)</td>
<td><strong>Very fast</strong> (just wait for the next batch)</td>
</tr>
<tr class="odd">
<td>Complexity of technology</td>
<td><strong>Low</strong></td>
<td>High (ZK-SNARKs are very new and mathematically complex technology)</td>
</tr>
<tr class="even">
<td>Generalizability</td>
<td><strong>Easier</strong> (general-purpose EVM rollups are already close to mainnet)</td>
<td>Harder (ZK-SNARK proving general-purpose EVM execution is much harder than proving simple computations, though there are efforts (eg. <a href="https://medium.com/starkware/hello-cairo-3cb43b13b209">Cairo</a>) working to improve on this)</td>
</tr>
<tr class="odd">
<td>Per-transaction on-chain gas costs</td>
<td>Higher</td>
<td><strong>Lower</strong> (if data in a transaction is only used to verify, and not to cause state changes, then this data can be left out, whereas in an optimistic rollup it would need to be published in case it needs to be checked in a fraud proof)</td>
</tr>
<tr class="even">
<td>
    Off-chain computation costs
  </td>
<td>
    <strong>Lower</strong> (though there is more need for many full nodes to redo the computation)
  </td>
<td>
    Higher (ZK-SNARK proving especially for general-purpose computation can be expensive, potentially many thousands of times more expensive than running the computation directly)
  </td></p>