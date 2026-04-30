---
title: Add a Task tab on the Standard Ticket page
description: Add a Task tab on the Standard Ticket page to let employees view the tasks that are assigned to them by the agents.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring your service for Universal Task, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Add a Task tab on the Standard Ticket page

Add a Task tab on the Standard Ticket page to let employees view the tasks that are assigned to them by the agents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration**.

2.  Click your service-specific table to open it.

3.  In the Tabs Configurations related list, click **New**.

4.  On the Tab configuration form, in the **Type** field, select **Custom**.

5.  Enter the **Tab name**.

    For example, `Tasks/To-dos`.

6.  Add the appropriate filter conditions to control the visibility of the tab.

    For example, set **Sys ID** to `javascript:new sn_uni_task.UniversalTaskUtils().hasTasksToShow(current)` to make the task tab visible only if there tasks are assigned to the employee. ![Filter conditions for tab configurations.](../images/ut-tab-configuration.png)

7.  In the **Widget** field, add a widget.

    **Note:** The Uni Task Parent is the default widget that you can use to add the **Universal Task** tab in the Standard Ticket.

8.  Click **Submit**.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Add a Universal Task related list](create-relatedlist-ur.md)

**Next topic:**[Define the agent criteria for Universal Task](ut-config-extn-point-agent.md)

