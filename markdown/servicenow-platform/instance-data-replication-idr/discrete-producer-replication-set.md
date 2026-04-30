---
title: Create a discrete producer replication set for Instance Data Replication
description: Distinguish consumers for a producer replication set in Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a discrete producer replication set for Instance Data Replication

Distinguish consumers for a producer replication set in Instance Data Replication \(IDR\).

## Before you begin

Role required: admin

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**:

    -   Click **New** for a new replication set
    -   Click on a producer replication set.
2.  Check **Discrete** to enable discrete mappings for your producer replication set.

    Once you enable discrete mapping, each outbound entry for a replication set has a discrete value column. You can define the mapping of each consumer subscription by setting a discrete value.

3.  Navigate to **Outbound Entries** tab and click **New**.

<table id="table_ty4_pmz_clb"><thead><tr><th>

Options

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Table Name

</td><td>

Select one of the tables on the producer instance to replicate. For example, .NET Application \[cmdb\_ci\_dot\_net\]

</td></tr><tr><td>

Discrete Field

</td><td>

Choose a reference field that defines the mapping for each consumer subscription. For example, if you choose the **Assigned To** field in the Incident source table, you can distinguish user assignments for specific consumers.

</td></tr><tr><td>

\[Optional\] Filter

</td><td>

Within the **Filter** section, you can use the **Add Filter Condition** to select filter criteria to control the records in the table that are being replicated. For example, you might want to replicate only active records. In that case, select **Active** in the **– choose field –** list, **Is** in the **– oper –** list, and **True** in the **– value –** list. If you do not use a filter, all the fields in the producer replication set table appear in the Available column.

**Note:** The Available column contains the fields in the Source Table that you specified. That table may not contain the **Active** field.

</td></tr><tr><td>

\[Optional\] Include Attachments

</td><td>

Select this option to replicate files that are associated with the records that are being replicated.

</td></tr><tr><td>

\[Optional\] Included Fields

</td><td>

In the Included Fields columns, use the arrows to move table fields into the Selected column to replicate them or into the Available column to prevent replicating them.**Note:** Some fields, such as **SYS ID \(Mandatory\)**, must be replicated. Other fields, such as **Edge Encrypted** and **Password1**, can't be replicated and do not appear in either column.

</td></tr></tbody>
</table>4.  Navigate to **Discrete Mappings** tab, click **New**, and fill in the form fields.

    |Field|Description|
    |-----|-----------|
    |Discrete Value|This field sets a rule for what displays for the selected consumer instance within the producer replication set. For example, an **Assigned To** discrete value gives choices from a designated table of a specific user to show assignments.|
    |Outbound Replication Entry|Select an outbound replication entry that you configured with a source table for this producer replication set.|
    |Replication Subscription|Choose the consumer instance that displays the discrete value assignment.|

    **Note:** For each consumer that subscribes to a producer replication set with discrete mapping enabled, they must have a discrete value set.


**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a producer replication set in Instance Data Replication](create-p-replication-set.md)

[Create a consumer replication set for Instance Data Replication](create-c-replication-set.md)

[Seed a consumer instance for Instance Data Replication](seed-consumer-instance.md)

[Trigger a workflow after replication using Instance Data Replication](post-replication-actions.md)

[Reconfigure a replication set in Instance Data Replication](change-replication-set-config.md)

[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Set up bidirectional replication in Instance Data Replication](bi-directional-replication.md)

