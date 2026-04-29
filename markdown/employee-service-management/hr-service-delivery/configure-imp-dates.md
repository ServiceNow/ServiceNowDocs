---
title: Configure important dates
description: Configure important dates, such as employee leaves, employee birthdays, or anniversaries, that you want to display on the Upcoming team events widget in Manager Hub.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Configure important dates

Configure important dates, such as employee leaves, employee birthdays, or anniversaries, that you want to display on the **Upcoming team events** widget in Manager Hub.

## Before you begin

Role required: sn\_mh.admin

## Procedure

1.  Navigate to **All** &gt; **Manager Hub** &gt; **Administration** &gt; **Important Dates Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_urb_sxq_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table on which you want to apply filter conditions.

</td></tr><tr><td>

Condition

</td><td>

Conditions that you want to apply on the selected table.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate important dates configuration record.

</td></tr><tr><td>

User field

</td><td>

Field of the table on which the manager filter is applied to fetch the reporting employee details such as name or email.

</td></tr><tr><td class="sub-head" colspan="2">

Display details

</td></tr><tr><td>

Is annual recurring event

</td><td>

Enable the check box if the event occurs every year, for example, birthdays or anniversaries.**Note:** For an annual recurring event, the offset date range must be less than 365 days.

</td></tr><tr><td>

Date offset unit

</td><td>

Number of days, weeks, or months that defines your offset units. For example, week, day, or month.

</td></tr><tr><td>

Date offset before quantity

</td><td>

Do you want your offset to be before the start date field that you have selected, for example, 1.

</td></tr><tr><td>

Date offset after quantity

</td><td>

Do you want your offset to be after the start date field that you have specified, for example, 1.

</td></tr><tr><td>

Start date field

</td><td>

Indicates the start date from which you want to pull important dates.For example: Assume that the important dates configuration record is being created to display birthdays of team members. Data offset unit is **Week** and Date offset before quantity and Date offset after quantity is **1**.

 All the birthdays before and after a week of start date are pulled and displayed on the Important dates widget in Manager Hub in Employee Center.

</td></tr><tr><td>

End date field

</td><td>

Indicates the end date until which you want to pull important dates.

</td></tr><tr><td>

Display data source

</td><td>

Display source for grouping based on the field selected. For example, PTOs can be grouped by PTO type.

</td></tr><tr><td>

Order

</td><td>

Order in which the important dates configuration records are to be displayed on Manager Hub in Employee Center. The important dates configuration record with the lowest order number appears first, and the important dates configuration record with the highest order number appears last on the user interface.

</td></tr><tr><td>

Action type

</td><td>

Type of action displayed against the important date record on Manager Hub in Employee Center, such as URL or Email.

</td></tr><tr><td>

URL

</td><td>

URL to be displayed against the important date record on Manager Hub in Employee Center.

</td></tr><tr><td>

Action icon

</td><td>

Display icon to be displayed against the important date record on Manager Hub in Employee Center.

</td></tr><tr><td>

Action tooltip

</td><td>

Text that appears when you point to the action icon against the important date record on Manager Hub in Employee Center.

</td></tr><tr><td>

Single record display label

</td><td>

Text that must appear only if a single important date configuration record is displayed on Manager Hub in Employee Center. For example: $\{employee\_name\}'s anniversary.**Note:** Use tokens in display labels to show dynamic variables to end users. Available tokens: $\{employee\_name\}, $\{display\_data\}

</td></tr><tr><td>

Multiple record display label

</td><td>

Text that must appear when multiple important date configuration records are displayed in Manager Hub in Employee Center. For example: $\{count\} employee's have anniversary.**Note:** Use tokens in display labels to show dynamic variables to end users. Available tokens: $\{display\_data\}, $\{count\}

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configure Manager Hub](set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](run-rca-mh.md)

[Activate a scheduled job](../reference/activate-sj-mh.md)

[Configure team requests](configure-team-requests.md)

[Configure team data](configure-team-data.md)

[Configure team column data](configure-team-columndata.md)

[Configure team filters](configure-team-filter.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](configure-daily-stats.md)

[Configure to do mappings](use-to-do-map.md)

[Configure widgets](configure-team-insights.md)

