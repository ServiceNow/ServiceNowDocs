---
title: Configure team column data
description: Configure column titles that you want to display on the Team members tab in Your team menu. For example, configure a column title to denote the current status of an employee such as new hire, or on leave.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Configure team column data

Configure column titles that you want to display on the Team members tab in Your team menu. For example, configure a column title to denote the current status of an employee such as new hire, or on leave.

## Before you begin

Role required: sn\_mh.admin

## Procedure

1.  Navigate to **All** &gt; **Manager Hub** &gt; **Administration** &gt; **Team Column Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Column title|Name of the team column configuration record. For example, Location.|
    |Order|Order in which the column must appear on the Team members tab in Your team menu.|
    |Active|Option to activate or deactivate the team column configuration.|

4.  Click **Submit**.


## What to do next

Associate the record to a team column data configuration.

1.  In the Team Column Data Configuration related list, click **New**.

2.  On the form, fill in the fields.

<table id="table_ujf_lmx_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Team column configuration

</td><td>

Name of the Team Column Configuration record. For example, Location.

</td></tr><tr><td>

Team data configuration

</td><td>

Team data configuration with which you want to associate the Team column configuration record. For example, User.

</td></tr><tr><td>

Table

</td><td>

Table that is associated with the team data configuration. This field gets auto-populated by selecting the Team data configuration. For example, sys\_user

</td></tr><tr><td>

Column display fields

</td><td>

Fields of the table that you want to display on the Team members tab in Your team menu in Employee CenterFor example, you want to display time zone, city, state, and country fields \(of employees\) from the sys\_user table on the Location column on the Team members tab in Your team menu in Employee Center

</td></tr><tr><td>

Order

</td><td>

Order in which you want to display the column display fields on the Team members tab in Your team menu in Employee Center. The column display field with the lowest order number appears first, and the column display field with the highest order number appears last on the user interface.**Note:** On the compact cards \(list or grid view\) there is a limit of what gets displayed, but on the employee modal all the data gets displayed. In addition, if no data is available for an employee for one of the team data records, the next one that is available in order gets displayed.

</td></tr></tbody>
</table>3.  Click **Submit**

**Parent Topic:**[Configure Manager Hub](set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](run-rca-mh.md)

[Activate a scheduled job](../reference/activate-sj-mh.md)

[Configure important dates](configure-imp-dates.md)

[Configure team requests](configure-team-requests.md)

[Configure team data](configure-team-data.md)

[Configure team filters](configure-team-filter.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](configure-daily-stats.md)

[Configure to do mappings](use-to-do-map.md)

[Configure widgets](configure-team-insights.md)

