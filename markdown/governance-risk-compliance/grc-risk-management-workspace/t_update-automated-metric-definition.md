---
title: Update a metric definition
description: Update an existing metric definition to collect the new metrics. You can associate new goals, targets, and entities with the metric definition.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Update a metric definition

Update an existing metric definition to collect the new metrics. You can associate new goals, targets, and entities with the metric definition.

## Before you begin

Role required: sn\_grc.metric\_manager, sn\_risk.user and sn\_compliance.user

## About this task

You can use the same form for updating the automated metric definition, manual metric definition, and composite metric definition.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Metrics**.

2.  Select a metric definition from the list.

3.  On the form, update the fields as necessary.

<table id="table_trw_s3v_kwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Tabs and related lists

</td></tr><tr><td>

Details tab

</td><td>

Details of the metric, such as metric definition, metric properties, method, and schedule in the automated metric definition.

 Details of the metric, such as collection method, schedule, data collection details, approval in the manual metric definition.

 Details of the metric, metric properties, and roll up properties in the calculated metric definition. The fields on the Details tab are explained in the Metric definition forms.

</td></tr><tr><td>

Entity type

</td><td>

Details of the entity type to be associated with the metric. For example, provides the name, description, and conditions, such as active, need update, and processing entities. To add a new entity type, click **Add**.**Note:** The Entity type related list is displayed only for an automated metric definition and a manual metric definition. It isn’t displayed for the calculated metric definition.

</td></tr><tr><td>

Additional entities

</td><td>

Additional entities that can be associated with the metric definition. Provides details, such as name, owned by, class, and compliance score in percentage \(%\). To add new entities, click **Add**.**Note:** This related list is displayed only for an automated metric definition and a manual metric definition. It isn’t displayed for the calculated metric definition.

</td></tr><tr><td>

Child Metric Definition

</td><td>

Child metric definition associated with the parent metric definition. Displays the details such as name, frequency, and description of the child metric definition. To add a new child metric definition, click **Add**.**Note:** This related list is displayed only for the calculated metric definition. It isn’t displayed for the automated metric definition and the manual metric definition.

</td></tr><tr><td>

Metrics

</td><td>

Details of the metrics, such as name, associated entity, and active state of the metric. To add a new metric, click **New**.

</td></tr><tr><td>

Citations

</td><td>

Details of the citations such as reference, name, authority document, description, and compliance score in percentage \(%\). To add a new citation, click **Add**.

</td></tr><tr><td>

Goals

</td><td>

Details of the goals, such as name, state, category, start date, end date, owner, and status. To add a new goal, click **Add**.

</td></tr><tr><td>

Targets

</td><td>

Details of the target, such as name, owner, state, status, progress, actual value, target value, and end date. To add a new target, click **Add**.

</td></tr><tr><td>

Metric definition data

</td><td>

Details of the metric definition data, such as collection frequency, collection definition, interval end date, value, and state. **Note:** This related list is displayed only for an automated metric definition and a manual metric definition. It isn’t displayed for the calculated metric definition.

</td></tr><tr><td>

Calculated metric data

</td><td>

Details of the calculated metric data, such as interval end date, roll up frequency, and value. **Note:** This related list is displayed only for the calculated metric definition. It isn’t displayed for the automated metric definition and the manual metric definition.

</td></tr></tbody>
</table>4.  To save the metric definition, click **Save**.

5.  To calculate the composite metric data for the composite metric definition, click **Aggregate**.

    The **Aggregate** action calculates the composite metric data for the current interval end date and roll-up frequency to its parent metric definition. The composite metric data record is displayed under the Composite metric data related list. A composite metric definition score is created if it doesn’t exist for the current interval.

6.  To delete the metric definition, click **Delete**.

7.  To visually explore the 360° relationship view of the metric definition, click **360° view**.


