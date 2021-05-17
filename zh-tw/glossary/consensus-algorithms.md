---
title: Consensus Algorithms
description: Consensus algorithms are mechanisms in computer science that blockchains use to operate as intended.
published: true
date: 2021-05-17T16:31:17.364Z
tags: ethereum, bitcoin, bitcoin-cash, blockchain, monero
editor: markdown
dateCreated: 2021-05-14T03:15:41.556Z
---

## Summary{#summary}

Consensus algorithms are mechanisms in computer science that allow the users or nodes of a distributed network to coordinate and establish agreement upon a single truth so that everyone's copy of the ledger can update in real-time, making them essential for any blockchain. Proof-of-Work uses miners that solve cryptographic puzzles to be rewarded, Proof-of-Stake uses validators that lock up a coin to propose and vote on blocks in exchange for that same coin, Proof-of-Elapsed Time forces nodes to sleep for a random duration of time before picking blocks and being rewarded, and Proof-of-Authority uses trust and identity, with approved validator accounts. Regardless of the type of consensus algorithm, it is always feared that a 51% attack could take place, and sometimes they do on smaller blockchains, but as time goes on, these algorithms should continue to improve, offering solutions to those acting maliciously on networks.

## Types of Consensus Algorithms{#types-of-consensus-algorithms}

### Proof of Work{#pow}

There are many types of consensus algorithms used in blockchain technology, but the first was **Proof-of-Work**, or PoW, where validators (miners) use electricity and special hashing hardware to run data through a hash function to create a hash and solve cryptographic puzzles in hopes that the network will verify their data. If the miner has produced a valid hash that meets the conditions outlined by the PoW protocol, a reward will be issued, if rejected, no reward will be issued, and the money spent on operating costs will be a loss. The issue with PoW is the massive amount of energy consumption caused by it, and although the blockchains causing this issue are looking for fixes to implement, the energy consumption issue grows larger every day. As of March 2021, Bitcoin's energy consumption was estimated to be around 130TWh (Terawatt hours per year), more than many countries. Track current estimates of Bitcoin's energy consumption [here](https://cbeci.org/). **Proof-of-Burn**, or PoB, is a spinoff of PoW that addresses the high energy usage issues by enabling miners to burn tokens by sending them to a specific address, granting them access to write new blocks in proportion to the number of coins burnt. By doing so, miners receive a reward in the native currency of the blockchain.

### Proof of Stake{#pos}

**Proof-of-Stake**, or PoS, does away with the concept of miners and expensive hardware, saving on energy consumption as a result. To operate PoS correctly, the blockchain will keep track of a list of validators, which in this case, are holders of the coin that decide to stake it. Staking is the process of depositing funds to be locked up to become a validator and, amongst other validators, propose and vote on new blocks, with the weight each validator's vote depending upon the size of their stake and the reward depending upon the total amount staked by all users. There are two major types of PoS algorithms, although as more networks begin to utilize PoS, more types will emerge.

The first being **Chain-Based PoS**, where validators are pseudo-randomly chosen during time slots and assigned to choose a block they think can be added to the chain. That block must point back to a previously validated block, and this typically results in validators adding blocks to the longest existing chain until eventually a majority of the blocks will be on one extremely long chain, ensuring everyone has the same blockchain history.

The second being **BFT-style PoS**, where validators are assigned at random to propose blocks, and then vote in a multi-round process on individual blocks, essentially betting on which one will be chosen. Validators as a whole then decide which blocks are to be put on chain, and those that picked correctly in the proposing round are rewarded with the currency they are staking. There are some downsides associated  with PoS just as there are with PoW. Because validators aren't necessarily trying to lengthen one chain, they run the risk of causing a hard fork by continuing to validate blocks on a short or no longer accurate chain. The name BFT refers to the Byzantine fault tolerance, which is the network's ability to decipher whether or not a node is considered good or bad when there is insufficient information. It is possible for a network failure to occur in response to a byzantine fault, which happens when some nodes start presenting different network symptoms to different nodes, in turn nullifying the information on that node so that it appears both failed and functioning.

To combat these issues, Ethereum chose to adopt the **Casper PoS Consensus Protocol** when it made the decision to go from PoW to PoS. Casper acts the same as BFT-style in every way except one, it grants the network the ability to punish any node that goes offline or acts maliciously by slashing off their stake. This helps to ensure blocks get validated at a faster rate and prevents unnecessary hard forks and attacks. Not everyone in a network can afford to run a node that is guaranteed to stay online all the time, so to avoid running the risk of losing their stake, users can stake on an exchange in turn for a fee of their reward.

Another twist on the PoS algorithm is **Delegated Proof-of-Stake**, or DPoS, where users of the network can vote for witnesses and delegates in a continuous election voting  process to incentivize them to refrain from malicious behavior. Witnesses are meant to create and validate blocks and are rewarded in fees for each transaction they validate. Delegates have the power to change transaction fees, block sizes, witness pay, and block intervals, but despite all this, delegates are not paid. This algorithmic strategy ensures that every user in the network gets a vote if they choose to use it, thus creating a digital democracy.

### Proof of Elapsed Time{#poet}

**Proof-of-Elapsed Time**, or PoET, was developed by [Intel](https://www.intel.com/content/www/us/en/homepage.html?cid=sem&source=sa360&campid=2021_ao_gmc_us_mbcbu_mbe3_bp_text-link_brand_exact_cd_intel-brand-refresh-intel_O-2FX5D_google_b2c_is_nonpbm&ad_group=brand_intel_b2c1-awa&intel_term=intel&sa360id=43700060054833261&gclsrc=ds&gclsrc=ds) and is meant for permissoned blockchains, which require special verification from a node when joining. PoET algorithms work by generating and sending out a random wait timer to each node in the network and forces the nodes to sleep for the specified amount of time. The first node to wait their time will wake up and receive the block, along with being allowed to add a new block to the chain, before that information is sent off to the entire network. This process is repeated indefinitely, and because of the nodes being put to sleep for set amounts of time, these blockchains are far more energy efficient than any PoW or PoS blockchain.

### Proof of Authority{#poa}

**Proof-of-Authority**, or PoA, is an algorithm focused on the reputation of the validators and a high level of trust in the network. Validators wait time, just the same as PoET, however instead of staking resources validators stake their identities and reputations, and are pre-approved by the network, as PoA is meant for private blockchains. This stops validators from committing any malicious activity, as their identities are attached. They run software that allows them to put transactions in blocks autonomously, but it does require an uncompromised node, so validators in a PoA network should be very reliable.

## 51% Attack{#51attack}

A 51% attack refers to a group of people within a network coming together to pool more than 50% of the network's computing power with the intent of malicious activity. When this happens, the group with 51% power is able to prevent new transactions from going through, halt payments between any users, and reverse transactions, opening up the door for them to double-spend coins. Double spending is an issue that is specific to digital currencies, because physical currencies cannot be easy manipulated or replicated, while digital currencies can be in the circumstance of a network failure, more than likely spurred by a 51% attack.
