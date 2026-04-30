---
title: Make a timeline visible to a selected user
description: Create a custom module within an application and defining the roles that can access it, to make selected timelines available to users.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Timeline pages, Viewing record information over time, Time configuration references, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Make a timeline visible to a selected user

Create a custom module within an application and defining the roles that can access it, to make selected timelines available to users.

## About this task

To permit these users to update task records directly from the timeline, configure the timeline to enable span dragging.

**Note:** Timelines delivered by a custom module are not entirely dynamic. The left pane, summary pane, auto-refresh feature, and the grid lines are not dynamic, and do not reflect updates to the timeline record after creating the module link. However, the data represented by the spans, labels, and tooltips display all updates in the custom module.

To create a timeline page module:

## Procedure

1.  Click the **Edit application** icon on an application \(such as Incident\) in the navigation pane.

2.  In the application Modules related list, click **New**.

3.  Configure the Module form to add the **Timeline page** field.

4.  Fill in the form as described in the table and click **Submit**.

    The Module form provides the following fields.

    |Field|Description|
    |-----|-----------|
    |Title|Name of the module as it appears in the navigation pane. For example, you might use Planning Timeline.|
    |Order|Number to determine the sequence in which this condition should be evaluated if more than one matching condition exists. Conditions with a lower order are evaluated first.|
    |Application|Application for the new module.|
    |Hint|Brief description of the module that appears when the user places the cursor over the module name. For example, you might enter Weekly view of high priority changes.|
    |Active|Check box that enables the module for the defined roles. Clear this check box to disable the module for all users.|
    |Image|Icon that should appear with the module name.|
    |Link type|Select **Timeline Page**. When you select this link, the **Timeline Page** field appears.|
    |Timeline Page|Timeline page you want to appear in this module. For example, for the Change application select a change-related timeline, for the Incident application select an incident-related timeline.|
    |Roles|Roles that can access this module.|
    |Override application menu roles|Check box that indicates that this module should appear when the user has the specified roles. Otherwise, the user must have the roles specified by both the application menu and the module.|


**Parent Topic:**[Timeline pages](../concept/c_TimelinePages.md)

