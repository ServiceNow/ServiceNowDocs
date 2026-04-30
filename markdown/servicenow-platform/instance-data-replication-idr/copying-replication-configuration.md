---
title: Deploying a replication configuration from one instance to another in Instance Data Replication
description: Copy a replication configuration from one instance to another through an update set in Instance Data Replication \(IDR\).
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Deploying a replication configuration from one instance to another in Instance Data Replication

Copy a replication configuration from one instance to another through an update set in Instance Data Replication \(IDR\).

In IDR, you can capture a snapshot of a replication configuration, including selected fields, filters, or data transformations using the **Track in Update Set** option, and then copy it to another instance using an update set.

**Important:** The **Track in Update Set** option in IDR is the only supported method for capturing a replication configuration that you want to copy to another instance.

## Key benefits

-   Save time by defining a replication configuration once and using it as a template for new replication sets on other instances.
-   Minimize potential impact to your production instance by developing a replication configuration in your sub-prod instance first.
-   Verify a replication configuration in a sub-prod instance before rolling it out to a production instance.

## Configuration entities

The following configuration entities are captured in an active update set when you select the **Track in Update Set** option.

-   **Entry set**

    An entry set is a bundle of replication entries \(like a replication set\), that doesn't contain any instance-specific metadata like the Producer ID. A new Producer ID is used in the target instance when you create a producer replication set based on an entry set.

    Replication options that are tracked in an entry set and their status \(active or inactive\) include:

    -   Bi-directional replication
    -   Discrete value mapping
-   **Replication entries**

    A replication entry contains configuration settings for each table that you want to replicate. Replication entries are either outbound or inbound.

    -   Outbound entries from a producer instance contain the source table, filter, fields you want to replicate, and data transformation settings.
    -   Inbound entries from a consumer instance include the target table, the option to run business rules after replication, and data transformation settings.

## Viewing an entry set and replication entries

When you create a replication set, a new record is added to the Entry Sets \[idr\_entry\_set\] table. New records are added to the Replication Entries \[idr\_replication\_entry\] table for each outbound entry that you add to the replication set.

After selecting **Track in Update Set**, you can view the entry set and its replication entries in the current update set by navigating to **All** &gt; **System Update Sets** &gt; **Local Update Sets**, selecting the update set, and then viewing the **Customer Updates** tab.

-   **[Deploy a replication configuration through an update set in Instance Data Replication](../task/deploy-through-update-set.md)**  
Export a replication configuration from one instance and import it on another instance through an update set in Instance Data Replication \(IDR\).

**Parent Topic:**[Administering Instance Data Replication](administering-instance-data-replication.md)

**Related topics**  


[Manage consumer access to replication data in Instance Data Replication](../task/approve-consumer.md)

[Comparing replicated data between instances in Instance Data Replication](comparing-replicated-data.md)

[Cloning with Instance Data Replication](cloning-with-instance-data-replicaton.md)

[Monitoring replication status in Instance Data Replication](instance-data-replication-dashboard.md)

[Monitoring queues in Instance Data Replication](idr-queue-dashboard.md)

[Avoiding insert and update errors in Instance Data Replication](preventing-insert-update-errors.md)

[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

