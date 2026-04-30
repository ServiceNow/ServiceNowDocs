---
title: Policy dynamic approval setup with redlining
description: Set up dynamic approval configuration on a policy for which redlining is enabled.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Set up dynamic approval configuration for policy, Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Policy dynamic approval setup with redlining

Set up dynamic approval configuration on a policy for which redlining is enabled.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_manager, sn\_compliance\_ws.corporate\_compliance\_user

## About this task

A user with the sn\_compliance\_ws.corporate\_compliance\_manager role can create dynamic approval configuration and a user with the sn\_compliance\_ws.corporate\_compliance\_user role has read permission for the policy record.

To use dynamic approval for policy redlining, ensure that the redlining setup is done and the users in the approver rule have required roles for document access. When redlining is enabled, a user should have the mp\_document\_user role with either the sn\_grc.business\_user or sn\_grc.business\_user\_lite role to access the documents.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon.

3.  Navigate to **Compliance library** &gt; **My policies** and open a policy record.

    You can [create a new policy](../../grc-workspace-compliance/task/create-policy-ws.md) or open a policy record to enable the redlining feature.

4.  Select the Policy text related list to view the contents of the policy text.

    1.  Select the **Enable Word editing** button.

    2.  To create a document as a policy owner, select **Create new document** in the **Enable Word editing** list.

    3.  Enter the path to the Folder including the Folder name in the **Folder link** field in the Create a document pop-up.

    4.  Enter the name of the document in the **Document name** field.

    5.  Select **Create**.

5.  Select the **Request review** button.

6.  Select **Request**.

7.  Select the **Complete publishing checklist** button.

    You can complete the tasks in the publishing checklist. For more information on redlining, see [Policy authoring and redlining in Compliance Workspace](../concept/policy-authoring-redlining.md).

8.  Select **Save**.

9.  Select **Request approval**.

    If an active dynamic approval configuration does not have any users associated with it, it is not considered as a valid configuration. In such cases, selecting **Request approval** returns an error message: `Could not request approvals because matching approval rule could not be found. Make sure to configure appropriate approval rule for this policy here.` To rectify the error, edit the configuration and request approval again.

    The **Document access** tab displays the revised list of the users who can access the policy as described in the following example:

    1.  When the policy first moves to the **Awaiting approval** state, approval configuration is applied on the policy record. If the policy has two levels of approval, the document access is provided only to level 1 users by default. Group users of level 1 can get access through the **Request document access** UI action.
    2.  Once level 1 users approve the policy, the document access is added for level 2 users. If any user rejects the policy at level 1, it moves to the **Draft** state.
    3.  When the policy moves to the **Awaiting approval** state again, next level of approval configuration \(for example, approval configuration 2\) is applied on the policy record. In this case, all users that are common between the two levels and have access to the document, can access the policy and the document access is removed for the rest of the users.
    The **Request document access** UI action is visible to the users with the business user role and business user lite role. If any user groups do not have these user roles, they cannot access the document. The approvers have the view access or comment access in the approval state.

    **Note:** In the approval rule, the access is given to the individual users only and not to the group users. Giving access to many users in the group can lead to performance issues.

    If you are a group user, you must select **Request document access**. The group users can log in as one of the users in the group and select **Request document access**. The group users are then granted the document access and a message is displayed: `Doc access request has been raised, please refresh or try to access document in a few minutes.`

    In the approval configuration workflow, if an approver rejects the policy at any level, it moves to the **Draft** state. The **Document access** tab in the form displays a list of the users who have access to the policy with the roles and status displayed. Only level 1 users can access and review the record. When level 1 users approve the record, then the document access is provided to level 2 users, and so forth.

    When all levels are approved, the policy moves to the **Published** state.

10. In the **Policy text** tab, select **Open in Word**.

    The Word document opens up in the tab. In the **Manage access** tab of the document, you can also view the users who have permissions to view the document. The configured policy approval rule is displayed in the **Approval rule** field. The Approval levels related list displays information on the approval levels, users, and status of the approval for the policy record.

    If the policy gets rejected at any state, it is reset to the **Draft** state. Once the approvers approve the policy, it moves to the **Published** state.


**Parent Topic:**[Set up dynamic approval configuration on a policy record](../concept/dynamic-approval-config-for-a-policy.md)

