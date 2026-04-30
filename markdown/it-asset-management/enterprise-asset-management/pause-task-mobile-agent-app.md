---
title: Pause a task using the Mobile Agent application
description: Record a break from a work order task or asset task in the Mobile Agent application if you’re not continuing to work on it. Resume the task when you start working on it again. The system automatically tracks and calculates the actual time taken to complete the task even though the work was interrupted.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Record time worked on a task using the Mobile Agent application, Manage an Enterprise Asset Management task using the Mobile Agent application, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Pause a task using the Mobile Agent application

Record a break from a work order task or asset task in the Mobile Agent application if you’re not continuing to work on it. Resume the task when you start working on it again. The system automatically tracks and calculates the actual time taken to complete the task even though the work was interrupted.

## Before you begin

The **work.management.allow.auto.timecard** system property must be enabled for the time cards to be automatically created when you start working on a task.

Role required:

-   To work on a work order task: wm\_agent and sn\_eam.enterprise\_asset\_technician
-   To work on Pick Up Asset task: sn\_eam.enterprise\_asset\_technician

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen of the My Tasks application opens with the first few tasks in the list of tasks assigned to you displayed.

3.  If the task you want to pause isn't displayed, tap **See all**.

4.  Filter or sort the task view.

    -   To filter your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\) and enter the values to use as a filter in the **Due Date**, **Asset**, **Location**, or **Priority** fields.
    -   To sort your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\), tap **Sort by**, and select the fields by which to sort your tasks.
5.  Tap the task record that you want to pause.

6.  Tap the more actions icon \(![More actions icon](../../hardware-asset-management/image/more-actions-icon.png)\) at the top right corner of the screen and then tap **Pause work**.

    On the **Details** tab, the **Close complete** option changes to **Resume work**.

7.  Tap **Resume Work** when you’re ready to work on the activity again.


## Result

Each time you pause or resume work on the task, the actual time you worked on the task is automatically calculated. An entry for the time worked is created in the Time worked time card.

**Parent Topic:**[Record time worked on a task using the Mobile Agent application](../concept/record-time-mobile-agent-app.md)

**Related topics**  


[Record time worked for a task manually using the Mobile Agent application](record-time-worked-manually.md)

