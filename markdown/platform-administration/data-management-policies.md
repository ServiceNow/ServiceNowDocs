---
title: Managing the growth of data on your instance
description: Manage the growth and storage of data on your instance using data management policies.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing the growth of data on your instance

Manage the growth and storage of data on your instance using data management policies.

## Key benefits

-   Access all of a table's data management rules from the table's data management policy record.
-   Simplify data management administration by defining multiple archive rules and table cleaner rules in one place.
-   Coordinate the data management effort among your administrators and easily locate all the data management rules that exist for each of your tables.
-   Activate or deactivate all rules at once by updating the data management policy record.

## Accessing data management policies

You can define and access the data management policy for a table by navigating to **All** &gt; **System Data Management** &gt; **Data Management Policies**.

## Use cases

-   View and update the data management policy for tables with archive rules or table cleaner rules. After upgrading to at least Xanadu, data management policies are automatically created for any table with an archive rule or table cleaner rule.
-   Create a data management policy for any table that accumulates data that can be archived or deleted periodically. Create archive rules and table cleaner rules to manage the growth of data.

-   **[Create a data management policy](../task/create-data-management-policy.md)**  
Define a set of rules for managing the data in a table on your instance.
-   **[Archiving records](archiving-older-records.md)**  
Manage table size growth and improve query performance by archiving records.
-   **[Deleting older or unwanted records](deleting-older-records.md)**  
Delete older, expired, or unwanted records from tables automatically.

**Parent Topic:**[Data Management](c_DataManagement.md)

