---
title: Exploring Instance Data Replication
description: Instance Data Replication \(IDR\) replicates data updates on one instance, called the producer instance, to one or more other instances, called the consumer instances.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Exploring Instance Data Replication

Instance Data Replication \(IDR\) replicates data updates on one instance, called the producer instance, to one or more other instances, called the consumer instances.

## IDR overview

-   Data is automatically replicated to one or more other instances.
-   Data can be [modified and mapped to any table and table column](../task/modify-replicated-data.md) on other instances. For example, you can modify and map table columns to localize data for different locales.
-   Data that is updated on consumer instances can be [replicated to the producer instance](../task/bi-directional-replication.md).

    Data, such as problem requests, can be copied to consumer instances for third parties to use. The third party can update the problem issue on the consumer instance. The data can then be updated on the producer instance.

-   Business rules can trigger [post-replication workflows](../task/post-replication-actions.md), such as generating notifications or validating the replication.
-   Data that is in transit during a crash is recoverable.

## How Instance Data Replication works

You use the Instance Data Replication plugin \(com.glide.idr\) to replicate data updates on one instance, called the producer instance, to one or more other instances, called the consumer instances.

By configuring a producer replication set, you can specify the tables and table columns on the producer instance to replicate. When you configure a consumer data set, you can specify the tables and table columns on the consumer instances that receive the producer replication set data.

Next, you activate both producer and consumer replication sets to turn on the IDR functionality. The data that is updated in a producer replication set automatically updates the corresponding data in the consumer replication sets.

Syncing the producer and consumer replication sets requires that you do a one-time download \(called seeding\) of all the producer replication set data to the consumer instances.

You can initiate seeding requests on a consumer instance when you activate a consumer replication set. Beginning with the Rome release, you can use a filter criterion feature \(called partial seeding\) to restrict the number of records that are seeded. Use partial seeding to divide large jobs into smaller jobs when you have a large number of records to duplicate.

After seeding, replication involves data updates only. An audit trail contains a history of those record updates.

By default, the table data on a producer instance goes into the tables of the same name on consumer instances. [Transformation](../task/modify-replicated-data.md) is the process of replicating producer data in tables or table columns that have a different name on the consumer instances.

IDR [adapters](../task/modify-replicated-data.md) modify data before storing it on consumer instances. Adapters perform string and mathematical operations, such as converting one currency to another, or converting one time zone to another.

![Data replicates from a producer instance to one or more consumer instances.](../image/idr-concept-diagram-with-adapter.png "IDR overview")

**Warning:** IDR overwrites data on instances and can replicate sensitive data. Avoid potential data loss and data exposure, by testing your IDR implementation in a pre-production environment. See [data privacy in IDR](data-privacy-consumers-idr.md) for more information.

## IDR and instance upgrades

Upgrading your instance with IDR enabled is a seamless process.

-   IDR doesn't consume or produce messages during an instance upgrade. IDR jobs are automatically stopped when the upgrade begins.
-   The data\_replication\_queue tracks the timestamp of the last message sent. This ensures that replication resumes from the last change made prior to the upgrade.
-   Any seeding in progress before the upgrade will be automatically paused when the upgrade starts and will resume once the upgrade is completed. To ensure that seeding completes without interruptions, avoid initiating a seeding request before an upgrade.
-   Seeding requests can't be initiated during an instance upgrade.
-   Replication resumes immediately after the upgrade is completed. There is no need to make any adjustments to IDR for record replication to continue.

## IDR limitations and when not to use IDR

-   Do not use IDR to clone instances.

    IDR does not replicate metadata tables, child metadata tables, and most user and system tables. IDR is designed to replicate data, not to clone instances. For example, the Application File \[sys\_metadata\] table and tables that extend \[sys\_metadata\] \(including the Business Rules \[sys\_script\], Catalog \[sc\_catalog\], and Workflow \[wf\_workflow\] tables\) are excluded and can't be replicated. For details on cloning, see [System clone](https://www.servicenow.com/docs/access?context=c_SystemClone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   Avoid using IDR to replicate a series of large attachments on a regular basis. If you need to include attachments that are larger than 10 MB regularly, monitor IDR to ensure that the lag time doesn't exceed expectations.
-   Avoid continuous replication of CMDB tables. Replicating CMDB data as changes occur can create performance issues or unforeseen consequences with replication due to the number of records involved. If you must replicate CMDB tables, consider scheduling replication or use conditions to constrain the count of replicated records and ensure all required columns are included in the replication set.
-   You cannot replicate Edge Encrypted, Column Level Encryption, and Password \(2-Way Encrypted\) fields.
-   IDR does not synchronize data archiving between instances. For example, archiving records or restoring archive records on a producer instance doesn't affect archived records on the consumer instance \(and vice versa\). You must create and manage archive rules for each instance independently.
-   Additional replication limitations:
    -   Maximum record size is 10 MB.
    -   IDR supports replicating approximately 1 million records per day.
-   Limitations for seeding records:

    -   Replication seeding must not take longer than seven days to complete.
    -   Initial seeding of the tables must not exceed 3 million records per replication set.
    **Note:** To overcome these limitations, reduce the number of tables in the seeding request, reduce the size of the records, or use partial seeding.


