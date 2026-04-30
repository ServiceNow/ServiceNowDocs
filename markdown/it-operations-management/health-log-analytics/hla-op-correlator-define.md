---
title: Add a log correlator to identify relationships in logs
description: Detect related alerts in log data by adding log correlators. The base system includes several log correlators and you can define custom log correlators.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using log correlators to detect relationships in log data, Using Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Add a log correlator to identify relationships in logs

Detect related alerts in log data by adding log correlators. The base system includes several log correlators and you can define custom log correlators.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

To learn more about the types and functions of log correlators, see [Using log correlators to detect relationships in log data](../concept/hla-op-correlator-what-is-a.md). For more information on log sources, see [Verify your log sources](../../health-log-analytics-admin/task/hla-log-sources-review.md).

## Procedure

1.  Use one of the following methods to add a log correlator.

<table id="choicetable_aks_4jj_dpb"><thead><tr><th align="left" id="d538594e104">

Option

</th><th align="left" id="d538594e107">

Procedure

</th></tr></thead><tbody><tr><td id="d538594e113">

**Add a log correlator for a specific log source**

</td><td>

1.  Navigate to **Health Log Analytics** &gt; **Log Anomaly Detection** &gt; **Log Correlators**. The list of existing log correlators opens.
2.  Click the name of a log correlator. The names appear in the **Correlation indicator** column.
3.  Click **New**.


</td></tr><tr><td id="d538594e158">

**Add a log correlator that applies either to all log sources or to only those log sources that become active after you define this log correlator**

</td><td>

1.  Navigate to **Health Log Analytics** &gt; **Data Input** &gt; **Log Sources**.
2.  Click the name of the log source.

The Log correlators related list displays the list of existing log correlators that analyze log data from the selected log source.

3.  On the **Log correlators** tab, click **New**.


</td></tr></tbody>
</table>2.  Fill in the Log correlator form.

<table id="table_rcp_spb_zmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of log correlator. Choices are as follows.-   **Free text correlator**: The log correlator analyzes text in the log message.
-   **Log-key correlator**: The log correlator analyzes log metadata. For example, the name of a service instance in your infrastructure. Log property correlators are specific to the business context of your environment.
 For more information, see [Using log correlators to detect relationships in log data](../concept/hla-op-correlator-what-is-a.md).

</td></tr><tr><td>

Free text term or Identifier

</td><td>

Text that the log correlator isolates when parsing log lines. The label for this field is **Free text term** for free text correlators and **Identifier** for log property correlators.

**Note:** The value of this field can be the text for either type of log correlator. As a result, the label for this column in the resulting list of log correlators is **Correlation indicator**.

</td></tr><tr><td>

Active

</td><td>

Option to apply the log correlator. When you select this field, the system applies the log correlator to the log stream.

</td></tr><tr><td>

Range of analysis

</td><td>

Set of sources whose log data are analyzed by this log correlator. Choices are as follows:-   **All sources**: The log correlator is applied to log lines from all sources in the data stream.
-   **Only new sources**: The log correlator is applied to log lines from all sources created after this log correlator is activated.
-   **Specified source**: The log correlator is applied only to the log lines from the source that you specify on this form.


</td></tr><tr><td>

Excluded sources

</td><td>

Sources that are excluded from the log correlator. The system does not analyze log lines from sources that are listed in this field.**Note:** This field applies only when the **Range of analysis** field is set **All sources** or **Only new sources**.

 For information about excluding a source from a log correlator, see [Exclude a source from a log correlator](../../health-log-analytics-admin/task/hla-correlators-exclude-source.md).

</td></tr><tr><td>

Source

</td><td>

Source of the log correlator. The log correlator analyzes the data of this log source.This field appears only when you are adding the log correlator from the Log Sources form. This field is automatically set to the log source that you are working on.

</td></tr></tbody>
</table>3.  Select **Active** and then click **Submit**.


**Parent Topic:**[Using log correlators to detect relationships in log data](../concept/hla-op-correlator-what-is-a.md)

