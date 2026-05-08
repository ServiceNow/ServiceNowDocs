---
title: Transform replication data
description: Transform producer instance data for tables or table columns that are named differently on consumer instances in Instance Data Replication \(IDR\).
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Replicate data, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Transform replication data

Transform producer instance data for tables or table columns that are named differently on consumer instances in Instance Data Replication \(IDR\).

## Before you begin

-   Create and activate a producer replication set.
-   Create, activate, and seed one or more consumer replication sets.
-   Role required: idr\_admin or admin

## About this task

The replicated data from producer tables and table columns goes into tables and table columns of the same name on consumer instances. You can map the producer data into any table or table column on consumer instances. If existing tables or table columns have different names, you can replicate the data to a different table or table column. Adapters modify the data before storing it on consumer instances. For example, adapters can localize data from the producer instance before it is consumed by the consumer instance.

You can also use adapters to modify the producer data during replication. For example, you can localize the data or populate the data that has been labeled differently in consumer tables.

Transformations have the following limitations:

-   sys\_created, sys\_created\_by, sys\_domain, sys\_updated\_by, sys\_id, sys\_mod\_count, and other systems are automatically mapped to the consumer and can't be remapped.

    No other sys\_ fields can be replicated.

-   Adapters can't operate on the sys\_journal field type such as Comments or Worknotes columns in a Task table.
-   Calculated fields won't be transformed.

    A calculated field, such as the name field from sys\_user, will replicate but cannot be transformed. Allowing a transformation breaks the calculation for the resulting field.

    **Note:** Calculated fields will not show as an option to transform.


## Procedure

1.  Choose a producer or consumer instance and navigate to the replication set.

<table id="choicetable_lbg_kqq_snb"><tbody><tr><td id="d559800e107">

**Consumer Instance**

</td><td>

Navigate to **Instance Data Replication** &gt; **Consumer Replication Sets** and click a consumer replication set.

</td></tr><tr><td id="d559800e125">

**Producer instance**

</td><td>

Navigate to **Instance Data Replication** &gt; **Producer Replication Sets** and click a producer replication set.

</td></tr></tbody>
</table>2.  Choose an inbound or outbound entry.

<table id="choicetable_oh1_45q_snb"><tbody><tr><td id="d559800e152">

**Consumer Instance**

</td><td>

On the **Inbound Entries** tab, click an inbound entry.

</td></tr><tr><td id="d559800e164">

**Producer instance**

</td><td>

On the **Outbound Entries** tab, click an outbound entry.

</td></tr></tbody>
</table>    An entry appears.

    ![Enable transforms](../image/enable-transform.png)

3.  Select the **Enable Transform** option.

4.  In the Target Table Name list, select the table into which you want to replicate the source table data and click **Update**.

5.  On the **Inbound Entries** or the **Outbound Entries** tab, click the same entry.

6.  Click the lock icon next to **Transform Map** to unlock it.

    The image shows a Transform Map, with the field names from the source table appearing in the left column. The middle column shows matching field names in the target table. All fields that do not have the same names in both tables appear in the – choose source field – or – choose target field – lists.

    ![Transform different fields](../image/transform-diff-fields.png)

    **Note:** If a table in a producer replication set is not on a consumer instance, the consumer instance will fill the first column with the producer schema definition sent during synchronization.

7.  Map a producer column to a consumer column that has a different name:

    1.  Click **– choose source field –** and select the source field that you want to map.

    2.  Click **– choose target field –**, select the target field into which you want to map the data, and then click **Add**.

    3.  If you want to remove a field from replicating the producer instance to the consumer instance, click the **X** at the end of the row to delete the field.

8.  To modify the producer data before replicating it in the consumer instance, click **Add Adapter**.

    The image shows the type of Adapter rules that you can create.

    ![Adapters](../image/adapter-choices.png)

9.  Click the adapter that you want to use and then configure it.

    For more information about configuring adapters, see [Adapter descriptions](../reference/adapter-descriptions.md).

    **Note:** Adapters do not modify the data on the producer instance.


-   **[Warning and error messages in Instance Data Replication](../reference/schema-warnings-error.md)**  
Understand error and warning messages related to schema definitions. You can then troubleshoot or fix Instance Data Replication \(IDR\) replication issues.

**Parent Topic:**[Replicating data with Instance Data Replication](../concept/replicating-data.md)

