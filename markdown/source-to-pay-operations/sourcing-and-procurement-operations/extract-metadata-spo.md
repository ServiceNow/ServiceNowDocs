---
title: Start a metadata extraction for a contract from Source-to-Pay Workspace
description: Extract metadata from a signed contract attached in a contract repository record.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 1
breadcrumb: [Using Now Assist for Contract Management in Sourcing and Procurement Operations, Sourcing and Procurement Operations integration with Contract Management Pro, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Start a metadata extraction for a contract from Source-to-Pay Workspace

Extract metadata from a signed contract attached in a contract repository record.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

By default, the following use cases are available for Sourcing and Procurement Operations, which are mapped to the purchase requisition, purchase line item, and negotiation tables.

-   CM Pro - Contract Analysis
-   CM Pro - Contract Metadata Extraction

For more information, see [Metadata extraction using Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-metadata-extract-land&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

## Procedure

1.  Open the **Source-to-Pay Workspace**.

2.  Navigate to **Lists** &gt; **My work** &gt; **Open contract requests**

3.  Select a contract request that is in Closed complete or Contract signed state.

4.  Select **Initiate metadata extraction**.

    A message appears stating that the metadata extraction process has been initiated. You receive an email notification when the process is completed.

    The **Review extracted metadata** button appears on initiating the metadata extraction. You can select the button after the metadata extraction is completed.


## What to do next

Review the metadata extracted from a contract and add it to the contract repository. For more information, see [Work with extracted metadata](https://www.servicenow.com/docs/access?context=cncore-review-metatdata&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

The Extraction results tab in the contract repository record displays the processed metadata and their statuses, indicating whether the metadata have been successfully added to the mapped fields in the contract repository. For more information, see [Metadata extraction results](https://www.servicenow.com/docs/access?context=cncore-metadata-ext-results&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

**Parent Topic:**[Using Now Assist for Contract Management in Sourcing and Procurement Operations](../concept/use-now-assist-cmpro-spo.md)

**Related topics**  


[Enable Now Assist in Contract Management](activate-na-cmpro-spo.md)

[Analyze a contract document from Source-to-Pay Workspace](analyze-contract-spo.md)

