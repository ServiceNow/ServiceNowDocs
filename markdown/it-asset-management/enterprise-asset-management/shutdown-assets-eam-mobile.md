---
title: Set enterprise assets to the shutdown state using the Mobile Agent application
description: Move assets of a shutdown work order task to the shutdown state in the Mobile Agent application to indicate that the assets are unavailable for use during maintenance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/shutdown-assets-eam-mobile.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Shut down enterprise assets, Shutdown work order task, Shutdown work type]
breadcrumb: [Manage an Enterprise Asset Management task using the Mobile Agent application, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Set enterprise assets to the shutdown state using the Mobile Agent application

Move assets of a shutdown work order task to the shutdown state in the Mobile Agent application to indicate that the assets are unavailable for use during maintenance.

## Before you begin

The shutdown work order task must be in the Work in progress state before you can shut down assets. The assets must be in the In use or In maintenance state.

Role required: sn\_eam.asset\_technician

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen of the My Tasks application opens, displaying the first few tasks assigned to you.

3.  If the task you want to start isn't displayed, tap **See all**.

4.  Filter or sort the task view.

    -   To filter your tasks, tap the Filter icon \(\[Omitted image "filter-mobile-task-eam.png"\] Alt text: Filter icon\) and enter the values to use as a filter in the **Due Date**, **Asset**, **Location**, or **Priority** fields.
    -   To sort your tasks, tap the Filter icon \(\[Omitted image "filter-mobile-task-eam.png"\] Alt text: Filter icon\), tap **Sort by**, and select the fields by which to sort your tasks.
5.  Tap the work order task of the **Shutdown** work type that has the assets that you want to shut down.

6.  On the **Details** tab, tap **Start Work**.

7.  Tap the **Related** tab.

    The **Affected assets** section shows all the assets associated with the work order.

8.  Tap **Shutdown**.

9.  In the **Select assets to shutdown** screen, select the assets that you want to shut down.

10. Tap **Submit**.


## Result

In the Affected assets list, the substate of the assets that are shut down changes to Is shutdown.

**Parent Topic:**[Manage an Enterprise Asset Management task using the Mobile Agent application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/work-order-mobile-agent-eam.md)

**Related topics**  


[View your tasks using the Mobile Agent application]()

[Assign a group task to yourself using the Mobile Agent application]()

[Start working on tasks using the Mobile Agent application]()

[Record time worked on a task using the Mobile Agent application]()

[Initiate a request to source parts for work order tasks using the Mobile Agent application]()

[Close a Pick Up Asset task using the Mobile Agent application]()

[Take action on an enterprise asset using the Mobile Agent application]()

[Close a work order for an enterprise asset using the Mobile Agent application]()

[Create a checklist for work order tasks using the Mobile Agent application]()

[View knowledge articles related to work order tasks in the Mobile Agent application]()

[Create work notes about the work order tasks using the Mobile Agent application]()

[Start up enterprise assets after maintenance activities using the Mobile Agent application]()

[Move enterprise assets to maintenance state using the Mobile Agent application]()

