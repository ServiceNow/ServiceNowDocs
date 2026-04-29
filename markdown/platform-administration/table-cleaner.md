---
title: Table cleaner
description: Prevent tables from growing to an unmanageable size by deleting records automatically.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table cleaner

Prevent tables from growing to an unmanageable size by deleting records automatically.

## Key benefits

-   Improve query performance by deleting records you no longer need.
-   Delete older, expired, or unwanted records from tables automatically.
-   Prevent data from growing exponentially.

## Accessing table cleaner rules

You can define and access table cleanup rules for a table by navigating to **All** &gt; **System Data Management** &gt; **Data Management Policies** and selecting the data management policy for the table.

## Use cases

-   Delete closed incidents that haven't been updated in 30 days. In this scenario, you define a table cleanup rule on the Incident \[incident\] table using sys\_updated\_on as the match field and you specify 2,592,000 as the age in seconds. You specify the condition State is Closed to only delete closed incidents.
-   Manage data growth in tables used by Virtual Agent and Conversational Interfaces by activating table cleanup rules for the following tables:
    -   Chat Server \[sys\_cs\_analytics\]
    -   Conversations \[sys\_cs\_conversation\]
    -   Message Last Reads \[sys\_cs\_message\_last\_read\]
    -   Ci Analytics \[sys\_ci\_analytics\]
-   Conversation-related tables can increase in size and end up affecting system performance. Limit data growth by cleaning records in tables related to Advanced Work Assignment. See .

For information on using table cleaner, see [Deleting older or unwanted records in Core UI](deleting-older-records.md).

