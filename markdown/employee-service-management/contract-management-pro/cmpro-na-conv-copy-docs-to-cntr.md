---
title: Copy contract documents to contract repository
description: Copy signed contract documents into the contract repository for conversational search.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Configure conversational search, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Copy contract documents to contract repository

Copy signed contract documents into the contract repository for conversational search.

## Before you begin

Role required: admin

## About this task

Contract documents must be stored in the contract repository to enable conversational search and retrieve queried information. For existing contracts, run the scheduled job **CM Pro – Copy Signed Document Revision to AST Repo** to copy signed contract documents into the repository.

For new contracts, the scheduled job runs automatically when the contract request moves to Closed complete state.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

2.  Search for **CM Pro Copy Signed Document Revision to AST repo** and open the job.

3.  Select **Execute Now**.

    ![Scheduled job to copy contract documents to the contract repository](../image/cmpro-na-conv-search-job.png "Scheduled job to copy contract documents to the contract repository")


## Result

The signed contract documents are copied into the contract repository.

## What to do next

Index data for conversational search. [Index contracts table for conversational search](cmpro-converse-search-indexing.md)

