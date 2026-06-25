---
title: Close a Pick Up Asset task using the Mobile Agent application
description: Complete and close the Pick Up Asset task for the enterprise asset that you have picked up from the designated stockroom for your assigned work order using the Mobile Agent application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/pickup-asset-task-mobile-agent.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage an Enterprise Asset Management task using the Mobile Agent application, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Close a Pick Up Asset task using the Mobile Agent application

Complete and close the Pick Up Asset task for the enterprise asset that you have picked up from the designated stockroom for your assigned work order using the Mobile Agent application.

## Before you begin

The status of the Pick Up Asset task must be Work in progress.

Role required: wm\_agent or sn\_eam.enterprise\_asset\_technician

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen of the My Tasks application opens with the first few tasks in the list of tasks assigned to you displayed.

3.  If the task you want to close isn't displayed, tap **See all**.

4.  Filter or sort the task view.

    -   To filter your tasks, tap the Filter icon \[Omitted image "filter-mobile-task-eam.png"\] Alt text: and enter the values to use as a filter in the **Due Date**, **Asset**, **Location**, or **Priority** fields.
    -   To sort your tasks, tap the Filter icon \[Omitted image "filter-mobile-task-eam.png"\] Alt text:, tap **Sort by**, and select the fields by which to sort your tasks.
5.  Tap the work order task for which you want to close the associated Pick Up Asset task.

6.  Tap the **Parts** tab.

    The Pick Up Asset Tasks section shows the first few Pick Up Asset tasks in the list of tasks associated with the work order task assigned to you.

7.  If the task you want to complete isn't displayed, tap **See All**.

8.  Tap the Pick Up Asset task that you want to complete and then tap **Close complete**.


## Result

-   The state of the Pick Up Asset task changes from Open to Closed Complete.
-   A record is created in the Asset Usages section with the Status of Not Used and State of In stock.

    **Note:** For a consumable asset, the State changes to Consumed.


## What to do next

Take necessary asset action on the enterprise asset associated with the work order. For details, see [Take action on an enterprise asset using the Mobile Agent application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/complete-work-order-mobile-agent.md).

**Parent Topic:**[Manage an Enterprise Asset Management task using the Mobile Agent application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/work-order-mobile-agent-eam.md)

**Related topics**  


[View your tasks using the Mobile Agent application]()

[Assign a group task to yourself using the Mobile Agent application]()

[Start working on tasks using the Mobile Agent application]()

[Record time worked on a task using the Mobile Agent application]()

[Initiate a request to source parts for work order tasks using the Mobile Agent application]()

[Take action on an enterprise asset using the Mobile Agent application]()

[Close a work order for an enterprise asset using the Mobile Agent application]()

[Create a checklist for work order tasks using the Mobile Agent application]()

[View knowledge articles related to work order tasks in the Mobile Agent application]()

[Create work notes about the work order tasks using the Mobile Agent application]()

[Set enterprise assets to the shutdown state using the Mobile Agent application]()

[Start up enterprise assets after maintenance activities using the Mobile Agent application]()

[Move enterprise assets to maintenance state using the Mobile Agent application]()

