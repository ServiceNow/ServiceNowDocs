---
title: Create a producer replication set in Instance Data Replication
description: Specify the tables and columns on the producer instance that you want to replicate in Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a producer replication set in Instance Data Replication

Specify the tables and columns on the producer instance that you want to replicate in Instance Data Replication \(IDR\).

## Before you begin

Verify that the producer and consumer instances belong to the same customer.

Plan your data replication strategy by reviewing the important considerations described in [Preparing for Instance Data Replication](../concept/prepare-instance-data-replication.md).

Role required: idr\_admin or admin

## About this task

Creating the producer replication set is the first step of setting up Instance Data Replication. Seeding is the initial download of all the records in the producer replication set to the tables in the consumer replication set. After seeding, Instance Data Replication \(IDR\) only replicates data updates. The seeding limitations are:

-   The maximum record size is 10 MB.
-   The maximum seeding size is 3 million records.

    **Note:** If your replication set contains more than 3 million records, seeding cannot start. To fix this situation, break the replication set into multiple replication sets with fewer records in each or use partial seeding.

-   The maximum seeding time is 7 days.

![Seeding from the producer replication set.](../image/IDR-producer-seeding.png "Seeding replication sets")

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets** and click **New**.

2.  On the form, fill in the fields.

<table id="table_gmk_zs1_plb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Names can only contain alphanumeric characters and hyphens. **Note:** The consumer replication set must have the same name as the producer replication set, so the name should not be producer-specific.

</td></tr><tr><td>

Bi-Directional

</td><td>

Option to enable bi-directional replication on consumer instances. Bi-directional replication enables changes to records made on the consumer instance to propagate to the producer instance. If you want to set up a producer replication set with bi-direction for consumer instances, see [Bidirectional replication](bi-directional-replication.md).

</td></tr><tr><td>

Discrete

</td><td>

Option to enable discrete mapping from a producer replication set. This mapping distinguishes different consumer instances. For more information, see [create discrete mappings for a producer replication set](discrete-producer-replication-set.md).

</td></tr><tr><td>

Description

</td><td>

Description of the replication set.

</td></tr><tr><td>

Entry Set

</td><td>

Set of outbound entries. If you imported an update set from another instance or you created one earlier on your instance, you can choose an existing entry set.

</td></tr></tbody>
</table>    After you submit the Producer Replication Set form, the system auto-generates the producer ID. The **Producer ID** field identifies the producer instance in the system.

    ![Producer replication set.](../image/producer-replication-set.png)

3.  To add outbound entries to your producer replication set, click the **Outbound Entries** tab and click **New**.

4.  On the form, fill in the fields.

    For each outbound entry, you must select a source table from the producer instance to replicate data records. You can also select associated table columns, include attachments to records, and set filter conditions for each source table.

<table id="table_ty4_pmz_clb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Table Name

</td><td>

Name of one of the tables on the producer instance to replicate. For example, SAN Disk \[cmdb\_ci\_san\_disk\].

</td></tr><tr><td>

Filter

</td><td>

Filter criteria to control the records in the table that the system is replicating. -   Use the filter to limit the number of records in your replication set. For example, if the table has an **Active** field, add a filter condition like **\[Active\] \[is\] \[True\]** to replicate only active records.
-   If you want to replicate and preserve a parent and child table hierarchy, add a filter for the sys\_class\_name column to each outbound entry. This ensures that all of the child table columns are replicated, and not just the parent the columns.

For example, to replicate both the Task \[task\] parent table and the Incident \[incident\] child table, you must add **\[Task type\] \[is\] \[Task\]** as a filter in the parent table entry and **\[Task type\] \[is\] \[Incident\]** as a filter in the child table entry. In this example, Task type is the label for the sys\_class\_name column on each table. For details, see [Preserving table hierarchy in Instance Data Replication](../concept/preserving-table-hierarchy.md).

</td></tr><tr><td>

Include Attachments

</td><td>

Option to replicate the files associated with the records that you are replicating.

</td></tr><tr><td>

Included Fields

</td><td>

Fields to include. Move table fields into the Selected column to replicate them or into the Available column to prevent replicating them.**Note:** The system must replicate some fields, such as **sys\_id \(Mandatory\)**. The system cannot replicate some fields, such as **Edge Encrypted** and **Password1**. They do not appear in either column.

</td></tr><tr><td>

Enable Custom Coalesce

</td><td>

Option to enable you to choose a field other than the default **sys\_id** field to coalesce IDR.

</td></tr><tr><td>

Coalesce Field

</td><td>

Choose a field to use to coalesce IDR. Only unique fields are available. See [Coalesce columns in Instance Data Replication](../concept/idr-coalesce.md).

 This field only displays if you select **Enable Custom Coalesce**.

</td></tr></tbody>
</table>5.  Select **Submit**.

    **Note:** If the table that you add to the replication set has child tables, add the child tables to the replication set to maintain data integrity.

6.  Repeat step 3 for each table that you want to include in the replication set.

    After you submit, the **Activate** button is added to the form.

7.  Select **Activate**.

    Replication can't happen until you link the producer replication set to one or more consumer replication sets. Activating the producer replication set makes the producer data available for replication to consumers.

8.  Select the **Notification Configuration** related link and choose a tab to configure notification details.

<table id="choicetable_drl_xtf_hlb"><tbody><tr><td id="d148783e488">

**When to send**

</td><td>

Specify the conditions for sending a notification.-   **Record inserted or updated**— You can send notifications when records are updated or inserted.
-   **Event is fired**—Specify the event type that sends the notification.
-   **Triggered**—A notification is sent when triggered by a ServiceNow® Workflow Studio flow. For more information, see [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).


</td></tr><tr><td id="d148783e526">

**Who will receive**

</td><td>

Send notifications to users, groups, or user groups in the fields on the ServiceNow record that generates the notification.

</td></tr><tr><td id="d148783e538">

**What it will contain**

</td><td>

You can choose an email template to populate the Subject and Message HTML. You can also override the template and customize the text as appropriate.

</td></tr><tr><td id="d148783e547">

**What Digest will contain**

</td><td>

If you select **Allow Digest**, you can configure an email digest interval through the Digest Interval module in System Notification.

</td></tr></tbody>
</table>9.  Select **Update**.

10. To see a preview of the notification, select **Preview Notification**.

11. To discard the Producer Replication Set, select **Delete**.


## Result

The producer is ready to send the data that is specified in the replication set to one or more consumer instances.

## What to do next

-   For information about creating and activating the consumer replication set, see [Create and activate a consumer replication set](create-c-replication-set.md).
-   For information about granting access to the replication data, see [Grant access to replication data](approve-consumer.md).

    After creating a consumer replication set, you must ask for permission to receive the producer replication data. See [Grant access to replication data](approve-consumer.md) to learn how to grant or deny access.

-   If you believe that a consumer set should no longer receive replication data, you can [revoke the consumer set access](revoke-consumer-sets.md).

**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a consumer replication set for Instance Data Replication](create-c-replication-set.md)

[Seed a consumer instance for Instance Data Replication](seed-consumer-instance.md)

[Trigger a workflow after replication using Instance Data Replication](post-replication-actions.md)

[Reconfigure a replication set in Instance Data Replication](change-replication-set-config.md)

[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Set up bidirectional replication in Instance Data Replication](bi-directional-replication.md)

[Create a discrete producer replication set for Instance Data Replication](discrete-producer-replication-set.md)

