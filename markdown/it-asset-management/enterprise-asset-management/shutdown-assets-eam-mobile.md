---
title: Set enterprise assets to the shutdown state using the Mobile Agent application
description: Move assets of a shutdown work order task to the shutdown state in the Mobile Agent application to indicate that the assets are unavailable for use during maintenance.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-02-21"
reading_time_minutes: 4
keywords: [Shut down enterprise assets, Shutdown work order task, Shutdown work type]
breadcrumb: [Manage an Enterprise Asset Management task using the Mobile Agent application, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Set enterprise assets to the shutdown state using the Mobile Agent application

Move assets of a shutdown work order task to the shutdown state in the Mobile Agent application to indicate that the assets are unavailable for use during maintenance.

## Before you begin

**Important:** The Affected assets tab, Shutdown work type, and **Shutdown** option are available with Enterprise Asset Management version 10.0 and later.

The shutdown work order task must be in the Work in progress state before you can shut down assets. The assets must be in the In use or In maintenance state.

Role required: sn\_eam.enterprise\_asset\_technician

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen of the My Tasks application opens, displaying the first few tasks assigned to you.

3.  If the task you want to start isn't displayed, tap **See all**.

4.  Filter or sort the task view.

    -   To filter your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\) and enter the values to use as a filter in the **Due Date**, **Asset**, **Location**, or **Priority** fields.
    -   To sort your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\), tap **Sort by**, and select the fields by which to sort your tasks.
5.  Tap the work order task of the **Shutdown** work type that has the assets that you want to shut down.

6.  On the **Details** tab, tap **Start Work**.

7.  Tap the **Related** tab.

    The **Affected assets** section shows all the assets associated with the work order.

8.  Tap **Shutdown**.

9.  In the **Select assets to shutdown** screen, select the assets that you want to shut down.

10. Tap **Submit**.


## Result

In the Affected assets list, the substate of the assets that are shut down changes to Is shutdown.

**Parent Topic:**[Manage an Enterprise Asset Management task using the Mobile Agent application](work-order-mobile-agent-eam.md)

**Related topics**  


[View your tasks using the Mobile Agent application](track-tasks-using-mobile-agent-app.md)

[Assign a group task to yourself using the Mobile Agent application](pick-task-from-assignment-group.md)

[Start working on tasks using the Mobile Agent application](start-work-mobile-agent-eam.md)

[Record time worked on a task using the Mobile Agent application](../concept/record-time-mobile-agent-app.md)

[Initiate a request to source parts for work order tasks using the Mobile Agent application](source-parts-mobile-agent.md)

[Close a Pick Up Asset task using the Mobile Agent application](pickup-asset-task-mobile-agent.md)

[Take action on an enterprise asset using the Mobile Agent application](complete-work-order-mobile-agent.md)

[Close a work order for an enterprise asset using the Mobile Agent application](close-workorder-mobile-app-eam.md)

[Create a checklist for work order tasks using the Mobile Agent application](manage-work-orders-using-checklist.md)

[View knowledge articles related to work order tasks in the Mobile Agent application](view-knowledge-articles-mobile-agent.md)

[Create work notes about the work order tasks using the Mobile Agent application](create-worknote-mobile-agent.md)

[Start up enterprise assets after maintenance activities using the Mobile Agent application](startup-assets-eam-mobile.md)

[Move enterprise assets to maintenance state using the Mobile Agent application](move-assets-maintenance-mobile.md)

