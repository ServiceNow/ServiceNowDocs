---
title: Provide data for a metric data task
description: Use the metric data task to provide data for a manual metric.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Provide data for a metric data task

Use the metric data task to provide data for a manual metric.

## Before you begin

Role required: sn\_grc\_metric.user, sn\_risk.reader, and sn\_compliance.reader

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

2.  Select the list ![](../../grc-workspace-risk/image/list-icon-risk-workspace.png) icon.

3.  Navigate to **Metrics** &gt; **Metrics**.

4.  Open the metrics and select the Metric data tasks tab.

5.  Open the task for which you want to provide the data.

6.  Select **Move to In Progress**.

7.  On the Metric information form, under the Metric input section, fill in the fields.

<table id="table_ln3_y5g_3rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric data

</td><td>

Value for the metric. This field appears only when **Quantitative** is selected in the **Category** field in the metric form.

</td></tr><tr><td>

Unit

</td><td>

Unit of the data. For example, US dollar.**Note:** You can provide the data in any unit and it gets converted to the reporting unit specified in the metric definition.

</td></tr><tr><td>

Override metric data

</td><td>

Option to manually override the system calculated metric value. When selected, you can enter a different value for the metric.

</td></tr><tr><td>

Variance \(%\)

</td><td>

Percentage difference between the system-calculated metric value and the overridden value. This field is populated only when metric data is overridden.

</td></tr><tr><td>

I acknowledge that I have reviewed the response and evidence attached, if any

</td><td>

Option to confirm that you have reviewed the metric data and any supporting evidence before completing the task.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Add notes or explanations related to the metric data task. These comments are visible to the customer and can be used to provide context or justification.

</td></tr></tbody>
</table>8.  Select **Save**.

9.  To provide evidence or supporting information, select Related Documents tab, and select **New**.

10. On the Related Document form, and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the related document. This name helps identify the document when reviewing or auditing the metric data task.|
    |URL|Supporting link to the external document or evidence that supports the metric data.|
    |Metric data task|This field is automatically set to the name of the metric data task for which you are providing information.|

11. Select **Save**.

12. Select **Submit**.


**Parent Topic:**[Using GRC: Metrics to provide data](../concept/using-metrics-irm.md)

