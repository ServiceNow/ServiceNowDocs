---
title: Configuring Time Recording for Field Service
description: Agents record time worked on tasks and activities. Time recorded entries automatically generate time cards and time sheets for approval by managers. Configuring time recording is optional, but will save Field Service agents from having to record their time manually.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring Time Recording for Field Service

Agents record time worked on tasks and activities. Time recorded entries automatically generate time cards and time sheets for approval by managers. Configuring time recording is optional, but will save Field Service agents from having to record their time manually.

The time recording feature extends the functionality of the Time card management application to Field Service Management. Agents can record time worked on tasks from the Work Order Task form and time spent on other activities, such as meetings or training, from the Time Worked form. Time worked entries automatically create time cards for each selected work category. Time cards are automatically included in a weekly time sheet.

The time recording feature also extends the functionality of the [Cost Management](https://www.servicenow.com/docs/access?context=r_CostManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US) application to Field Service Management. Managers can view and create rate types and labor rate cards and also view expense lines. Time sheets use [labor rate cards](https://www.servicenow.com/docs/access?context=c_TaskAndLaborRateCards&version=australia&pubname=australia-it-business-management&ft:locale=en-US) to determine costs.

Agents can modify the hours recorded on time cards. Once a time sheet is approved and a time card is processed, the agent can still go back and modify the time worked. The time sheet reverts to the **Pending** state and new time cards are created. If an agent adds more time worked records to an approved time sheet for the same week, a new time sheet record is created for the current week.

Managers can view time worked records, time cards, and time sheets for agents in their assignment groups, as well as approve and reject time sheets. After a time sheet is approved, the system processes the time cards and uses rate cards based on the time card category to create expense lines.

## Time Sheet policy

For users with the wm\_agent role, creating time worked records automatically creates or modifies time cards regardless of the setting for the **com.snc.time\_card.time\_worked** system property. The Time Sheet policy controls this functionality. The administrator can disable the auto creation of time cards for a specific user with the wm\_agent role by creating a separate Time Sheet policy for that user.

## Field Service view

The Time Card form and the Time Sheet form have a Field Service view. For users with the wm\_agent and wm\_manger roles, this view:

-   Removes the **Generate Time Cards** UI action.
-   Displays the **Time Worked** related list on the Time Card form.

## Configuration overview

The steps for setting up Time Recording for Field Service are:

1.  [Activate Time Recording for Field Service](../task/Activate-time-recording.md)

    Install the Time Recording for Field Service plugin \(com.snc.wm\_time\_recording\) for if you have the admin role.

2.  [Configure time recording categories for Field Service Management](../task/configure-time-categories.md)

    Create time recording categories to accurately track the work that Field Service technicians do. For example, you may want to create a category called Training if there are regular trainings technicians complete.


