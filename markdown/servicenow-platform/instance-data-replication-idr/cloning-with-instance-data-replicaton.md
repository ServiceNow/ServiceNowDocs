---
title: Cloning options with Instance Data Replication
description: Ensure that certain tables are preserved or excluded to clone your database from one instance to another successfully with Instance Data Replication \(IDR\).
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Cloning options with Instance Data Replication

Ensure that certain tables are preserved or excluded to clone your database from one instance to another successfully with Instance Data Replication \(IDR\).

There are multiple methods for copying an IDR configuration from one instance to another.

-   **Capture the configuration in an update set**

    An update set captures a group of configuration changes that you can move from one instance to another but doesn’t include data that a producer replicates to a consumer. You can capture a snapshot of an IDR replication configuration, including selected fields, filters, or data transformations using the **Track in Update Set** option, and then copy it to another instance using an update set. See [Deploying a replication configuration from one instance to another in Instance Data Replication](copying-replication-configuration.md).

-   **Copy the configuration using a clone profile**

    Cloning your instance copies everything in the database from one instance to another, including the data and the IDR replication configuration.

    Before you clone your instance, you must determine whether to exclude or include your IDR replication configuration.

    For details on cloning, see [Instance Clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md).


## IDR cloning use cases

You must preserve and exclude different sets of IDR tables in your cloning profile depending on your cloning use case.

-   **Recurring clone**

    In this use case, you clone your source instance regularly without affecting the existing IDR configuration on the target instance.

    For example, you configure IDR to replicate data from instance A to instance B. You determine that you must clone the database from instance A to another instance called instance C. Instance A and instance C both have IDR configured with different replication configurations. When you clone the database from instance A to instance C, you don’t want to clone any of the IDR replication configuration from A to C.

    **Note:** If you regularly clone data from your source instance to your target instance, and find that you need to copy the IDR replication configuration from the source instance to the target instance, use the **Track in update set** feature to copy the IDR to the target instance.

    To clone your database from one instance to another without affecting the IDR configuration on the target instance, you must update the preserve and exclude lists in your cloning profile according to the Recurring Clone use case described in [KB0965218](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0965218).

-   **True clone**

    In this use case, you clone your source instance to your target instance and include the complete IDR replication configuration. The target instance inherits everything from the source. After the clone is finished, you must resubscribe all consumer instances to the target instance.

    For example, you decide to provision a new production instance from a non-production instance that already has IDR configured. When you clone the non-production instance, the new production instance inherits everything from the non-production instance. To ensure that data replicates from the production instance and not the non-production instance, you resubscribe all consumer instances to the new production instance.

    To clone your database and copy the current IDR configuration to the target instance, you must update the preserve and exclude lists in your cloning profile according to the True Clone use case described in [KB0965218](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0965218).

-   **Migration clone**

    In this use case, you clone your source instance to the target instance, including the complete IDR replication configuration from the source instance, while preserving the target instance’s replication configuration.

    The migration clone involves performing a true clone, but with additional steps.

    1.  On the target instance, you create an update set and use the **Track in update set** feature to upload the existing replication sets on the target instance into the update set.
    2.  Perform a true clone.
    3.  After performing the true clone, you import the update set to the target instances, and you set up replication sets using entry sets to preserve the configuration.

<table id="table_jzx_kjx_cbc"><thead><tr><th>

Use case

</th><th>

Description

</th><th>

Prerequisites

</th><th>

Post requisites

</th></tr></thead><tbody><tr><td>

Recurring clone

</td><td>

Clone your source instance to your target instance regularly but exclude your IDR replication configuration.When complete,replication sets on the target instance should not be changed.

</td><td>

Verify that IDR is configured correctly, and that replication is successful on both the source and target instances.

</td><td>

After performing a recurring clone, you can copy the IDR replication configuration from the source instance to the target instance using the **Track in update set** feature.

</td></tr><tr><td>

True clone

</td><td>

Clone your source instance to your target instance and copy your IDR configuration to the target instance.When complete, entry sets from the source instance should be cloned to the target instance.

</td><td>

Verify that IDR is configured correctly, and that replication is successful on the source instance.

</td><td>

After performing a true clone, you must perform the following actions on the target instance:1.  Re-create the replication sets using the cloned entry sets from the source instance.
2.  Resubscribe each consumer to the newly-provisioned producer.

</td></tr><tr><td>

Migration clone

</td><td>

Clone your source instance to your target instance and copy your IDR configuration to the target instance, while preserving the target instance’s replication configuration.When complete, entry sets from the source instance should be cloned to the target instance.

</td><td>

1.  Capture the existing replication sets on the target instance in an update set using the **Track in update set** feature.
2.  Perform a true clone.

</td><td>

After performing the true clone, you must perform the following actions on the target instance:1.  Import the update set.
2.  Re-create the target replication sets using the entry sets captured in the update set.
3.  Re-create the source replication sets using the cloned entry sets from the source instance.

</td></tr></tbody>
</table>**Parent Topic:**[Administering Instance Data Replication](administering-instance-data-replication.md)

**Related topics**  


[Manage consumer access to replication data in Instance Data Replication](../task/approve-consumer.md)

[Comparing replicated data between instances in Instance Data Replication](comparing-replicated-data.md)

[Deploying a replication configuration from one instance to another in Instance Data Replication](copying-replication-configuration.md)

[Monitoring replication status in Instance Data Replication](instance-data-replication-dashboard.md)

[Monitoring queues in Instance Data Replication](idr-queue-dashboard.md)

[Avoiding insert and update errors in Instance Data Replication](preventing-insert-update-errors.md)

[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

