---
title: Integration with Project Portfolio Management
description: Link project tasks to work orders to assist with managing installation or deployment projects in the field.
locale: en-US
release: xanadu
product: Field Service Integrations
classification: field-service-integrations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Integration with Project Portfolio Management

Link project tasks to work orders to assist with managing installation or deployment projects in the field.

A project can have multiple tasks that are assigned to field service agents. Using the Field Service Management integration with Project Portfolio Management, you can create work orders directly from project tasks. Linking project tasks to work orders in this way:

-   Synchronizes the planned and actual dates between the project task and the work order.
-   Synchronizes the states between the project task and the work order.

To create a work order from a project task, click the **Create Work Order** related link on the Project Task form. To view an active linked work order, click the **View Work Order** related link on the Project Task form. Project tasks can have more than one linked work order, but only one work order can be active at a time.

## Dates

Dates are synchronized in one direction, from the project task to the linked work order and to any work order tasks.

-   Work order tasks created for a linked work order have fixed **Window start** and **Window end** dates that are based on the planned start and end dates of the project task.
-   Updates to project task dates are also updated in the linked work order tasks for tasks that are not in the **Work In Progress** or **Closed** states.

**Note:** Changes to the dates on a work order task do not change the dates on the linked project task.

## States

State changes are synchronized in one direction, from the work order to the project task.

-   Updating the work order state also updates the state of the linked project task.
-   Updating the state of a project task add a note to the **Work Notes** field on the linked work order.
-   Closing a work order also closes the project tasks.

If an update to the state of a project task fails, a note is added to the project task **Work notes** field about the corresponding work order update. Updates can fail with project tasks that have dependencies.

Work order and project task states are updated as follows.

|Work Order State|Project Task State|
|----------------|------------------|
|Work In Progress|Work In Progress|
|Close Complete|Close Complete|
|Close Incomplete|Close Incomplete|
|Canceled|Close Skipped|

## Plugins

Activate the Field Service with Project Management plugin \(com.snc.wm\_ppm\) to use this feature. This plugin requires the Field Service Management plugin \(com.snc.work\_management\) and the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

-   **[Customize the work order state transition map](customize-state-transition-map.md)**  
Users with the system administrator role can customize the work order state transition map, which maps work order states to project task states.

**Parent Topic:**[Integrating Field Service Management with other applications](integrate-fsm-other-applications.md)

