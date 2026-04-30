---
title: Update a metric definition
description: Update an existing metric definition to collect the new metrics. You can associate new goals, targets, and entities with the metric definition.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Update a metric definition

Update an existing metric definition to collect the new metrics. You can associate new goals, targets, and entities with the metric definition.

## Before you begin

Role required: sn\_esg.metric\_manager

## About this task

You can use the same form for updating the automated metric definition, manual metric definition, and calculated metric definition.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Metrics**.

2.  Select a metric definition from the list.

3.  To update the metric definition Name field, do the following:

    1.  Select the ![](../../../reuse/icons/product-icons/pencil-page-outline-24.svg) edit icon on the **Name** field.

    2.  Update the metric definition name.

    3.  Select **Apply name changes to selected metrics**.

    4.  Select the associated metrics where you want the name change should apply.

    5.  Select **Update**.

    **Note:** After creating a metric, its name is read only but can be edited via a pop-up modal. When updated, you can choose which associated child metrics to apply the change to, and their related tasks are updated automatically.

4.  On the form, update the fields as necessary.

<table id="table_l2g_jzy_vqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Tabs and related lists

</td></tr><tr><td>

Details tab

</td><td>

Details of the metric, such as metric definition name, metric properties, method, and schedule in the automated metric definition.

 Details of the metric, such as collection method, schedule, data collection details, are approved in the manual metric definition.

 Details of the metric, metric properties, and roll up properties in the calculated metric definition. The fields on the Details tab are explained in the Metric definition forms.

</td></tr><tr><td>

Entity type

</td><td>

Details of the entity type to be associated with the metric. For example, provides the name, description, and conditions, such as active, need update, and processing entities. To add a new entity type, select **Add**.**Note:** The Entity type related list is displayed only for an automated metric definition and a manual metric definition. It isn’t displayed for the calculated metric definition.

</td></tr><tr><td>

Entities

</td><td>

Entities that can be associated with the metric definition. Provides details, such as name, owned by, class, and compliance score in percentage \(%\). To add new entities, select **Add**.**Note:** This related list is displayed only for an automated metric definition and a manual metric definition. It isn’t displayed for the calculated metric definition.

</td></tr><tr><td>

Metrics

</td><td>

Details of the metrics, such as name, associated entity, and active state of the metric. To add a new metric, select **New**.

</td></tr><tr><td>

Citations

</td><td>

Details of the citations such as reference, name, authority document, description, and compliance score in percentage \(%\). To add a new citation, select **Add**.

</td></tr><tr><td>

Goals

</td><td>

Details of the goals, such as name, state, category, start date, end date, owner, and status. To add a new goal, select **Add**.

</td></tr><tr><td>

Targets

</td><td>

Details of the target, such as name, owner, state, status, progress, actual value, target value, and end date. To add a new target, select **Add**.

</td></tr><tr><td>

Metric definition data

</td><td>

Details of the metric definition data, such as collection frequency, collection definition, interval end date, value, and state. **Note:** This related list is displayed only for an automated metric definition and a manual metric definition. It isn’t displayed for the calculated metric definition.

</td></tr><tr><td>

Calculated metric data

</td><td>

Details of the calculated metric data, such as interval end date, roll up frequency, and value. **Note:** This related list is displayed only for the calculated metric definition. It isn’t displayed for the automated metric definition and the manual metric definition.

</td></tr><tr><td>

Thresholds

</td><td>

Details of the metric definition thresholds, such as threshold type, metric definition, valid from, valid until, red threshold, amber threshold, and target value.**Note:** This related list is displayed only for an automated metric definition and a manual metric definition. It isn’t displayed for the calculated metric definition.

</td></tr></tbody>
</table>5.  To save the metric definition, select **Save**.

6.  To calculate the calculated metric data for the calculated metric definition, select **Aggregate**.

    The **Aggregate** action calculates the calculated metric data for the current interval end date and roll-up frequency to its parent metric definition. The calculated metric data record is displayed under the calculated metric data related list. A calculated metric definition score is created if it doesn’t exist for the current interval.

7.  To delete the metric definition, select **Delete**.

8.  To visually explore the 360° relationship view of the metric definition, select **360° view**.


**Parent Topic:**[Configuring GRC: Metrics](../concept/configuring-grc-metrics.md)

