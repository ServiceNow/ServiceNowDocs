---
title: Managing SPM work in Collaborative Work Management
description: Team members can view and update project tasks and demand tasks directly in Collaborative Work Management \(CWM\) using team member roles, without requiring access to Project Workspace or Next Experience for Demand Management.
locale: en-US
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 2
keywords: [team member, project tasks, collaborative work management]
breadcrumb: [Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Managing SPM work in Collaborative Work Management

Team members can view and update project tasks and demand tasks directly in Collaborative Work Management \(CWM\) using team member roles, without requiring access to Project Workspace or Next Experience for Demand Management.

Collaborative Work Management application provides roles that give team members access to project tasks and demand tasks within CWM. Using these roles, team members can manage their assigned work through CWM features such as My Work and Connected Work ad submit time card against the project tasks and demand tasks.

## Team member roles

The following roles are available for team members:

-   **Team member read \[sn\_stm.team\_member\_read\]**

    Allows users to view project tasks and demand tasks, and leave comments on them.

-   **Team member read-write \[sn\_stm.team\_member\_read\_write\]**

    Allows users to view and edit project tasks and demand tasks.


**Note:** Assigning one of these team member roles automatically grants the CWM user role \[sn\_cwm.cwm\_user\] and Time card user role \[timecard\_user\].

## Accessing project and demand tasks in CWM

After a team member role is assigned, users can view and manage project and demand tasks in CWM through the following features:

-   **My Work**: View all project and demand tasks assigned to you in one place. For more information, see [My Work in CWM](my-work-in-cwm.md).

-   **Connected Work**: Pull project and demand tasks into CWM Boards using flexible filters, such as tasks assigned to you, your assignment group, or other criteria. You can edit and update tasks directly from the board.

    For more information, see [Connected work in CWM](unified-boards-for-connected-work-in-cwm.md)


By default, team member roles provide broad access to the tasks assigned to them. Administrators can configure additional ACLs to restrict access to specific tasks.

## Accessing My Calendar

Users assigned these team member roles can access My Calendar and perform the following actions:

-   View My calendar
-   Edit My calendar
-   Create Events on calendar
-   Delete their own events

## Considerations

The following limitations apply to team member roles in this release:

-   Team member roles don't grant access to Project Workspace or Next Experience for Demand Management.

-   The SPM applications such as Project Workspace and Next Experience for Demand Management must be present in your ServiceNow AI Platform instance for team members to be able to access those work items from CWM.

-   The Timecard Management application must be installed to for team members to create timecards against their project tasks or demand tasks.

**Parent Topic:**[Using Collaborative Work Management](using-collaborative-work-management.md)

