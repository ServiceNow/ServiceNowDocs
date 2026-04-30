---
title: My active items widget configuration
description: The My active items widget displays all user activity that requires your input or review.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-02-26"
reading_time_minutes: 3
breadcrumb: [Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# My active items widget configuration

The My active items widget displays all user activity that requires your input or review.

In the My active items widget, tasks, surveys, and request activities are available by default in the Employee Center. The Tasks activity is set to primary by default. Task activities are displayed using the existing to-do configuration and the Requests activities are displayed using the existing request filters.

**Note:** You can add additional configurations to display your activities. For example, to display activities for reservations, you must install and activate the plugin for the ServiceNow® Workplace Reservation Management application.

From **My Active Items** widget, admins can perform the following actions.

-   Organize items based on priority or urgency.
-   View the items in vertical or horizontal layouts.
-   Perform actions on the assigned tasks from **My Active Items**.

## My active items actions

You can now configure action framework to allow employees to perform actions from the My active items.

​Configure **Action group** for the primary activity to complete suitable actions. For tasks, the approve and reject actions are available out-of-the-box. For more information, see [Enable task configuration for approvals](../task/approval-hub-to-dos-page-filters.md)

**Note:** When you do not associate an action group with the tasks, the **View details** option appears to navigate to the activity details page.

**My Active Items Widget Layout Guidance**

The My Active Items widget is designed for optimal display and usability when configured using a column size of 3 or greater. This layout ensures that information presented within the widget remains readable and visually consistent across Employee Center topics.

**Note:** The My Active Items widget does not support column sizes less than 3. If you use a column size below 3, the widget is not guaranteed to display correctly for all screen widths. Currently, there are no plans to improve support for smaller column sizes. We suggest you use a column size of 3 or higher moving forward.

![My active items widget showing the summary view at the top and the list view at the bottom of the widget.](../images/my-active-items-widget.png "My active items widget items")

To change the display options, see [Perform an advanced activity configuration](../task/configure-my-activity.md).

## Summary view

The summary view displays a count of all the activities. The count for the primary activity is shown at the top of the widget. The count for the non-primary activities is shown after that. For example, tasks \(9 Tasks\) is the primary activity and requests \(9+ Requests\) is the non-primary activity. If the number of activities is zero, the summary view displays **0** next to the activity name. For example, if there are zero tasks, then the summary view displays 0 Tasks. If the count of tasks exceeds 9 in number, the summary view displays 9+ next to the activity name. For example, If there are 10 tasks, then the summary view displays 9+ Tasks.

Clicking an activity in the widget opens the page that you specified in the **Internal Link** field of the Activity Configuration form.

## List view

The list view displays a list of to-dos only for the primary activity. If you set the Tasks activity as primary, the list view displays to-dos only for the Tasks activity. The **View All** option opens the page you have configured for the primary activity.

You can do an advanced configuration or a basic configuration for an activity. Use the out-of-the-box **Approvals action group** to display the actions such as **Approve** and **Reject**.

**Note:** When you do not associate an action group with the tasks, the **View details** option appears to navigate to the activity details page.

For more information, see [Action framework](action-group-framework.md).

**Note:** For actions to appear in my items widget, you can add the OOTB **Approvals action group** from **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configurations**, click an existing to-dos configuration, navigate to the **To-do Configuration Details** record, and use the OOTB action group under **Fields Mapping**.

**Related topics**  


[Perform a basic activity configuration](../task/configure-my-basic-activity.md)

[Perform an advanced activity configuration](../task/configure-my-activity.md)

