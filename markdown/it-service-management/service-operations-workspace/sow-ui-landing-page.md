---
title: Service Operations Workspace for ITSM for ITSM landing page
description: An agent can get quick visibility into the work assigned, view announcements, and view upcoming tasks.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Explore, Service Operations Workspace for ITSM, IT Service Management]
---

# Service Operations Workspace for ITSM for ITSM landing page

An agent can get quick visibility into the work assigned, view announcements, and view upcoming tasks.

## Roles required to access the landing page

A user should have the itil role to access the landing page. A tier-1 agent is an itil user who belongs to a service desk group. A tier-2 agent is an itil user who doesn’t belong to a service desk group. For more information about redirection of tier-1 and tier-2 agents to the respective landing page, see [Redirect non-admin users to Service Operations Workspace](../task/redirect-sow-landing-page.md).

## Use cases

For examples of how people in your organization can use this landing page, see these use cases. Unless specified otherwise, various sections of the landing page are available for both tier-1 and tier-2 agents.

<table id="table_g4p_vkl_trb"><thead><tr><th>

User

</th><th>

Use case

</th></tr></thead><tbody><tr><td>

Tier 1 agent

</td><td>

-   Get quick visibility into the work assigned to the agent or the agent's team before starting the day.
-   Analyze incidents and catalog tasks that need attention and navigate to the records on which action should be taken.
-   Monitor incidents with service level agreements \(SLAs\) that have been breached or at risk, open P1 incidents, or the ones not updated in 24 hours.

 To use the features in Workforce Optimization for ITSM, see the **Explore key features in Workforce Optimization for ITSM** section.

</td></tr><tr><td>

Tier 2 agent

</td><td>

-   Get quick visibility into the work assigned to the agent and the agent's team before starting the day.
-   Analyze incidents, problems, change requests, and tasks that need attention and navigate to the records on which action should be taken.
-   View the upcoming tasks and announcements.
-   Access the recently viewed items.

</td></tr></tbody>
</table>## Landing page sections

<table id="table_c4t_lwj_zdc"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Header

</td><td>

This section displays the greeting text and shift details of the agent. For information about how you can customize this section, see [Configure the header message on the landing page](../task/modify-greeting-text.md).The image on the banner of the header section in the SOW landing page supports custom themes for a more personalized experience.For more information, see [Configure the space man on the landing page](../task/modify-space-man-landing-page.md).

The alert notification displayed on the banner of the pages in SOW is expanded automatically to adjust and fit the complete message. For more information, see [Configure the header message on the landing page](../task/modify-greeting-text.md).

![Header section](../image/greeting-text.png "Header section")

**Note:** A tier-1 agent with the sn\_shift\_planning.agent role can navigate to the shift schedule when the Shift Planning for Configurable Workspace application \(sn\_uib\_agent\_sp\) is enabled.

![Option to navigate to the shift schedule of an agent](../image/shift-schedule-agent.png "Shift schedule of an agent")

</td></tr><tr><td>

Overview

</td><td>

From this section, an agent can get an overview of various assignments from the donuts.

 **Important:**

-   A tier-1 agent can get an overview of catalog tasks and unresolved incidents assigned to the agent or the agent’s group.
-   A tier-2 agent can get an overview of problems, change requests, catalog tasks, and unresolved incidents assigned to the agent or the agent’s group.
-   A tier-1 or tier-2 agent can view tasks delegated to the agent by other users.

 When an agent selects any part of the donut area, the associated records are displayed in the list view. When an agent selects the center of the donut area, all records associated with that card are displayed in a list view. From these list views, you can preview and update the record information in the workspace view for the following records by pointing to a record and selecting the preview icon \(![preview record icon](../image/inc-preview-record.png)\):

-   Incident
-   Problem
-   Interaction
-   Change
-   Request

 For information about customizing this section, see [Configure the donuts in the tier 1 landing page](../task/customize-first-level-cards.md).

</td></tr><tr><td>

Announcements

</td><td>

This section notifies an agent of any announcements. The agent can view them in a list view or grid view.

 For information about how you can customize this section, see [Configure the Announcements section on the landing page](../task/modify-announcements-section.md).

 ![Announcements section](../image/announcements.png "Announcements section")

</td></tr><tr><td>

Upcoming

</td><td>

This section reminds agents of the upcoming tasks for the same day and next day. You can select the link to access the task.If there’s a single record for the task type, the record opens. If there are multiple records for the task type, it opens a list of all records in a new tab.

**Note:** An agent can also view tasks delegated to the agent by other users.

 ![Upcoming section](../image/upcoming-section.png)

 -   The **Today** tab shows tasks that you may want to attend to on the current day.
-   The **Tomorrow** tab shows tasks coming up the day after the current day.

 When the [Workforce Optimization for ITSM plugin](../../configurable-workforce-optimization-itsm/task/activate-configurable-workforce-optimization-itsm.md) \(sn\_wfo\_cfg\_itsm\) is activated, you can also view your upcoming shift information and the following tasks are displayed in this section:

-   Events: Number of events such as training and time off that's related to your shifts.

**Note:** If you have an upcoming PTO on the day after the current day, in the **Upcoming** section, the **Today** list will display that you have an upcoming PTO the next day. If you are on PTO the current day, this list does not display that you have a PTO.

-   Shifts: Number of work shifts.
-   Skill review requests: Number of requests from your manager to review your skills.
-   Shift sign-ups: Shifts that you can sign up for that are due on the current day and the day after the current day.

 For more information on Workforce Optimization for ITSM in Service Operations Workspace, see [Service Operations Workspace - Scheduling](itsm-sow-workspace-scheduling.md).

 For information about how you can customize this section, see [Configure the Upcoming section on the landing page](../task/modify-upcoming-section.md).

</td></tr><tr><td>

Quick links

</td><td>

This section displays the configured quick links. For information about how you can customize this section, see [Add a user-specific quick link on the ITSM landing page](../task/add-quick-link.md).

 ![Quick links section](../image/quick-links-section.png "Quick links section")

</td></tr><tr><td>

Explore key features in Service Operations Workspace

</td><td>

It provides an onboarding experience by specifying all key features to get started with Service Operations Workspace for ITSM.

 ![Onboarding experience for logged-in users](../image/onboarding-sow-itsm.png "Onboarding section")

</td></tr><tr><td>

My performance

</td><td>

Analyze performance targets set by your manager.**Important:** This section is displayed only when the [Workforce Optimization for ITSM plugin](../../configurable-workforce-optimization-itsm/task/activate-configurable-workforce-optimization-itsm.md) \(sn\_wfo\_cfg\_itsm\) is activated.

</td></tr><tr><td>

My active learning section

</td><td>

Monitor learning tasks that you must complete. This section displays up to three learning tasks, which could include learning paths and courses that are new, due soon, or overdue. These tasks are either the ones that have been assigned to you or the ones you chose to self-enroll. The tasks are sorted by the due date and they're highlighted in red when they're overdue. You can also see the remaining duration to complete a task that you can select and complete.**Important:** This section is displayed only when the [Workforce Optimization for ITSM plugin](../../configurable-workforce-optimization-itsm/task/activate-configurable-workforce-optimization-itsm.md) \(sn\_wfo\_cfg\_itsm\) is activated.

![My active learning](../image/my-active-learning.png)

For more information, see [Service Operations Workspace - Learning](itsm-sow-coaching.md).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Service Operations Workspace for ITSM](explore-sow.md)

**Related topics**  


[Access Service Operations Workspace for ITSM](../task/access-sow-itsm.md)

[Service Operations Workspace for ITSM user interface](service-operations-workspace-ui.md)

[Exploring Recommended Actions for ITSM in Service Operations Workspace](exploring-recommended-actions-for-itsm-in-service-operations-workspace.md)

[Exploring On-call Scheduling in Service Operations Workspace](../task/on-call-scheduling-in-service-operations-workspace.md)

