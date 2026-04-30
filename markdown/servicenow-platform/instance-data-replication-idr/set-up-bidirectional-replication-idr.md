---
title: Set up bidirectional replication
description: Replicate updated data on a consumer instance to the producer instance using bidirectional replication in Instance Data Replication \(IDR\).
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Replicate data, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Set up bidirectional replication

Replicate updated data on a consumer instance to the producer instance using bidirectional replication in Instance Data Replication \(IDR\).

## Before you begin

Role required: admin

## About this task

Bidirectional replication enables you to replicate data on a consumer instance to the producer instance. For example, data, such as problem requests, can be copied to consumer instances for third parties to use. The third party can update the problem issue on the consumer instance. The data can then be updated on the producer instance.

Note that seeding options are not available in bi-directional sets by design.

## Procedure

1.  Create a producer replication set.

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select **New**.

    3.  Enter a name and description for the producer replication set.

        -   The name can only contain alphanumeric characters and hyphens.
        -   Avoid using a name that applies only to the producer instance. You must provide the same name in the consumer replication set, so the name shouldn't be producer-specific.
    4.  Enable changes to records that are made on the consumer instance to propagate to the producer instance by selecting **Bi-Directional**.

        **Note:** Bi-directional replication works for records that originate on the producer or consumer.

    5.  Enable discrete mapping from a producer replication set by selecting **Discrete**.

        Discrete mapping distinguishes different consumer instances. For details, see [Set up discrete replication](set-up-discrete-replication-idr.md).

    6.  Create the producer replication set from a list of outbound entries by selecting **Entry set**.

        If you imported an update set from another instance or you created one earlier on your instance, you can choose an existing entry set.

    7.  Select **Submit**.

        The producer replication set is created with an auto-generated producer ID that identifies the producer instance in the system.

2.  Specify the tables and columns on the producer instance that you want to replicate.

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

    5.  Select **Submit**.

3.  Make the producer data available for replication to consumers by selecting **Activate**.

    The producer is ready to send the data that is specified in the replication set to one or more consumer instances.

4.  Create a consumer replication set.

    1.  On a consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Producer Instance URL|URL of the producer instance. For example, https://&lt;producer\_instance&gt;.servicenow.com.|
        |Producer Replication Set Name|Name of the consumer replication set. The name on the consumer must match the name on the producer. Obtain the name from the producer administrator.|
        |Description|Description of the purpose of the replication.|

    4.  Select **Submit**.

        The system sends a request to the producer replication set administrator to approve or deny the request.

5.  Approve the consumer request.

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select the producer replication set where you want to approve consumer access.

    3.  Under Related Links, on the **Consumer Subscriptions** tab, select the option for the consumer replication set that you want to approve.

    4.  On the Actions on selected rows list, select **Approve**.

    The consumer set is approved and ready to receive replicated data.

6.  Activate the consumer replication set.

    1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

    2.  Select the consumer replication set that you want to activate.

    3.  Select **Activate**.

    After some time, the status changes to Active Replication.

7.  Update the Consumer Replication Entries configuration to match the configuration on the producer by selecting **Synchronize Replication Entries**.

    If you do not see this option, refresh the page.

8.  In the dialog box that appears, confirm the synchronization.


## Result

Data that is updated on this consumer instance automatically replicates on the producer instance, which then replicates the updates to its other consumer instances.

**Parent Topic:**[Replicating data with Instance Data Replication](../concept/replicating-data.md)

