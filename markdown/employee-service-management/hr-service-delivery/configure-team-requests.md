---
title: Configure team requests
description: Configure the type of team requests that you want to display on the Requests opened by your team widget in Manager Hub in Employee Center.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure Manager Hub, Manager Hub, Persona Based Experiences, HR Service Delivery, Employee Service Management]
---

# Configure team requests

Configure the type of team requests that you want to display on the **Requests opened by your team** widget in Manager Hub in Employee Center.

## Before you begin

Role required: sn\_mh.admin

This allows managers to be informed of any support requests their team has, that they may want to be aware of, even if no specific approval or task has been assigned to them.

In addition to the sn\_mh.manager\_hub\_user role, the logged in manager must also have the required ACLs or roles to view certain team requests. For example, if there are any open requests related to HR cases, then the logged in manager must also have the sn\_hr\_core.case\_reader role to view those requests.

## Procedure

1.  Navigate to **All** &gt; **Manager Hub** &gt; **Administration** &gt; **Team Requests Configurations**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_urb_sxq_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table on which the conditions are applied. For example: Requested item

</td></tr><tr><td>

Request type

</td><td>

Field of the table on which the conditions are applied. For example: cat\_itemThis field can be used to group the requests and display $\{request\_type\} in singular and multiple records labels.

</td></tr><tr><td>

Request status

</td><td>

State of the request.

</td></tr><tr><td>

User field

</td><td>

User to whom the request is placed. For example: Requested for

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the team request configuration record.

</td></tr><tr><td class="sub-head" colspan="2">

Display Details

</td></tr><tr><td>

Action type

</td><td>

Type of action displayed against the team request on Manager Hub in Employee Center, such as URL or Email.

</td></tr><tr><td>

URL

</td><td>

URL to be displayed against the team request on Manager Hub in Employee Center.

</td></tr><tr><td>

Action icon

</td><td>

Display icon to be displayed against the team request on Manager Hub in Employee Center.

</td></tr><tr><td>

Order

</td><td>

Order in which the team request configuration records are to be displayed on Manager Hub in Employee Center. The team request configuration record with the lowest order number appears first, and the team request configuration record with the highest order number appears last on the user interface.

</td></tr><tr><td>

Single record display label

</td><td>

Text that must appear when a single request is displayed on Manager Hub in Employee Center.For example: $\{employee\_name\} requested for $\{request\_type\}

 **Note:** Use tokens in display labels to show dynamic variables to end users. Available tokens: $\{employee\_name\}, $\{request\_type\}

</td></tr><tr><td>

Multiple record display label

</td><td>

Text that must appear when multiple requests are displayed on Manager Hub in Employee Center.For example: $\{count\} employee's requested for $\{request\_type\}

 **Note:** Use tokens in display labels to show dynamic variables to end users. Available tokens: $\{request\_type\}, $\{count\}

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configure Manager Hub](set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](run-rca-mh.md)

[Activate a scheduled job](../reference/activate-sj-mh.md)

[Configure important dates](configure-imp-dates.md)

[Configure team data](configure-team-data.md)

[Configure team column data](configure-team-columndata.md)

[Configure team filters](configure-team-filter.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](configure-daily-stats.md)

[Configure to do mappings](use-to-do-map.md)

[Configure widgets](configure-team-insights.md)

