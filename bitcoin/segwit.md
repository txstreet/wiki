---
title: Segwit
description: 
published: true
date: 2021-03-15T13:52:46.562Z
tags: bitcoin
editor: markdown
dateCreated: 2021-03-15T13:52:46.562Z
---

## Summary{#summary}

Segwit was added to the Bitcoin (BTC) protocol in 2017 as a "soft fork" with backwards compatibility. The main function of segwit is removing the signature data (witness) from transactions and storing them in a separate area of the block that legacy nodes (nodes running bitcoin software from before segwit) cannot see. Segwit also removes the block size limit of 1mb (1,000,000 bytes), and replaces it with a "weight limit" of 4mwu (4,000,000 weight units), giving bitcoin a slight increase in transaction throughput, if utilized. However, it is not a simple 4x increase because the way in which the weight limit operates is complex.

Since segwit was a soft fork, both legacy nodes and segwit nodes can continue to operate on the same network. Both legacy transactions and segwit transactions can be relayed by all nodes. However, segwit transactions cannot be validated by legacy nodes, since they do not have access to the signature data, and have to assume that they are valid transactions. The main difference is how each node interprets and stores the data from each transaction.

When a segwit node receives a legacy transaction, it simply multiplies the size of that transaction in bytes by 4 and includes it in the block weight. Since the block weight is measured as 4x bigger than the block size, this means that if 100% of the transactions in a block were legacy transactions, it would be both 1mb and 4mwu at the same time, with a 0% transaction throughput increase. The increase comes from segwit transactions, which have their raw transaction data and signatures separated. The signature is added to the block weight at a rate of 1 byte to 1 weight unit, and the signatures are then easily accessible by segwit nodes. The rest of the transaction data again, has it's size in bytes multiplied by 4 and added to the block weight. So if 100% of the transactions in a block were segwit transactions, it would be larger than 1mb, but still would not come close to 4mb. Depending on the size of the raw transaction data, it would most likely be between 2-3mb.

When a legacy node receives a segwit transaction, it receives a smaller version of that transaction because the witness data (signatures) have been stripped. In the same scenario above, when 100% of the transactions in a block were segwit transactions, and the block was between 2-3mb, legacy nodes would still only receive 1mb of that data, because it is only the raw transaction data. This is how segwit achieves backwards compatibility with the 1mb block size limit. Legacy nodes have no knowledge or understanding of segwit, which means that a block with 100% legacy transactions, and 100% segwit transactions would look nearly identical. The only difference is that the legacy transactions would still have their signatures attached.

It is important to clarify that a block can have a mixture of both legacy and segwit transactions, and this is the case now in almost every block.
