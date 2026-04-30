---
title: Preparing for Instance Data Replication
description: Before you set up Instance Data Replication \(IDR\), analyze the tables and columns in the producer and consumer instances to replicate data successfully.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Instance Data Replication set up, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Preparing for Instance Data Replication

Before you set up Instance Data Replication \(IDR\), analyze the tables and columns in the producer and consumer instances to replicate data successfully.

## Deciding which tables to replicate

Before you create a producer replication set, decide which tables to replicate. Avoid replicating system tables \(tables with a sys\_ prefix\). If you replicate system tables \(like sys\_user, sys\_user\_group, or sys\_user\_grmember\) that have existing data in the consumer instance, insert and update failures can occur during replication. If you decide to replicate these tables, you may have additional work afterwards to clean these tables.

Avoid replicating CMDB tables. Replicating CMDB tables can create performance issues or unforeseen consequences with replication due to the number of records involved. If you determine the CMDB tables must be replicated, use conditions to constrain the count of replicated records and ensure all required columns are included in the replication set.

For a list of tables you should avoid replicating, see [Excluded tables in Instance Data Replication](../reference/IDR-excluded-tables.md).

## Analyzing table hierarchies

For each table you want to replicate, determine if the table is a parent or child table. If the table belongs to a parent-child hierarchy, decide if you want to preserve the hierarchy and what strategy you want to use to move the hierarchy from the producer to the consumer.

**Important:** To maintain data integrity and ensure that reference fields are populated on the consumer as you'd expect, you must replicate all of the parent and child tables in the table hierarchy.

See [Preserving table hierarchy in Instance Data Replication](preserving-table-hierarchy.md).

## Analyzing table relationships

For each table you want to replicate, determine if the table has reference fields that point to other tables. If you are replicating a table with a reference field that points to another table, but you don’t include that table in your replication set, the reference field will be empty in the record on the consumer instance. Replicating table relationships maintains data integrity and ensures that reference fields are populated on the consumer as you'd expect.

## Organizing replication sets

As part of the planning phase, determine how you want to organize your replication sets and the tables they contain.

-   Create a single replication set for each table. This option requires more setup, configuration, and time management, but allows you to pause replication for a single table without impacting other tables.
    -   Replication is performed in parallel using multiple jobs.
    -   Throughput metrics are easier to track with separate replication sets.
    -   When an error occurs, replication for a single table is affected instead of all multiple tables.
-   Create a replication set for a group of related tables. This option is easier to set up and manage, but oversight and potential issues impact all tables in the group.

    -   If you need find information about replication status, the logical name you use for this replication set might be easier to find and understand compared to using distinct replication sets for each table.
    -   If you want to pause replication, you can do so for the entire group of tables by pausing replication from one replication set.
    -   If a replication issue occurs on one table and replication stops, this stops replication for all tables in the replication set.
    If you decide to group tables in a single replication set, try to limit it to five or fewer tables. If you have more than five tables to replicate, use multiple replication sets with five or fewer tables in each set.


## Deciding which columns to replicate

For each table you want to replicate, decide which columns to include. Avoid including every column in your replication set by default. Instead, decide which columns are necessary, and exclude any sys\_ columns or other columns that are updated by scripts automatically.

For example, if you include a column updated by the system automatically on a frequent basis, IDR may replicate data more often than necessary. When the system replicates this data, it can negatively impact the capacity subscription. Periodically check the **IDR License and Usage Details** dashboard to monitor the message count that is generated from the producer.

## Preparing target tables on the consumer instance

By default, IDR uses a record's sys\_id field as the lookup value to keep data synchronized between the producer and consumer instance. If the target table contains existing data or records from prior data imports, the sys\_id values in the consumer don't match the sys\_ids from the producer instance.

Always consider the producer instance as the source of truth. For optimal replication results, follow these guidelines:

-   Make the producer instance the exclusive data source for the consumer instance.
-   Prior to replication, ensure that the target table in the consumer instance is empty. Ideally, the initial records in the target instance are created from data sent exclusively from the producer via a replication set or a clone.
-   Ensure that there are no other ongoing data imports or updates to target tables on the consumer instance after replication starts.

For example, if users from LDAP are imported to the consumer instance using a different data source, the sys\_ids for those records don't match the sys\_id values in the producer instance. In this scenario, existing user records in the target table on the consumer aren't updated and duplicate records are created.

In situations where this cannot be avoided, clean the tables on the consumer instance prior to replication. You must delete the records in the target table or ensure the sys\_id values in producer and consumer are the same.

Alternatively, you can use a custom **Coalesce** field to identify unique records \(instead of the default sys\_id column\) for replication. Use a custom **Coalesce** column when records on the consumer instance have a different sys\_id for the same records on the producer instance. For more information on using a custom **Coalesce**, see [Coalesce columns in Instance Data Replication](idr-coalesce.md).

## Reviewing business rules

You can use business rules to trigger workflows after replication, such as sending a notification or validating the replicated data. Review any business rules on the consumer instance that might prevent the idr.system user from inserting, updating, or deleting records in the target table.

If failures related to business rules occur, they appear in the **Instance Data Replication** &gt; **Replication Payload Error** table on the consumer instance. View the **Error Message** field for details on the script that is causing the failure.

With bidirectional replication, records created on the producer instance are replicated to a consumer instance and vice versa. When the record is inserted on the consumer instance and it triggers a business rule that updates the record, that update is not replicated back to the producer instance.

## Reviewing ACLs

Review the ACLs in place on the target table in the consumer instance to ensure that IDR can replicate data successfully. Confirm that the idr.system user has the appropriate roles for the target table.

If failures related to ACLs occur, they appear in the **Instance Data Replication** &gt; **Replication Payload Error** table on the consumer instance. View the **Error Message** field for details on the ACL that is causing the failure.

## Reviewing data policies

Review any data policies in place on the target table in the consumer instance to ensure that IDR can replicate data successfully. Confirm that the data you are replicating satisfies the data policy.

If failures related to data policies occur, they appear in the **Instance Data Replication** &gt; **Replication Payload Error** table on the consumer instance. View the **Error Message** field for details on the data policy that is causing the failure.

**Parent Topic:**[Instance Data Replication set up](instance-data-replication-set-up.md)

**Related topics**  


[Request an Instance Data Replication subscription](../task/request-instance-data-replication.md)

[Preserving table hierarchy in Instance Data Replication](preserving-table-hierarchy.md)

[Upgrading legacy replication sets to V2 in Instance Data Replication](upgrading-legacy-replication-sets-v2.md)

