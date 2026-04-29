---
title: Conversational contract search and insights Workflow
description: Configure conversational contract search and insights workflow to enable searching information in contracts using natural language and dialogue-driven queries, making it easier to find relevant information.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Conversational contract search and insights Workflow

Configure conversational contract search and insights workflow to enable searching information in contracts using natural language and dialogue-driven queries, making it easier to find relevant information.

## Conditions for the Agentic Workflow to trigger

The Conversational contract search and insights is triggered when you enter queries in the Now Assist panel.

Contract fulfillers and assignment group managers with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller and now\_assist\_panel\_user role can view the agentic workflow conversation in the Now Assist panel.

**Note:** The agentic workflow isn’t supported in the Virtual Agent panel.

Conversational query supports the following types of searches:

-   Queries related to contract metadata. Example: List all contracts for the vendor Acme. Vendor is a metadata associated with the contract.
-   Queries related to clauses within contract documents. Example: List contracts that have a Confidentiality clause.
-   Combined queries related to fields in the contract AND clauses within the contract document. Example: List contracts for Acme vendor with Confidentiality clause.
-   Summarization and Q&amp;A on contract documents. Example: Summarize the contract CNTR21002.

