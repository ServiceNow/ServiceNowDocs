---
title: Create application records from improvement initiatives
description: Create records for integrated applications from improvement initiatives or CIM tasks to transform improvement initiatives into broader, actionable efforts to enable improvements across teams and processes.
locale: en-US
release: australia
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an improvement request, Continual Improvement Management, IT Service Management]
---

# Create application records from improvement initiatives

Create records for integrated applications from improvement initiatives or CIM tasks to transform improvement initiatives into broader, actionable efforts to enable improvements across teams and processes.

## Before you begin

Role required: sn\_cim.improvement\_coordinator or sn\_cim.improvement\_manager

## Procedure

1.  Navigate to your improvement initiative or CIM task record.

    -   Improvement initiative: **All** &gt; **Continual Improvement** &gt; **My CIM Initiatives**
    -   CIM task: **All** &gt; **Continual Improvement** &gt; **CIM Tasks**
2.  Find and open the Improvement Initiative or CIM task record from which you want to create an application record.

3.  Create an application record by selecting the corresponding application record link in the Related Links section.

    **Note:** Related links are visible only when a CIM task is in the Open, Work in Progress, or On Hold state.

<table id="table_ugr_kht_bgc"><thead><tr><th>

Record type

</th><th>

Link to select

</th></tr></thead><tbody><tr><td>

Demand

</td><td>

Create Demand

</td></tr><tr><td>

Project

</td><td>

Create Project

</td></tr><tr><td>

Coaching opportunity

</td><td>

Create Coaching Opportunity

</td></tr><tr><td>

Knowledge base articles

</td><td>

Create Knowledge

</td></tr><tr><td>

Agile Development story

</td><td>

Create Story

</td></tr><tr><td>

Performance Analytics automated indicator

</td><td>

Create PA Indicator

</td></tr><tr><td>

Change

</td><td>

Create Change**Note:** You must have the following roles to view and create change requests:

-   change\_read, change\_write, or ITIL roles to view the **Create Change** link.
-   change\_write or ITIL roles to create change records.
If you have not been assigned the required roles, contact your system administrator.

</td></tr></tbody>
</table>    **Note:**

    Default field values set in the **sn\_cim.initiative\_copy\_attributes** property are populated in the application record form. Contact your administrator to edit this property by adding or deleting fields. For more information, see [Configure CIM integration property](configure-cim-int-property.md).

4.  Select **Submit**.


## Result

The application record is created and UI changes display on the source improvement initiative or CIM task record and corresponding application records. For more information, see [Updates after application record creation from improvement initiatives](../reference/updates-app-record-from-initiative.md).

**Parent Topic:**[Create an improvement request](create-cim-request.md)

