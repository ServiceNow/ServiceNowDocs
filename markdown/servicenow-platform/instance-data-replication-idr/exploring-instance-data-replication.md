---
title: Exploring Instance Data Replication
description: Instance Data Replication \(IDR\) replicates data updates on one instance, called the producer instance, to one or more other instances, called the consumer instances.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Exploring Instance Data Replication

Instance Data Replication \(IDR\) replicates data updates on one instance, called the producer instance, to one or more other instances, called the consumer instances.

## IDR overview

Maintain consistent data across different instances using IDR.

-   Automatically replicate data to one or more other instances.
-   Synchronize data between different organizations in your company or even between different companies with separate instances.
-   Data that is in transit during a crash is recoverable.

## IDR users

|User|Description|
|----|-----------|
|IDR admin|The IDR admin determines which tables and columns to replicate and analyzes table hierarchies and relationships. The IDR admin creates producer and consumer replication sets and monitors ongoing replication.|

## IDR workflow

This image shows how IDR replicates data from multiple tables on a producer instance to multiple consumer instances.

![Data replicates from a producer instance to one or more consumer instances.](../image/idr-concept-diagram-with-adapter.png "Replication overview")

1.  On the producer instance, the IDR admin specifies the tables and table columns to replicate by creating a producer replication set.
2.  The IDR admin activates the producer replication set, which makes the producer data available for replication to consumers.
3.  The IDR admin creates consumer replication sets on one or more consumer instances to receive the producer replication set data.
4.  On each consumer instance, the IDR admin requests approval from the producer instance.
5.  On the producer instance, the IDR admin approves or denies the requests from each consumer instance.
6.  On each approved consumer instance, the IDR admin activates the consumer replication set. After the consumer replication is activated, data that is updated in a producer replication set automatically updates the corresponding data in the consumer replication sets.
7.  On each consumer instance, the IDR admin can optionally replicate existing data from the producer instance by seeding data to the consumer instances.
8.  On either the producer or consumer instance, the IDR admin can optionally replicate data to tables or table columns that have different names on the consumer instance by configuring a transformation in the replication set.
9.  On either the producer or consumer instance, the IDR admin can optionally modify producer data before replicating it to a consumer by configuring an adapter in the replication set.

## IDR benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Continuously replicate inserts and updates from a producer instance to one or more consumer instances in near-real time, ensuring minimal delay.|[Continuous replication](continuous-replication.md)|Administrator|
|Schedule replication of historical inserts and updates from a producer instance to one or more consumer instances at predefined intervals.|[Scheduled replication](scheduled-replication.md)|Administrator|
|Continuously replicate inserts and updates from a producer instance to a consumer instance in near-real time, with changes on either side replicated back to the other.|[Bidirectional replication](bidirectional-replication.md)|Administrator|
|Continuously replicate inserts and updates from a producer instance to specific, distinguished consumer instances in near-real time, ensuring each consumer instance receives updates independently.|[Discrete replication](discrete-producer-replication-sets.md)|Administrator|
|Map producer data to tables and table columns that are named differently on consumer instances. For example, you can modify and map table columns to localize data for different locales.|[Transform replication data](../task/modify-replicated-data.md)|Administrator|
|Modify producer data before replicating it to a consumer instance using an adapter. For example, you can configure adapters that perform string and mathematical operations, such as converting one currency to another, or converting one time zone to another.|[Transform replication data](../task/modify-replicated-data.md)|Administrator|
|Trigger post-replication workflows such as generating notifications or validating replication using business rules.|[Triggering workflows after replication](modifying-replication-behavior-idr.md#)|Administrator|

## IDR limitations and when not to use IDR

-   Do not use IDR to clone instances.

    IDR does not replicate metadata tables, child metadata tables, and most user and system tables. IDR is designed to replicate data, not to clone instances. For example, the Application File \[sys\_metadata\] table and tables that extend \[sys\_metadata\] \(including the Business Rules \[sys\_script\], Catalog \[sc\_catalog\], and Workflow \[wf\_workflow\] tables\) are excluded and can't be replicated. For details on cloning, see .

-   Avoid using IDR to replicate a series of large attachments on a regular basis. If you need to include attachments that are larger than 10 MB regularly, monitor IDR to ensure that the lag time doesn't exceed expectations.
-   Avoid continuous replication of CMDB tables. Replicating CMDB data as changes occur can create performance issues or unforeseen consequences with replication due to the number of records involved. If you must replicate CMDB tables, consider scheduling replication or use conditions to constrain the count of replicated records and ensure all required columns are included in the replication set.
-   You cannot replicate Edge Encrypted, Field Encryption, and Password \(2-Way Encrypted\) fields.
-   IDR does not synchronize data archiving between instances. For example, archiving records or restoring archive records on a producer instance doesn't affect archived records on the consumer instance \(and vice versa\). You must create and manage archive rules for each instance independently.
-   Additional replication limitations:
    -   Maximum record size is 10 MB.
    -   Continuous replication supports up to approximately 1 million records per day.
    -   Seeding must not take longer than seven days to complete.
    -   You can only create one scheduled replication set in IDR, with only one outbound entry in that set.

**Warning:** IDR overwrites data on instances and can replicate sensitive data. Avoid potential data loss and data exposure, by testing your IDR implementation in a pre-production environment. See [data privacy in IDR](data-privacy-consumers-idr.md) for more information.

## What to explore next

To learn more about configuring and using IDR, see:

-   [Configuring Instance Data Replication](configuring-instance-data-replication.md)
-   [Replicating data with Instance Data Replication](replicating-data.md)
-   [Administering Instance Data Replication](administering-instance-data-replication.md)
-   [Instance Data Replication reference](reference-instance-data-replication.md)

