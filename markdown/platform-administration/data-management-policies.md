---
title: Managing data growth in Core UI
description: Manage the growth and storage of data on your instance by creating data management rules in Core UI.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing data growth in Core UI

Manage the growth and storage of data on your instance by creating data management rules in Core UI.

## Overview of managing data growth

Create and manage Data Management rules in Core UI.

-   [Create a data management policy in Core UI](../task/create-data-management-policy.md)

    Create a data management policy for any table that accumulates data that you want to archive or delete periodically.

-   [Archiving records in Core UI](archiving-older-records.md)

    Move records in a primary table to an archive table, including any records in other tables that reference those records.

-   [Deleting older or unwanted records in Core UI](deleting-older-records.md)

    Prevent data from growing exponentially by implementing table cleanup rules.

-   [Updating records safely in Core UI](updating-records-safely.md)

    Update several records simultaneously without using scripts by creating and executing a batch update job.

-   [Deleting records safely in Core UI](deleting-records-safely.md)

    Safely delete records from a table without using scripts and without deleting the table by creating and executing delete jobs.


-   **[Create a data management policy in Core UI](../task/create-data-management-policy.md)**  
Define a set of rules for managing table data on your instance.
-   **[Archiving records in Core UI](archiving-older-records.md)**  
Manage table size growth and improve query performance by archiving records.
-   **[Deleting older or unwanted records in Core UI](deleting-older-records.md)**  
Delete older, expired, or unwanted records from tables automatically.
-   **[Updating records safely in Core UI](updating-records-safely.md)**  
Update several records simultaneously without using scripts by creating and executing a batch update job.
-   **[Deleting records safely in Core UI](deleting-records-safely.md)**  
Safely delete records from a table without using scripts and without deleting the table by creating and executing delete jobs.
-   **[Migrating non-reference fields to reference fields](../../database-rotation/reference/archive-reference-migration.md)**  
Manually preserve sys\_ids in reference fields instead of storing the display name as a string.

**Parent Topic:**[Data Management](c_DataManagement.md)

