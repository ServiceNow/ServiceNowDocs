---
title: Add a log correlator to identify relationships between alerts in log data
description: Detect related alerts in log data by adding log correlators. The base system includes several log correlators and you can define custom log correlators.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Find correlations between alerts, Analyzing and resolving alerts, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Add a log correlator to identify relationships between alerts in log data

Detect related alerts in log data by adding log correlators. The base system includes several log correlators and you can define custom log correlators.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

For information about the types and functions of log correlators, see [Identifying related alerts in log data by using log correlators](../concept/hla-op-correlator-what-is-a.md).

## Procedure

1.  Use one of the following methods to add a log correlator.

<table id="choicetable_aks_4jj_dpb"><thead><tr><th align="left" id="d318269e72">

Option

</th><th align="left" id="d318269e75">

Procedure

</th></tr></thead><tbody><tr><td id="d318269e81">

**Add a log correlator for a specific log source**

</td><td>

1.  Navigate to **Health Log Analytics** &gt; **Log Anomaly Detection** &gt; **Log Correlators**. The list of existing log correlators opens.
2.  Click the name of a log correlator. The names appear in the **Correlation indicator** column.
3.  Click **New**.


</td></tr><tr><td id="d318269e120">

**Add a log correlator that applies either to all log sources or to only those log sources that become active after you define this log correlator**

</td><td>

1.  Navigate to **Health Log Analytics** &gt; **Data Input** &gt; **Log Sources**.
2.  Click the name of the log source.

The Log correlators related list displays the list of existing log correlators that analyze log data from the selected log source.

3.  On the **Log correlators** tab, click **New**.


</td></tr></tbody>
</table>2.  Fill in the Log correlator form.

    For a description of the fields, see [Log correlators form fields](../reference/hla-log-correlators-form-ref.md).

3.  Select **Active** and then click **Submit**.


**Parent Topic:**[Identifying related alerts in log data by using log correlators](../concept/hla-op-correlator-what-is-a.md)

