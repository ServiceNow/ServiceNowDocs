---
title: Find missing or mismatched records in Instance Data Replication
description: Find records missing from the consumer instance or mismatched records after data has been replicated by creating a data comparison request in Instance Data Replication \(IDR\).
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Comparing replicated data, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Find missing or mismatched records in Instance Data Replication

Find records missing from the consumer instance or mismatched records after data has been replicated by creating a data comparison request in Instance Data Replication \(IDR\).

## Before you begin

Make sure the following conditions are met:

-   The producer replication set is active.
-   Seeding isn't in progress.
-   No other data comparison requests are running.

Role required: admin

## About this task

Note the following:

-   Data comparison requests are purged after three months.
-   There are limitations when comparing transformed data. See [Comparing replicated data between instances in Instance Data Replication](../concept/comparing-replicated-data.md).

## Procedure

1.  On the producer instance, navigate to **All** &gt; **Instance Data Replication** &gt; **Producer Replication Sets**.

2.  Select an active producer replication set with replicated data that you want to compare.

3.  Create a data comparison request.

    1.  Navigate to the IDR Data Comparison Requests related list.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_ipd_2mq_1xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Replication Set

</td><td>

Name of the producer replication set.

</td></tr><tr><td>

Target Instance Name

</td><td>

Name of the consumer instance.

</td></tr><tr><td>

Target Instance URL

</td><td>

URL of the consumer instance.

</td></tr><tr><td>

Table Name

</td><td>

Name of the table in the outbound entry of the producer replication set.

</td></tr><tr><td>

Start Date

</td><td>

Start date and time for comparing data. Records with a sys\_updated\_on value after the date you select are included in the comparison.

</td></tr><tr><td>

End Date

</td><td>

End date and time for comparing data. Records with a sys\_updated\_on value before the date you select are included in the comparison.

</td></tr><tr><td>

Auto Seed

</td><td>

Option to automatically seed any missing or mismatched records from the producer instance to the consumer instance.You can optionally reseed missing or mismatched records at a later time. See [Reseed missing or mismatched records in Instance Data Replication](fix-replicated-data.md).

</td></tr></tbody>
</table>    4.  Select **Submit**.

4.  View a summary of the data comparison in the IDR Data Comparison Results form.

    -   Determine the percentage of missing or mismatched by viewing the pie chart.
    -   View the total number of missing and mismatched records in the **Mismatched Records Count** field.
5.  Identify records that are missing from the consumer instance after seeding through the pie chart or list.

    -   View the missing records by selecting the missing records portion of the pie chart.
    -   View records that have a **Missing** value in the **Record Type** column in the IDR Instance Comparison Results related list.
    **Tip:** Save copies of the missing record IDs in case you need to provide them to Customer Service and Support.

6.  View the differences between mismatched records after data replication.

    1.  Navigate to the IDR Instance Comparison Results related list.

    2.  Select the check box next to any record with a **Mismatched** value in the **Record Type** column.

    3.  Select the **Actions on selected rows** list.

    4.  Select **Compare records**.

    5.  View the highlighted differences between the records in the **Compare Record Payloads** dialog box.

        **Note:** Journal fields are excluded from the comparison due to the potential size of their content.

        Save a copy of the payload difference in case you need to provide it to Customer Service and Support.


## What to do next

[Reseed missing or mismatched records in Instance Data Replication](fix-replicated-data.md).

**Parent Topic:**[Comparing replicated data between instances in Instance Data Replication](../concept/comparing-replicated-data.md)

