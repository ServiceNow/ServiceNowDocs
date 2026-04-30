---
title: Update a manually created metric
description: Update a manually created manual metric to add goals, metric data, and targets. Associate citations to the metric.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Update a manually created metric

Update a manually created manual metric to add goals, metric data, and targets. Associate citations to the metric.

## Before you begin

Role required: sn\_grc.metric\_manager, sn\_risk.user and sn\_compliance.user

## About this task

You can use the same form for updating the automated metric definition, manual metric definition, and composite metric definition.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Metrics**.

2.  Select a metric definition from the list.

3.  On the form, update the fields as necessary.

<table id="table_l2g_jzy_vqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Tabs

</td></tr><tr><td>

Name

</td><td>

Name for the metric. For example, `Number of incidents- ACME Asia`.

</td></tr><tr><td>

Description

</td><td>

Brief description of the metric.

</td></tr><tr><td>

Metric definition

</td><td>

Metric definition associated with the metric.

</td></tr><tr><td>

Entity

</td><td>

Entity associated with the metric.

</td></tr><tr><td>

Enterprise Owner Type

</td><td>

Enterprise owner type who is responsible for the metric. This field is automatically set to display the enterprise owner type.

</td></tr><tr><td>

Type

</td><td>

Type of metric definition. This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Option to mark the metric definition as active. This field is automatically set.

</td></tr><tr><td>

Key metric

</td><td>

Option to mark the metric definition as a key metric. This field is automatically set.

</td></tr><tr><td>

Enterprise owner

</td><td>

Enterprise owner of the metric definition. This field is automatically set.

</td></tr><tr><td class="sub-head" colspan="2">

Metric Properties

</td></tr><tr><td>

Direction

</td><td>

Direction of the metric definition. This field is automatically set.

</td></tr><tr><td>

Precision

</td><td>

Precision for the metric definition. This field is automatically set.

</td></tr><tr><td>

Unit

</td><td>

Unit for the metric definition. This field is automatically set.

</td></tr><tr><td>

Nature

</td><td>

Nature of the metric definition. This field is automatically set.

</td></tr><tr><td class="sub-head" colspan="2">

Method

</td></tr><tr><td>

Instructions

</td><td>

Instructions for the data owner. Method of collection for the manual metric definition. This field is automatically set.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Calendar

</td><td>

Calendar to use for metric aggregation. Only the configured calendar options are available for selection. This field is automatically set to **Standard Calendar**. **Note:** Standard calendar refers to the Gregorian calendar.

</td></tr><tr><td>

Frequency

</td><td>

Collection frequency with which the metric is executed. Indicates how often the metric definition should collect the data. The choices are as follows:-   **Daily**
-   **Weekly**
-   **Monthly**
-   **Quarterly**
-   **Semi-annually**
-   **Annually**
This field is automatically set.

</td></tr><tr><td>

First run date

</td><td>

Date for the first run time. This field is automatically set.

</td></tr><tr><td>

Next run date

</td><td>

Date for the next run time.

</td></tr><tr><td>

Period date

</td><td>

Date used to specify the start and end dates for the data collection period.

</td></tr><tr><td>

Due date offset

</td><td>

Number of days after the schedule end date when the metric data task becomes overdue. For example, if the frequency of a metric definition is monthly and if you enter `15` in this field, then the due date for metric data task will be overdue 15 days after the month ends. This field is automatically set.

</td></tr><tr><td class="sub-head" colspan="2">

Data Collection Details

</td></tr><tr><td>

Data owner type

</td><td>

Data owner type such as User.

</td></tr><tr><td>

Data owner

</td><td>

Name of the user as the data owner.

</td></tr><tr><td class="sub-head" colspan="2">

Approval

</td></tr><tr><td>

Approval required

</td><td>

Option to be enabled if an approval is requested for the metric.

</td></tr><tr><td>

Metric data tasks tab

</td><td>

Information about the metric data task, such as name, number, assigned to, priority, and state

</td></tr><tr><td class="sub-head" colspan="2">

Classification

</td></tr><tr><td>

Group

</td><td>

Area that the metric relates to. This field is automatically set.

</td></tr><tr><td>

Subgroup

</td><td>

Tag used to categorise the metric. This field is automatically set.

</td></tr><tr><td>

Reporting classification

</td><td>

Tag under which the metric definition and metric is categorized. For example, **GRI**, **SASB**, or **Steering Committee Review**.

</td></tr><tr><td class="sub-head" colspan="2">

Related lists

</td></tr><tr><td>

Goals

</td><td>

Details of the goals associated with the metric, such as name, state, category, start date, end date, owner, and status. To add a new goal, select **Add**.

</td></tr><tr><td>

Metric data

</td><td>

Details of the metric data such as start date, end date, value, collector metric data, collection frequency, and type.

 Start date: The start date is the date that the data collection begins.

 End date: The end date is the end of the period date that determines the interval for which the score is calculated. The end date depends on the frequency of the metric definition. The end date is used for tracking the scores. Every score is time-dependent and it has a reference to the interval end date.

 Collection frequency: The options in the collection frequency field are:

-   **Daily**: Score that gets created for each day.
-   **Weekly**: Score that gets created by the end of the week date \(Sunday\). Monday is the start of the week and Sunday is the end of the week.
-   **Monthly**: Score that gets created by the end of the month.
-   **Quarterly**: Score that gets created by the end of the quarter. For example, Q1 ends on March 31, Q2 ends on June 30, Q3 ends on September 30, and Q4 ends on December 31 in a year.
-   **Semi-annually**: Score that is created by the end of the 6-month period. The end date for the semester is June 30 and December 31 in a year.
-   **Annually**: Score that gets created by the end of the year. The end date for the year is December 31.


</td></tr><tr><td>

Targets

</td><td>

Details of the targets associated with the metric, such as name, state, owner, start date, end date, type, and measure. To add a new target, select **Add**.

</td></tr><tr><td>

Citations

</td><td>

Details of the citations, such as reference, name, authority document, description, and compliance score percentage \(%\). To add a new citation, select **Add**.

</td></tr><tr><td>

Thresholds

</td><td>

Details of the thresholds associated with the metric, such as type, related metric, valid dates, threshold color, and target value. To add a new citation, select **Add**.

</td></tr></tbody>
</table>4.  To save the metric, select **Save**.

5.  To delete the metric definition, select **Delete**.

6.  To execute the metric, select **Execute**.

    A metric data score is created if it doesn’t exist for the current interval. Re-executing a metric or a metric definition for the current interval only updates the score.

7.  To visually explore the 360° relationship view of the metric definition, select **360° view**.


**Parent Topic:**[Configuring metrics](../concept/configuring-irm-metrics.md)

