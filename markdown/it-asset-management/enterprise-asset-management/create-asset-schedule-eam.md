---
title: Map enterprise assets to an operational schedule
description: Create an asset schedule to map the enterprise assets to an operation schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/create-asset-schedule-eam.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring KPI monitoring settings, Configure, Enterprise Asset Management, Asset Management]
---

# Map enterprise assets to an operational schedule

Create an asset schedule to map the enterprise assets to an operation schedule.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

An asset schedule record is stored in the Asset schedule policy \[sn\_asset\_cmn\_schdule\_policy\] table.

**Note:** If an asset isn't associated with an operational schedule, the Default asset schedule \(24 hours, 7 days a week or 24/7\) will be applied.

The **Asset performance - Map schedule policies** job runs weekly to sync the mapping between assets and the operational schedule.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  From the navigation panel of the Admin center view, navigate to **KPI configuration** &gt; **Asset schedules**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_tgv_h3c_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the asset schedule.

</td></tr><tr><td>

Source table

</td><td>

Source table for the assets. You can select any of the following tables:-   Enterprise asset \[sn\_ent\_asset\]
-   Construction asset \[sn\_ent\_construction\_asset\]
-   Facility asset \[sn\_ent\_facility\_asset\]
-   Industrial asset \[sn\_ent\_industrial\_asset\]
-   Linear asset \[sn\_eam\_linear\_asset\]
-   Medical asset \[sn\_ent\_medical\_asset\]
-   Retail asset \[sn\_ent\_reatail\_asset\]
-   Tactical equipment asset \[sn\_ent\_tactical\_asset\]
-   Transportation asset \[sn\_ent\_transportation\_asset\]
-   Wearable asset \[sn\_ent\_wearable\_asset\]
-   Hardware \[alm\_hardware\]


</td></tr><tr><td>

Condition

</td><td>

Set a condition to select the assets that you want to associate with the operational schedule. For example, if you set the **Department** field to **IT**, the operational schedule is inked to all assets within the IT department.**Note:** Select the source table before setting the condition.

</td></tr><tr><td>

Schedule

</td><td>

Operational schedule that you want to associate with the assets.

</td></tr><tr><td>

Priority

</td><td>

Order in which schedules should be applied to an asset when there are overlapping schedules.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the asset schedule is active.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  To sync the mapping between the assets and the operational schedules on demand, select **Sync KPI records**.


