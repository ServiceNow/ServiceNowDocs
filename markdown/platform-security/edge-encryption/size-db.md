---
title: Calculate the order-preserving and tokenization database size
description: If using order-preserving encryption or encryption patterns, determine the size of your MySQL database by multiplying the number of potential records by record size.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Planning for Edge Encryption, Edge Encryption, Encryption]
---

# Calculate the order-preserving and tokenization database size

If using order-preserving encryption or encryption patterns, determine the size of your MySQL database by multiplying the number of potential records by record size.

## Before you begin

Role required: admin

## About this task

Use a dedicated machine to run the order-preserving and tokenization database. Do not run the database on the same hardware as the proxy server.

## Procedure

1.  Determine the potential number of records that could include fields encrypted with order-preserving encryption.

    1.  Multiply the number of encryption configurations using order-preserving encryption by the number of records each configuration is applied to.

    2.  To allow for growth, multiply the result by three.

2.  Multiply the result of step 1 by 1,536.

    1,536 is the average size of a record in bytes.

3.  If using encryption patterns, perform steps 1–2 for tokenized records and add the result to the total.


## Result

The calculated value is the recommended size in bytes for your order-preserving and tokenization database.

**Parent Topic:**[Planning for Edge Encryption](../concept/c_EdgeEncryptionPlanning.md)

