---
title: Linking, delinking, and link conversion conditions
description: Several conditions can enable or disable you from linking, delinking, and hard or soft-linking records in Lead-to-Cash Process Management.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Lead-to-Cash Process Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Linking, delinking, and link conversion conditions

Several conditions can enable or disable you from linking, delinking, and hard or soft-linking records in Lead-to-Cash Process Management.

## Difference between hard and soft-linked nodes

Links can be toggled between hard and soft types based on whether they need to be actively monitored.

-   **Hard-linked nodes**

    A hard link is an active monitoring connection established by the sales process manager. When a record is hard linked, it’s actively tracked, and its emails and tasks are consolidated and visible in the sales process record. Hard links are represented by solid lines in the node map.

-   **Soft-linked nodes**

    A soft link is a passive connection based on database relationships. Records that are soft linked aren’t actively monitored by the sales process manager, and their emails and tasks aren’t consolidated in the sales process record. Soft links are represented by dotted lines in the node map.


## Conditions for linking and delinking records

Linking records: You can link records to all hard-linked nodes, including those records that are converted from soft links to hard links.

Delinking records: You can delink only hard-linked records and they must meet either of the following conditions:

-   The target node was added using the Link Records flow
-   The target node is a top-level entity

## Conditions for converting link types

Hard links cannot be converted to soft links if they meet the following conditions:

-   The target node was added using the Link Record flow.
-   The target node has immediate hard-linked child nodes but only one hard-linked source node.

Soft links can be converted to hard links only if the source node has at least one hard-linked record.

