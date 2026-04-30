---
title: Create planned task definitions
description: Create planned task definitions in Workplace Core to help workplace managers easily generate tasks that are often repeated and independent of shifts such as cleaning coffee vending machines or cleaning floors. You can quickly specify the task details and the frequency at which the task is to be performed.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing workplace tasks, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Create planned task definitions

Create planned task definitions in Workplace Core to help workplace managers easily generate tasks that are often repeated and independent of shifts such as cleaning coffee vending machines or cleaning floors. You can quickly specify the task details and the frequency at which the task is to be performed.

## Before you begin

**Important:** Starting with Workplace Core \(sn\_wsd\_core\) version 2.1, all updates and new features are available only on the Workplace Service Portal. The workplace services provided by ServiceNow® are removed from the Service Portal on Workplace Core \(sn\_wsd\_core\) beginning with version 2.1. To configure the Workplace service catalog in the Service Portal, see [Configure a catalog in Service Portal](https://www.servicenow.com/docs/access?context=associate-portal-catalog&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Role required: sn\_wsd\_core.admin or sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Workplace services** &gt; **Browse Workplace Services**.

2.  Select **Add planned task definition**.

3.  On the form, fill in the fields.

<table id="table_m13_jfb_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the planned task definition. For example, "Clean conference rooms" for the activity of sanitizing conference rooms.

</td></tr><tr><td>

Schedule

</td><td>

Work schedule to be used for planned tasks.

</td></tr><tr><td>

Workplace task template

</td><td>

Template used for the generated planned tasks. Selecting a template automatically populates certain fields such as **Assigned to**, **Short description**, and **Workplace task type** in the generated tasks. For information about workplace task templates, see [Configure a workplace task template](configure-workplace-task-template-wsd.md).

</td></tr><tr><td>

Processing Time \(hours\)

</td><td>

Amount of time it should take to complete a planned task.

</td></tr><tr><td>

Planned end time

</td><td>

Date and time by which the task should be finished.

</td></tr><tr><td>

Planned start time

</td><td>

Date and time when the task should start.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  If you accessed the form from Workplace Service Portal, on the verification page, you can create another planned task definition or generate planned tasks from this definition immediately.

    **Note:** You can also use this definition to generate planned tasks later. See the instructions in the [Generate planned tasks](create-planned-task-definitions-wsd.md) topic.

<table id="choicetable_hkt_5l1_xlb"><thead><tr><th align="left" id="d309373e257">

Option

</th><th align="left" id="d309373e260">

Action

</th></tr></thead><tbody><tr><td id="d309373e266">

**Create another planned task definition**

</td><td>

Select **Add another task definition**.

</td></tr><tr><td id="d309373e278">

**Generate planned tasks immediately**

</td><td>

1.  Select **View all task definitions**.
2.  Open the planned task definition and select **Generate Task**.
3.  Select the **Workplace Tasks** related list to view the generated planned tasks.


</td></tr></tbody>
</table>
## Result

-   The planned task definition is added to the list of all planned task definitions that you can view by navigating to **Workplace Core** &gt; **Workplace Tasks** &gt; **Planned Tasks Definitions**.
-   If you created planned tasks from this definition, they are added to the list of all planned tasks. You can view those tasks by navigating to **Workplace Safety Management** &gt; **Workplace Tasks** &gt; **Planned Tasks**.

**Parent Topic:**[Managing workplace tasks](../concept/managing-workplace-maintenance-tasks.md)

