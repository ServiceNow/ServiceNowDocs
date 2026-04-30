---
title: Configure team filters
description: Configure team filters that you want to display on the Team members tab in Your team menu in Employee Center. For example, a team filter can be Employee Type, which in turn contains other filters such as position and location type.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure Manager Hub, Manager Hub, Persona Based Experiences, HR Service Delivery, Employee Service Management]
---

# Configure team filters

Configure team filters that you want to display on the Team members tab in Your team menu in Employee Center. For example, a team filter can be Employee Type, which in turn contains other filters such as position and location type.

## Before you begin

Role required: sn\_mh.admin

## Procedure

1.  Navigate to **All** &gt; **Manager Hub** &gt; **Administration** &gt; **Team Filter Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Filter title|Unique title for the filter group record. For example, Employee type.|
    |Order|Order in which you want the group filter to appear on the Team members tab in Your team menu in Employee Center.|
    |Group all filters|Option to group filter. For example, you can group filters such as position and location type under one filter called Employee type.|
    |Active|Option to activate or deactivate the filter group record. When you deactivate a filter group record, the record does not appear on the user interface.|

4.  Click **Submit**.


## What to do next

Associate the filter to a team data configuration. Filter group is a UI shell, where you can configure display values and order related things. The data that is displayed in the filter group is fetched from a team data configuration.

1.  In the **Team Filter Group Data** related list, click **New**.

2.  On the form, fill in the fields.

<table id="table_ujf_lmx_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name of the filter group.

</td></tr><tr><td>

Team filter group

</td><td>

Name of the team filter group, for example, Employee Type.

</td></tr><tr><td>

Team data configuration

</td><td>

Contains configurations applied on table and fields of the table and so on. For example, for Employee Type the team data configuration is HR profile and Employee profile.

</td></tr><tr><td>

Table

</td><td>

Table associated with the team data configuration. It is selected by default after you have selected the team data configuration.

</td></tr><tr><td>

Column

</td><td>

Column to appear on the Your team tab.

</td></tr><tr><td>

Order

</td><td>

Order in which you want the filter to show up on the Team members tab in Your team menu in Employee Center.

</td></tr><tr><td>

Show select all option

</td><td>

Option to display **Select all in \{\}** in the filter on the Team members tab in Your team menu in Employee Center.Assume that there are 10 cities in a filter and if you want to provide an option to the user to select all the cities with a single link, then enable **Show select all option**.

</td></tr><tr><td>

Hide if all have same value

</td><td>

Option to hide the same filter values on the Team members tab in Your team menu in Employee Center.Assume that the **Hide if all have same value** option is selected and the **Show empty filter option** option is deselected; all the employees are residing in the same city, for example, London.

 In this case, the London filter will not appear on the Team members tab in Your team menu in Employee Center.

</td></tr><tr><td>

Show empty filter option

</td><td>

Option to display **No data** as a filter value so that managers can filter their employee list by users who do not have any data available. Assume that the **Hide if all have same value** and **Show empty filter option** options are selected; all the employees are residing in the same city, for example, London.

 In this case, both London and No data values appear on the Location filter on the Team members tab in Your team menu in Employee Center.

 **Note:** **Show empty filter option** should not be selected if you only want managers to filter by data values that are available for their employees. For example, if this option is not selected and most employees are residing in London, but some do not have a location set in their user record then the manager will only have the option London to select from.

</td></tr></tbody>
</table>3.  Click **Submit**.

**Parent Topic:**[Configure Manager Hub](set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](run-rca-mh.md)

[Activate a scheduled job](../reference/activate-sj-mh.md)

[Configure important dates](configure-imp-dates.md)

[Configure team requests](configure-team-requests.md)

[Configure team data](configure-team-data.md)

[Configure team column data](configure-team-columndata.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](configure-daily-stats.md)

[Configure to do mappings](use-to-do-map.md)

[Configure widgets](configure-team-insights.md)

