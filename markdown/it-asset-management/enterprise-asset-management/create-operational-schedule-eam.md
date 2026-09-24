---
title: Create an operational schedule for enterprise assets
description: Define the scheduled operational time, which is the duration during which the asset will be in use, by creating an operational schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/create-operational-schedule-eam.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring KPI monitoring settings, Configure, Enterprise Asset Management, Asset Management]
---

# Create an operational schedule for enterprise assets

Define the scheduled operational time, which is the duration during which the asset will be in use, by creating an operational schedule.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

An operational schedule record is stored in the Asset schedule \[sn\_itam\_common\_asset\_schedule\] table. If an operational schedule isn't defined, the Default operation schedule \(24/7\) hours is applied.

**Note:** The calculation of asset key performance indicators \(KPIs\) begins when the asset first moves to the In Use state. Therefore, the linked operational schedule must cover the entire period for accurate results.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  From the navigation panel of the Admin center view, navigate to **KPI configuration** &gt; **Operational schedules**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_izq_htb_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the operational schedule.

</td></tr><tr><td>

Parent

</td><td>

Parent schedule that constraints the new schedule.For more details, see [Parent and child schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_ParentAndChildSchedules.md).

</td></tr><tr><td>

Time zone

</td><td>

Time zone for the schedule. If you select **Floating**, the time zone is relative to whatever process is accessing the item at the time.-   For example, if an enterprise administrator in Amsterdam sets a floating schedule for 8:00A.M. to 5:00P.M., a user in San Jose sees the schedule as 8:00 A.M. to 5:00 P.M.
-   When a schedule is defined in a specific time zone, users in different time zones see the schedule with their own time zone applied.


</td></tr><tr><td>

Description

</td><td>

Description of the operational schedule.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  Add one or more schedule entries to the operational schedule.

    1.  Select the **Schedule Entries** tab.

    2.  Select **New**.

    3.  On the Schedule Entry New record, fill in the fields.

        For details on Schedule Entry New record fields, see [Schedule entry fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_ScheduleEntryFields.md).

    4.  Select **Submit**.

    A schedule entry is created and listed under the Schedule Entries tab.

    **Note:**

    You can’t edit a schedule or its entries. If you want to stop using an asset schedule, you can deactivate it by deselecting the **Active** check box. You can then create a schedule as needed.

8.  To view the calendar view of the schedule with the schedule entries, select **Show schedule**.


## What to do next

[Map enterprise assets to an operational schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/create-asset-schedule-eam.md).

