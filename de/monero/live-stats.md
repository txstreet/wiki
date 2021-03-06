---
title: Live Stats
description: Descriptions of live how live statistics are calculated on TxStreet.
published: true
date: 2021-04-19T23:03:12.582Z
tags: monero
editor: markdown
dateCreated: 2021-04-19T15:36:10.924Z
---

## Broadcasted Tx/Sec{#broadcasted-txsec}

Broadcasted transactions per second measures the number of new and unique transactions broadcasted within the last 5 minutes. This number is then divided by 300 to reach an average "per second" result.

## Confirmed Tx/Sec{#confirmed-txsec}

Confirmed transactions per second measures rate of confirmed transactions per second over the past hour. If there was no confirmed block in the past hour, the timespan is increased past one hour to the last block's timestamp.

## Mempool Size{#mempool-size}

Mempool Size measures the sum of the size (Megabytes) of the pending transactions in the mempool on the TxStreet Monero node.

## Mempool Count{#mempool-count}

Mempool Count measures the total number of pending transactions in the mempool on the TxStreet Monero node.

## Median Fee (USD){#median-fee-usd}

Median Estimated Fee (USD) measures the median fee in USD from new and unique transactions broadcasted within the last 5 minutes.

## Median Fee (XMR){#median-fee-xmr}

Median Estimated Fee (XMR) measures the median fee in XMR from new and unique transactions broadcasted within the last 5 minutes.

## Median Fee (Nanoneros/Byte){#median-fee-nanonerosbyte}

Median Estimated Fee (Nanoneros/Byte) measures the median fee in Nanoneros per Byte from new and unique transactions broadcasted within the last 5 minutes. A Nanonero is 0.000000001 XMR.

## Bytes Per Second{#bytes-per-second}

Bytes Per Second measures the sum of the size (Bytes) of each new and unique transaction broadcasted within the last 5 minutes. This number is then divided by 300 to reach an average "per second" result.

## Last Block{#last-block}

Last Block is the difference in time from now and the timestamp attached to the last block. The timestamp is generated by miners and is not exact, which is why the measurement may be higher than the truth.

## Median Txs Per Block{#median-txs-per-block}

Median Txs Per Block measures the median number of transactions included in each block over the last hour.

## Median Block Size{#median-block-size}

Median Block Size measures the median data used by a block (in megabytes) over the last hour.

## Current Block Size Limit{#current-block-size-limit}

Current Block Size Limit measures the dynamic block size limit calculated by Monero nodes. This value can change after every block, as it is twice the median block size of the last 100 blocks.

## Average Block Time{#average-block-time}

Average Block Time measures the average time between mined blocks over the last 250 blocks.