---
title: Service Operations Workspace for ITSM landing page
description: An agent can get quick visibility into the work assigned, view announcements, and view upcoming tasks.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Service Operations Workspace for ITSM user interface, Explore, Service Operations Workspace for ITSM, IT Service Management]
---

# Service Operations Workspace for ITSM landing page

An agent can get quick visibility into the work assigned, view announcements, and view upcoming tasks.

## Required roles

A user should have the itil role to access the landing page. A tier-1 agent is an itil user who belongs to a service desk group. A tier-2 agent is an itil user who doesn’t belong to a service desk group. For more information about redirection of tier-1 and tier-2 agents to the respective landing page, see [Redirect non-admin users to Service Operations Workspace](../task/redirect-sow-landing-page.md).

## Use cases

For examples of how people in your organization can use this landing page, see these use cases. Unless specified otherwise, various sections of the landing page are available for both tier-1 and tier-2 agents.

<table id="table_g4p_vkl_trb"><thead><tr><th>

User

</th><th>

Use case

</th></tr></thead><tbody><tr><td>

Tier-1 agent

</td><td>

-   Get quick visibility into the work assigned to the agent or the agent's team before starting the day.
-   Analyze incidents and catalog tasks that need attention and navigate to the records on which action should be taken.
-   Monitor incidents with service level agreements \(SLAs\) that have been breached or at risk, open P1 incidents, or the ones not updated in 24 hours.

 To use the features in Workforce Optimization for ITSM, see the **Explore key features in Workforce Optimization for ITSM** section.

</td></tr><tr><td>

Tier-2 agent

</td><td>

-   Get quick visibility into the work assigned to the agent and the agent's team before starting the day.
-   Analyze incidents, problems, change requests, and tasks that need attention and navigate to the records on which action should be taken.
-   View the upcoming tasks and announcements.
-   Access the recently viewed items.

</td></tr></tbody>
</table>## Header section

This section displays the greeting text and shift details of the agent. For information about how you can customize this section, see [Configure the header message on the landing page](../task/modify-greeting-text.md).

![Header section](../image/greeting-text.png "Header section")

**Note:** A tier-1 agent with the sn\_shift\_planning.agent role can navigate to the shift schedule when the Shift Planning for Configurable Workspace application \(sn\_uib\_agent\_sp\) is enabled.

![Option to navigate to the shift schedule of an agent](../image/shift-schedule-agent.png "Shift schedule of an agent")

## Overview section

From this section, an agent can get an overview of various assignments from the donuts.

**Important:**

-   A tier-1 agent can get an overview of catalog tasks and unresolved incidents assigned to the agent or the agent’s group.
-   A tier-2 agent can get an overview of problems, change requests, catalog tasks, and unresolved incidents assigned to the agent or the agent’s group.
-   A tier-1 or tier-2 agent can view tasks delegated to the agent by other users.

![Overview of PAR dashboard](../image/sow-par-db.png)

You can select the dashboard to view the data from the drop-down menu.

When an agent selects any part of the donut area, the associated records are displayed in the list view. When an agent selects the center of the donut area, all records associated with that card are displayed in a list view. From these list views, you can preview and update the record information in the workspace view for the following records by pointing to a record and selecting the preview icon \(![preview record icon](../image/inc-preview-record.png)\):

-   Incident
-   Problem
-   Interaction
-   Change
-   Request

For information about customizing this section, see [Configure the donuts in the tier 1 landing page](../task/customize-first-level-cards.md).

## Announcements section

This section notifies an agent of any announcements. The agent can view them in a list view or grid view.

For information about how you can customize this section, see [Configure the Announcements section on the landing page](../task/modify-announcements-section.md).

![Announcements section](../image/announcements.png "Announcements section")

## Upcoming section

This section reminds agents of the upcoming tasks for the same day and next day. If there’s a single record for the task type, the record opens. If there are multiple records for the task type, it opens a list of all records in a new tab.

**Note:** An agent can also view tasks delegated to the agent by other users.

<table id="table_xyl_ftk_nvb"><tbody><tr><td>

If you’re an agent using the Workforce Optimization for ITSM Service Operations Workspace, you can see links to your upcoming tasks at a glance in the **Upcoming**section. -   The **Today** tab shows tasks that you may want to attend to on the current day.
-   The **Tomorrow** tab shows tasks coming up the day after the current day.

 You can select the link to access the task.

</td><td>

![Upcoming section](../image/upcoming-section.png)

</td></tr></tbody>
</table>The following table describes the tasks displayed in this section.

<table id="table_vvf_2gj_w5b"><thead><tr><th>

Tasks

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Events

</td><td>

Number of events such as training and time off that's related to your shifts.**Note:** If you have an upcoming PTO on the day after the current day, in the **Upcoming** section, the **Today** list will display that you have an upcoming PTO the next day. If you are on PTO the current day, this list does not display that you have a PTO.

</td></tr><tr><td>

Shifts

</td><td>

Number of work shifts.

</td></tr><tr><td>

Skill review requests

</td><td>

Number of requests from your manager to review your skills.

</td></tr><tr><td>

Shift sign-ups

</td><td>

Shifts that you can sign up for that are due on the current day and the day after the current day.

</td></tr></tbody>
</table>For more information on Workforce Optimization for ITSM in Service Operations Workspace, see [Service Operations Workspace - Scheduling](itsm-sow-workspace-scheduling.md).

For information about how you can customize this section, see [Configure the Upcoming section on the landing page](../task/modify-upcoming-section.md).

## Quick links section

This section displays the configured quick links. For information about how you can customize this section, see [Add a user-specific quick link on the ITSM landing page](../task/add-quick-link.md).

![Quick links section](../image/quick-links-section.png "Quick links section")

## Explore key features in Service Operations Workspace section

It provides an onboarding experience by specifying all key features to get started with Service Operations Workspace for ITSM.

![Onboarding experience for logged-in users](../image/onboarding-sow-itsm.png "Onboarding section")

## Explore key features in Workforce Optimization for ITSM

In Service Operations Workspace, when the [Workforce Optimization for ITSM plugin](../../configurable-workforce-optimization-itsm/task/activate-configurable-workforce-optimization-itsm.md) \(sn\_wfo\_cfg\_itsm\) is enabled, you can do the tasks listed for each section in the following table.

|Section in Service Operations Workspace|Task description|
|---------------------------------------|----------------|
|**Upcoming**|View tasks for the current day and the next day.|
|**My performance**|Analyze performance targets set by your manager.|
|**My active learning section**|Monitor learning tasks that you must complete.|

**Upcoming section**

This section reminds agents of the upcoming tasks for the same day and next day. If there’s a single record for the task type, the record opens. If there are multiple records for the task type, it opens a list of all records in a new tab.

**Note:** An agent can also view tasks delegated to the agent by other users.

<table><tbody><tr><td>

If you’re an agent using the Workforce Optimization for ITSM Service Operations Workspace, you can see links to your upcoming tasks at a glance in the **Upcoming**section. -   The **Today** tab shows tasks that you may want to attend to on the current day.
-   The **Tomorrow** tab shows tasks coming up the day after the current day.

 You can select the link to access the task.

</td><td>

![Upcoming section](../image/upcoming-section.png)

</td></tr></tbody>
</table><table><thead><tr><th>

Tasks

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Events

</td><td>

Number of events such as training and time off that's related to your shifts.**Note:** If you have an upcoming PTO on the day after the current day, in the **Upcoming** section, the **Today** list will display that you have an upcoming PTO the next day. If you are on PTO the current day, this list does not display that you have a PTO.

</td></tr><tr><td>

Shifts

</td><td>

Number of work shifts.

</td></tr><tr><td>

Skill review requests

</td><td>

Number of requests from your manager to review your skills.

</td></tr><tr><td>

Shift sign-ups

</td><td>

Shifts that you can sign up for that are due on the current day and the day after the current day.

</td></tr></tbody>
</table>For information about how you can customize this section, see [Configure the Upcoming section on the landing page](../task/modify-upcoming-section.md).

For more information on scheduling in Workforce Optimization for ITSM in Service Operations Workspace, see [Service Operations Workspace - Scheduling](itsm-sow-workspace-scheduling.md).

**My active learning section**

<table id="table_urb_xvk_nvb"><tbody><tr><td>

The **My active learning** section displays up to three learning tasks, which could include learning paths and courses that are new, due soon, or overdue. These tasks are either the ones that have been assigned to you or the ones you chose to self-enroll. The tasks are sorted by the due date and they're highlighted in red when they're overdue. You can also see the remaining duration to complete a task that you can select and complete.

</td><td>

![My active learning](../image/my-active-learning.png)

</td></tr></tbody>
</table>For more information, see [Service Operations Workspace - Learning](itsm-sow-coaching.md).

**Parent Topic:**[Service Operations Workspace for ITSM user interface](service-operations-workspace-ui.md)

