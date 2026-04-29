---
title: Manually create GRC issues using the Compliance Workspace
description: Using the Compliance Workspace, GRC you can manually create issues to document policy, risk, or audit observations, or to accept any GRC problems. You can also identify the source of the issue to help analyze and classify the issues.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage issues using the Compliance Workspace, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manually create GRC issues using the Compliance Workspace

Using the Compliance Workspace, GRC you can manually create issues to document policy, risk, or audit observations, or to accept any GRC problems. You can also identify the source of the issue to help analyze and classify the issues.

## Before you begin

Role required: compliance\_admin, compliance\_manager, or sn\_compliance.user

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, click the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Issues** &gt; **All issues**.

    The list displays all issues. However, the base condition to filter issues is that the Classification must be Compliance or empty, or in the case where the issue has an m2m association with an engagement, the logged-in user must be one of the three users, such as an auditor, engagement lead, or approver.

4.  Click **New**.

    For field descriptions of the Create New Issue form, see [Compliance workspace issue form](../reference/new-issue-form-compliance-ws.md).

    **Note:** Starting with Version 12.0.1 of the Policy and Compliance Management application, the minimum role for the **Assigned to** user on the Issues form is GRC Business User \[sn\_grc.business\_user\]. The minimum role for the **Issue manager** is GRC User \[sn\_grc.\_user\].

5.  Save the issue record.

    The tabs enable you to perform various tasks for remediating the issue. You can add policy exceptions and create remediation tasks. You can also view other issues, indicator results, and task SLAs related to the issue.

    **Note:** Starting with Version 12.0.1, the **Task SLAs** tab creates and displays SLAs based on the **Due date**. Notifications are sent to the issue owner and issue manager when the issue **Due date** reaches 50%, then %75, then when it breaches. If the **Assigned to** and **Due date** fields aren’t empty and the issue isn’t in the **New** state, an SLA is created for the issue.

    If the due date for the SLA changes, a new SLA is created. The SLA is completed when the issue transitions to **Closed Complete** or **Closed Incomplete**. Also, if the **Due date** or **Assigned to** fields are empty, or the state is New, the SLA is cancelled.

    Also starting with Version 12.0.1, remediation tasks can be created by users with the **Assigned to** user and issue manager, as well as any user with the [GRC Business User role](../../grc-policy-compliance-implementation/task/assign-user-roles.md).

    You can navigate to the issue record that you created and use the related lists to.

    -   Link the issue to multiple records of the same object type such as a control. For example, if there are three controls that monitor Google Cloud, Microsoft Azure cloud, and AWS cloud and there are three different issues raised for them being down, you can link all the three controls to one issue as cloud services is down.
    -   Link the issue to different objects such as controls, control objectives, policies, and engagements.
    -   Relate the issue to different type of objects.
    **Note:** If the issue is closed, then you cannot create, add, or remove any of the objects from the issue form. You can view the Control, Control objective, Authority document, Policy, Engagement related lists in the Issue Overview page. However, the UI action buttons in each of these related lists such as New, Add, and Remove are inactive.

    ![Related lists in Issue form.](../image/IssueFormRelatedLists.png "Related lists in the Issue form")

    The related lists in the issue form for each type of object where the issue can be linked helps to:

    -   Reduce the number of open related issues existing in an organization.
    -   Help identify the root cause of the issue and group similar issues.
    -   Solve one issue, which resolves the related issues.

