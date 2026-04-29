---
title: Configure team data
description: Configure team data that you want to display on employee cards and modal in the Team members tab in Your team menu. Team data configurations are required to support column configurations and filter configurations.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Configure team data

Configure team data that you want to display on employee cards and modal in the Team members tab in Your team menu. Team data configurations are required to support column configurations and filter configurations.

## Before you begin

Role required: sn\_mh.admin

## Procedure

1.  Navigate to **All** &gt; **Manager Hub** &gt; **Administration** &gt; **Team Data Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_urb_sxq_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the team data configuration record. For example, team data configuration record is being created for **Leave**.

</td></tr><tr><td>

Table

</td><td>

Table on which you want to apply filter conditions. For example, table can be **Leave of absence**.

</td></tr><tr><td>

User field

</td><td>

Field of the table on which you want to apply conditions. For example, user field can be employee.

</td></tr><tr><td>

Conditions

</td><td>

Conditions applied on the selected table to display the required values. For example, conditions are being applied on **Leave of absence** table to pull the required details. Later, employee sys\_IDs are pulled.

</td></tr><tr><td>

Use alternate label

</td><td>

Option to display a text when records match or do not match the team data configuration.For example:

-   **Use alternate label** to display leaves.
-   **Use alternate label** to display the number of incidents raised by any employee.


</td></tr><tr><td>

Alternate label

</td><td>

Value displayed when one or more records match the set conditions.For example:

-   **Alternate label** can be: On leave
-   **Alternate label** can be: $\{count\} incidents found


</td></tr><tr><td>

No data alternate label

</td><td>

Value displayed when no records match the set conditions.For example, **No data alternate label** can be: No incidents found

</td></tr><tr><td>

Advanced

</td><td>

Option to add a script to retrieve the preferred records. This option allows you to configure display values from multiple data-sources, control the values, and provide a hyperlink for the display values.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configure Manager Hub](set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](run-rca-mh.md)

[Activate a scheduled job](../reference/activate-sj-mh.md)

[Configure important dates](configure-imp-dates.md)

[Configure team requests](configure-team-requests.md)

[Configure team column data](configure-team-columndata.md)

[Configure team filters](configure-team-filter.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](configure-daily-stats.md)

[Configure to do mappings](use-to-do-map.md)

[Configure widgets](configure-team-insights.md)

