---
title: Configure to do mappings
description: Create additional conditions or mappings to display managerial tasks and requests.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Configure to do mappings

Create additional conditions or mappings to display managerial tasks and requests.

## Before you begin

Role required: sn\_mh.admin

**Note:**

-   Prior to this Utah release, you could create additional conditions for to-do mappings using the To-dos Configuration form in Employee Center. Starting with the Utah release, you can create additional conditions for to-do mappings using the To-dos mapping module in Manager Hub.
-   If you are upgrading to Utah release, additional conditions that were created for to-do mappings in the To-dos Configuration form in Employee Center must be created again in the To-dos mapping module in Manager Hub.

## Procedure

1.  Navigate to **All** &gt; **Manager Hub** &gt; **Administration** &gt; **To-dos mappings**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_bj4_y5f_rvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To-do filter condition

</td><td>

To-do filter condition on which additional conditions are applied. For more information on to-do filter condition, see [Create or modify a to-dos filter](../../employee-center/task/configure-to-dos-page-filters.md).

</td></tr><tr><td>

Table

</td><td>

Read-only field that is picked from the To-dos configuration table. For example, HR Task \[sn\_hr\_core\_task\].

</td></tr><tr><td>

Map parent

</td><td>

Option to enable the selection of reportee fields from the To-dos configuration table or its parent table.

</td></tr><tr><td>

Parent mapping reference field

</td><td>

Option to select a reference field from the parent table.**Note:** This option appears only when the **Map parent** field is enabled.

</td></tr><tr><td>

Parent Reportee fields

</td><td>

Option to select reportee fields from the parent table. For example, select reportee fields from the HR Case \[sn\_hr\_core\_case\] table.**Note:** This option appears only when the **Map parent** field is enabled.

</td></tr><tr><td>

Reportee fields

</td><td>

Option to select reportee fields from the To-dos configuration table. For example, select reportee fields from the HR Task \[sn\_hr\_core\_task\].

</td></tr><tr><td>

Active

</td><td>

Option to activate the use of additional filter conditions.

</td></tr><tr><td>

Order

</td><td>

Order in which additional filter conditions are applied.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configure Manager Hub](set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](run-rca-mh.md)

[Activate a scheduled job](../reference/activate-sj-mh.md)

[Configure important dates](configure-imp-dates.md)

[Configure team requests](configure-team-requests.md)

[Configure team data](configure-team-data.md)

[Configure team column data](configure-team-columndata.md)

[Configure team filters](configure-team-filter.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](configure-daily-stats.md)

[Configure widgets](configure-team-insights.md)

