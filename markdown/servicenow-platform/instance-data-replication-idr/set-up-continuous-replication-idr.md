---
title: Set up continuous replication
description: Enable near-real time data replication from a producer instance to one or more consumer instances in Instance Data Replication \(IDR\).
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Replicate data, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Set up continuous replication

Enable near-real time data replication from a producer instance to one or more consumer instances in Instance Data Replication \(IDR\).

## Before you begin

Verify that the producer and consumer instances belong to the same customer.

Plan your data replication strategy by reviewing the important considerations described in [Preparing for Instance Data Replication](../concept/prepare-instance-data-replication.md).

Role required: idr\_admin or admin

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

2.  Select **New**.

3.  Enter a name and description for the producer replication set.

    -   The name can only contain alphanumeric characters and hyphens.
    -   Avoid using a name that applies only to the producer instance. You must provide the same name in the consumer replication set, so the name shouldn't be producer-specific.
4.  Create the producer replication set from a list of outbound entries by selecting **Entry set**.

    If you imported an update set from another instance or you created one earlier on your instance, you can choose an existing entry set.

5.  Select **Submit**.

    The producer replication set is created with an auto-generated producer ID that identifies the producer instance in the system.

    ![Producer replication set.](../image/producer-replication-set.png)

6.  Specify the tables and columns on the producer instance that you want to replicate.

    1.  Select the Outbound Entries related list.

    2.  Select **New**.

    3.  On the form, fill in the fields.

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

Choose a field to use to coalesce IDR. Only unique fields are available. See [Custom coalescing](../concept/modifying-replication-behavior-idr.md#).

 This field only displays if you select **Enable Custom Coalesce**.

</td></tr></tbody>
</table>    4.  Repeat these steps for each table that you want to include in the replication set.

        **Note:** If a table that you select has child tables, repeat these step and add outbound entries for each child table to maintain data integrity.

7.  Select **Submit**.

8.  Make the producer data available for replication to consumers by selecting **Activate**.

    The producer is ready to send the data that is specified in the replication set to one or more consumer instances.

9.  On a consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

10. Select **New**.

11. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Producer Instance URL|URL of the producer instance. For example, https://&lt;producer\_instance&gt;.servicenow.com.|
    |Producer Replication Set Name|Name of the consumer replication set. The name on the consumer must match the name on the producer. Obtain the name from the producer administrator.|
    |Description|Description of the purpose of the replication.|

12. Select **Submit**.

    The list of all consumer replication sets on the consumer instance appears. The system sends a request to the producer replication set administrator to approve or deny the request.

13. Approve the consumer request.

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select the producer replication set where you want to approve consumer access.

    3.  Under Related Links, on the **Consumer Subscriptions** tab, select the option for the consumer replication set that you want to approve.

    4.  On the Actions on selected rows list, select **Approve**.

        The approved consumer set starts receiving replicated data.

14. Activate the consumer replication set.

    1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

    2.  Select the consumer replication set that you want to activate.

    3.  Select **Activate**.

    After some time, the status changes to Active Replication, and the **Partial Seeding** and **Full Seeding** buttons are displayed.


## Result

Data in the producer tables is replicated into tables and table columns of the same name on the consumer instances.

## What to do next

-   [Seed a consumer instance](seed-consumer-instance.md)
-   [Transform replication data](modify-replicated-data.md)
-   [Trigger a workflow after replication](../concept/modifying-replication-behavior-idr.md#)

**Parent Topic:**[Replicating data with Instance Data Replication](../concept/replicating-data.md)

