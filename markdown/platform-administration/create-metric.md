---
title: Define a metric
description: Create a metric definition for a task table.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Metrics, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a metric

Create a metric definition for a task table.

## Before you begin

Role required: metric\_admin

## Procedure

1.  Navigate to **All** &gt; **Metrics** &gt; **Definitions**.

    **Important:** Don’t confuse these metric definitions with the metric definitions for the Assessments feature. The Assessments feature is concerned with questionnaires. It isn’t related to the Metrics feature.

2.  Select **New**.

3.  Complete the Metric definition form then select **Submit**.

    **Note:** In the base system, metrics are configured to work on the task table only. To apply metrics to cmdb\_ci tables, duplicate the metric events business rule that currently runs on the task table for the cmdb\_ci table. Without the events created, no metric processing can occur.

<table id="table_enc_bvd_zq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The system generates a unique record number for the metric definition.

</td></tr><tr><td>

Name

</td><td>

Enter a unique name to describe what metrics are collected.

</td></tr><tr><td>

Table

</td><td>

Select the table that you want to collect metrics for. A metric can only apply to one table.

 **Note:** The list shows only tables and database views that are in the same scope as the metric definition

</td></tr><tr><td>

Field

</td><td>

Select the table column that you want to monitor for changes. Metrics only work on audited fields. Creating a metric for a non-audited field produces unreliable metrics.**Note:** Fields starting with 'sys\_' don’t work for a metric definition, except for 'sys\_domain'.

</td></tr><tr><td>

Type

</td><td>

Select what values this metric generates.-   **Field value duration**: This type of metric measures the duration of time from when the value of the specified field is set until it’s changed. A Field value duration metric can optionally specify a script. The script can either return a duration value or set the answer variable to false to stop processing the metric. For example, the baseline incident metrics stop calculating duration when the Active field of an incident is set to false. The script can also carry out any other action such as closing the duration of other metrics defined on the same record. For more information, see [Sample field value duration script](../concept/c_SampleFieldValueDurationScript.md).
-   **Script calculation**: This type of metric creates a metric instance using a script. The script has access to the current row in the table \(for example an incident\) and the metric definition. The script must perform metric calculations and insert data into the metric\_instance table. The calculation doesn’t have to result in a duration. It can calculate any type of value and store it in the metric instance value.


</td></tr><tr><td>

Timeline

</td><td>

Check this box to display the metric on a timeline page. For more information, see [Timeline pages](../../../administer/time/concept/c_TimelinePages.md).

</td></tr><tr><td>

Active

</td><td>

Check this box to monitor changes for this metric.

</td></tr><tr><td>

Description

</td><td>

Specify what data the metric monitors and its conditions. A good description helps other metrics administrators understand the purpose of your metric.

</td></tr><tr><td>

Script

</td><td>

Enter the script that you want the metric to run to either calculate a duration or perform some calculation on the metric\_instance table.

</td></tr></tbody>
</table>
