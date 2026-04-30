---
title: Choosing an Integration Approach
description: You have several options to integrate your data with your platform. Review the Integration Guidance decision matrix to determine which is the best approach for your needs.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the developer guide, Financial Services Operations \(FSO\)]
---

# Choosing an Integration Approach

You have several options to integrate your data with your platform. Review the Integration Guidance decision matrix to determine which is the best approach for your needs.

Some options can be used in tandem with others. For instance, a Hybrid Batch solution could be used to load certain account/policy data into the system. If a support agent wants to query updated information on a record, they could do a lookup and persist any new information from the external system onto the local table.

Consider the following questions when choosing an integration approach:

-   Are you comfortable with any data being stored locally? What about all data being stored locally?
-   Do you need to see all account types from a single list?
-   Must the data be current when viewing?
-   Must the user see all the customer's related accounts?

![Decision matrix to determine the most suitable integration approach.](../image/integration-decision-matrix.png)

## Using the FSO Remote Table Plugin

When choosing your integration approach, also consider using the FSO Remote Table plugin in comparison to creating your own custom remote tables.

The FSO Remote Table plugin provides extensions off the lowest level FSO tables that extend Sold Product. However, this data won’t appear on parent tables because it’s cached in memory.

The FSO Remote Table plugin is a good option if your agents only need to access individual accounts / policies from an interaction or case.

If agents need to see several types of accounts in a single list, or they need to see all account information when looking at a customer record, you may consider creating a custom remote table and make references to tables such as Customer and Case where applicable.

