---
title: Create and manage a recovery team
description: Create a recovery team in the Business Continuity Workspace, add users and groups, attach locations, and build parent-child relationships to organize your business continuity response structure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-recovery-team.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 3
keywords: [recovery team, business continuity management, BCM, recovery team hierarchy]
breadcrumb: [Creating global recovery teams and collaboration threads, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create and manage a recovery team

Create a recovery team in the Business Continuity Workspace, add users and groups, attach locations, and build parent-child relationships to organize your business continuity response structure.

## Before you begin

Role required: sn\_bcm.core\_manager

## About this task

Recovery teams are created and managed at a global level, so you can reuse the same recovery team across multiple recovery plans and crisis events. You can add individual users, system user groups, or a combination of both to a recovery team. You can associate one or more locations with it and build a hierarchy of parent and child recovery teams to model your organizational structure.

Starting with BCM release 12.x.x, recovery teams are managed globally rather than being local to individual recovery plans, making the same team available across all BCM applications.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Recovery teams** in the List view.

2.  View the list of existing recovery teams.

    The **Recovery teams** list is displayed as shown in the example.

    \[Omitted image "cm-new-recovery-teams-list-in-ws-view.png"\] Alt text: Recovery teams list with name, description, active status, and locations columns.

3.  To create and manage a recovery team, select **New**.

    \[Omitted image "cm-create-recovery-team.png"\] Alt text: Create Recovery team form with name, description, active status, and locations fields.

4.  Enter a name and description for the recovery team.

5.  Select the **Active** check box to set the recovery team status and mark the team as active.

    To mark a recovery team as inactive, clear the **Active** check box. Inactive recovery teams are not displayed in the recovery team picker on a plan or in the recovery team type on the collaboration thread. You can change this status at any time.

6.  In the **Locations** field, add one or more locations to associate with the recovery team.

7.  Select **Save**.

    The recovery team is saved, and the recovery team record with the **Users**, **Groups**, **Parent recovery teams**, and **Child recovery teams** tabs is displayed as shown in the example.

    \[Omitted image "cm-recovery-teams-lists.png"\] Alt text: Recovery team record with Details, Users, Groups, Parent recovery teams, and Child recovery teams tabs.

8.  On the **Users** tab, select **Add**, search for and select one or more users from the list or filtered conditions, and select **Add** again to confirm the selection.

    The selected users are added as members of the recovery team.

    **Note:** The **Department** column on the **Users** tab reflects each member's department, helping you to review and confirm team composition by department.

9.  On the **Groups** tab, select **Add**, and select one or more system user groups from the list or filtered conditions, and select **Add** again to confirm the selection.

    All users who belong to a selected group are added as part of the recovery team.

10. On the **Parent recovery teams** tab, select **New**.

    The **Create New Recovery team hierarchy** form opens with the current recovery team already set in the **Child recovery team** field.

    1.  Select a team in the **Parent recovery team** field and select **Save**.

11. On the **Child recovery teams** tab, select **New**, select a team in the **Child recovery team** field, and select **Save**.

    If the selected team creates a duplicate or cyclic parent-child relationship, an error message appears and the record is not saved: `Invalid recovery team hierarchy: "[child team]" cannot be added as a child of "[parent team]" because it would create a cyclic dependency.`

12. Select **Save**.

    The recovery team is saved with its users, groups, and parent-child relationships.


**Related topics**  


[Recovery teams, loss scenarios, and recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/recovery-teams.md)

[Creating global recovery teams and collaboration threads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/recovery-team-collaboration.md)

[Add associated plans and recovery teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-related-plans-recovery-teams-bcp-uib-ws.md)

[Create a business continuity plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-bcp-plan-in-uib-ws.md)

