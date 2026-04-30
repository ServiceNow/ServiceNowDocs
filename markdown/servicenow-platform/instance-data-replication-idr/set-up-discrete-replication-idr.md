---
title: Set up discrete replication
description: Replicate data from a producer instance to specific, distinguished consumer instances in near-real time, ensuring each consumer instance receives updates independently in Instance Data Replication \(IDR\).
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Replicate data, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Set up discrete replication

Replicate data from a producer instance to specific, distinguished consumer instances in near-real time, ensuring each consumer instance receives updates independently in Instance Data Replication \(IDR\).

## Before you begin

Plan your data replication strategy by reviewing the important considerations described in [Preparing for Instance Data Replication](../concept/prepare-instance-data-replication.md).

Role required: idr\_admin or admin

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

2.  Select **New**.

3.  Enter a name and description for the producer replication set.

    -   The name can only contain alphanumeric characters and hyphens.
    -   Avoid using a name that applies only to the producer instance. You must provide the same name in the consumer replication set, so the name shouldn't be producer-specific.
4.  Distinguish replication for different consumer instances by selecting **Discrete**.

5.  Create the producer replication set from a list of outbound entries by selecting **Entry set**.

    If you imported an update set from another instance or you created one earlier on your instance, you can choose an existing entry set.

6.  Select **Submit**.

    The producer replication set is created with an auto-generated producer ID that identifies the producer instance in the system.

7.  Specify the tables and columns on the producer instance that you want to replicate.

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

Discrete Field

</td><td>

Choose a reference field that defines the mapping for each consumer subscription. For example, if you choose the **Assigned To** field in the Incident source table, you can distinguish user assignments for specific consumers.

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

        **Note:** If a table that you select has child tables, repeat these steps and add outbound entries for each child table to maintain data integrity.

8.  Map discrete values for each consumer instance.

    1.  Select the **Discrete Mappings** tab.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Discrete Value|This field sets a rule for what displays for the selected consumer instance within the producer replication set. For example, an **Assigned To** discrete value gives choices from a designated table of a specific user to show assignments.|
        |Outbound Replication Entry|Select an outbound replication entry that you configured with a source table for this producer replication set.|
        |Replication Subscription|Choose the consumer instance that displays the discrete value assignment.|

        **Note:** For each consumer that subscribes to a producer replication set with discrete mapping enabled, you must configure a discrete value.

    4.  Repeat these steps for each consumer that you want to subscribe to the producer replication set.

9.  Select **Submit**.

10. Make the producer data available for replication to consumers by selecting **Activate**.

    The producer is ready to send the data that is specified in the replication set to one or more consumer instances.

11. On a consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

12. Select **New**.

13. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Producer Instance URL|URL of the producer instance. For example, https://&lt;producer\_instance&gt;.servicenow.com.|
    |Producer Replication Set Name|Name of the consumer replication set. The name on the consumer must match the name on the producer. Obtain the name from the producer administrator.|
    |Description|Description of the purpose of the replication.|

14. Select **Submit**.

    The list of all consumer replication sets on the consumer instance appears. The system sends a request to the producer replication set administrator to approve or deny the request.

15. Approve the consumer request.

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select the producer replication set where you want to approve consumer access.

    3.  Under Related Links, on the **Consumer Subscriptions** tab, select the option for the consumer replication set that you want to approve.

    4.  On the Actions on selected rows list, select **Approve**.

    5.  Repeat these steps for each consumer instance.

16. Activate the consumer replication set.

    1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

    2.  Select the consumer replication set that you want to activate.

    3.  Select **Activate**.

    4.  Repeat these steps for each consumer instance.

    After some time, the status changes to Active Replication, and the **Partial Seeding** and **Full Seeding** buttons are displayed.


**Parent Topic:**[Replicating data with Instance Data Replication](../concept/replicating-data.md)

