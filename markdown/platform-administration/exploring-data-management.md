---
title: Exploring Data Management
description: Learn about Data Management capabilities and how they help you manage table data in the ServiceNow AI Platform.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Exploring Data Management

Learn about Data Management capabilities and how they help you manage table data in the ServiceNow AI Platform.

## Data Management overview

The Data Management capabilities enable you to manage the growth of data in your instance using data management policies.

-   Define and access a set of data management rules for a table using a data management policy.
-   Manage the growth of data on your instance by archiving and cleaning table data.
-   Visualize a summary of storage consumption on your instance.

## Data Management users

|User|Description|
|----|-----------|
|Administrator|Monitor growth and storage of data on the instance. Configure data management policies to archive and delete older records.|

## Data Management workflow

This infographic depicts how an administrator uses a data management policy to configure data management rules for a table and monitor data usage on an instance.

![Infographic depicting how an administrator uses a data management policy to configure data management rules for a table and monitor data usage. For details, refer to the following description.](../image/mmasset0020353-data-management-workflow-landing.png "Managing data on your instance")

1.  The instance admin monitors cloud storage entitlements and data usage at the account-level in Subscription Management.
2.  The instance admin finds that one instance is consuming a greater amount of storage than expected and decides to investigate.
3.  The instance admin logs in to the instance and analyzes which tables are consuming the most data by viewing the Data Usage Visualization Console dashboard. The instance admin notices that two tables are consuming more data than expected.
4.  The instance admin reviews the data management policies for the tables in question. One of the tables has never been archived or cleaned before, so the instance admin creates a data management policy for this table.
5.  The instance admin determines that older records in one of the tables can be moved to an archive table. The instance admin creates multiple archive rules using different criteria to move data from the primary table to an archive table.
6.  The instance admin decides that older records in the other table aren't needed after a certain date. The admin adds a table cleaner rule to the data management policy that deletes records from the table periodically as the records age out.
7.  After the archive and table cleaner jobs are finished, the instance admin continues to monitor the Data Usage Visualization Console dashboard to verify that data consumption is reduced and continues to monitor the top 10 tables.

## Data Management benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Archive older records|[Data archiving](../../database-rotation/concept/c_ArchiveData.md)|Administrator|
|Delete older or unwanted records automatically|[Table cleaner](table-cleaner.md)|Administrator|
|Monitor data usage on your instance over time|[Viewing data usage on your instance](viewing-data-usage.md)|Administrator|

## What to explore next

To learn more about configuring and using Data Management, see:

-   [Managing the growth of data on your instance](data-management-policies.md)
-   [Updating records safely](updating-records-safely.md)
-   [Deleting records safely](deleting-records-safely.md)
-   [Database rotation](../../database-rotation/concept/c_DatabaseRotation.md)
-   [Data Management reference](../reference/data-management-reference.md)

