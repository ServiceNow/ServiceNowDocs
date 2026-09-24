---
title: Create a recovery team
description: Create a recovery team from the administration menu in the BCM classic Workspace. Add users and groups, attach locations, and build parent-child relationships to organize your business continuity response structure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-recovery-team-classic-ws-admin.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a recovery team

Create a recovery team from the administration menu in the BCM classic Workspace. Add users and groups, attach locations, and build parent-child relationships to organize your business continuity response structure.

## Before you begin

Role required: sn\_bcm.core\_manager

## About this task

Recovery teams are created and managed at a global level, so you can reuse the same recovery team across multiple recovery plans and crisis events. You can add individual users, system user groups, or a combination of both to a recovery team. You can associate one or more locations with it and build a hierarchy of parent and child recovery teams to model your organizational structure.

**Note:** A separate **Recovery Teams** module is also available under **Business Continuity** &gt; **Planning**, which creates a recovery team that is local to a specific plan. This task covers the global recovery team module under **General Administration**, the same global recovery team described in [Create and manage a recovery team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-recovery-team.md).

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **General Administration** &gt; **Recovery Teams**.

    You can view the list of existing recovery teams as shown in the example.

    \[Omitted image "cm-new-recovery-teams-list-in-ws-view.png"\] Alt text: Recovery teams list with name, active status, description, locations, and domain columns.

2.  Select **New**.

    \[Omitted image "cm-create-recovery-team.png"\] Alt text: Create Recovery team form with name, description, active status, and locations fields.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the recovery team.|
    |Description|Description of the recovery team.|
    |Active|Sets the recovery team status and marks the team as active. Clear this check box to mark the recovery team as inactive. Inactive recovery teams aren't displayed in the recovery team picker on a plan or in the recovery team type on the collaboration thread.|
    |Locations|One or more locations to associate with the recovery team.|

4.  Select **Save**.

    The recovery team is saved, and the recovery team record with the **Users**, **Groups**, **Parent recovery teams**, and **Child recovery teams** tabs is displayed as shown in the example.

    \[Omitted image "cm-recovery-teams-lists.png"\] Alt text: Recovery team record with Details, Users, Groups, Parent recovery teams, and Child recovery teams tabs.

5.  On the **Users** tab, select **Add**, search for and select one or more users from the list or filtered conditions, and select **Add** again to confirm the selection.

    The selected users are added as members of the recovery team.

    **Note:** The **Department** column on the **Users** tab reflects each member's department, helping you review and confirm team composition by department.

6.  On the **Groups** tab, select **Add**, and select one or more system user groups from the list or filtered conditions, and select **Add** again to confirm the selection.

    All users who belong to a selected group are added as part of the recovery team.

7.  On the **Parent recovery teams** tab, select **New**.

    The **Create New Recovery team hierarchy** form opens with the current recovery team already set in the **Child recovery team** field.

    1.  Select a team in the **Parent recovery team** field and select **Save**.

8.  On the **Child recovery teams** tab, select **New**, select a team in the **Child recovery team** field, and select **Save**.

    If the selected team creates a duplicate or cyclic parent-child relationship, an error message is displayed and the record is not saved: `Invalid recovery team hierarchy: "<child-team>" cannot be added as a child of "<parent-team>" because it would create a cyclic dependency.`

    The recovery team hierarchy also has a maximum depth, controlled by the **sn\_bcm.recovery\_team.max\_hierarchy\_levels** system property \(default: 10 levels\). If adding a parent or child team would exceed this limit, an error message is displayed and the record is not saved. For more information about this property, see [Properties installed with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/properties-bcm.md).

9.  Select **Save**.

    The recovery team is saved with its users, groups, and parent-child relationships.


**Parent Topic:**[General administration setup for BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/set-up-bcm-bcmadmin-tasks.md)

**Related topics**  


[Create and manage a recovery team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-recovery-team.md)

[Global recovery teams and collaboration threads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/recovery-team-collaboration.md)

[Properties installed with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/properties-bcm.md)

