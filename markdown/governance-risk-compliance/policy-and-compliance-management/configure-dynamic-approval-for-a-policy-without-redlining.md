---
title: Policy dynamic approval setup
description: Set up dynamic approval configuration on a policy. Based on the configured approval levels, the Policy and Compliance Management application configures one or more approval rules on the policy record.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up dynamic approval configuration on a policy record, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Policy dynamic approval setup

Set up dynamic approval configuration on a policy. Based on the configured approval levels, the Policy and Compliance Management application configures one or more approval rules on the policy record.

## Before you begin

Role required: sn\_compliance.manager, sn\_compliance.user

## About this task

A user with the sn\_compliance\_ws.corporate\_compliance\_manager role can create dynamic approval configuration and a user with the sn\_compliance\_ws.corporate\_compliance\_user role has read permission for the policy record.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon.

3.  Navigate to **Compliance library** &gt; **My policies** and select **New**.

4.  Enter the name of the policy.

5.  In the Policy Assignment panel, update the **Owner** and **Reviewers** fields.

6.  Select the approval method in the **Approval method** field.

    |Step|Description|
    |----|-----------|
    |**__Select approvers__**|Option to select the approvers on the policy record. You can add the approvers in the **Approvers** field.|
    |**__Use approval rule__**|Option to use the approval rule for dynamic approval configuration. Based on the setup of the approval configuration and configured approval levels, the system applies one or more approval rules on the policy record. Once an approval rule has been configured, that value is populated in the **Approval rule** field.|

    For more information on creating a policy in the Compliance Workspace, see [create a new policy](../../grc-workspace-compliance/task/create-policy-ws.md).

    **Note:** If dynamic approval configuration is not set up on the policy record, the approvers are added in the **Approval** field of the policy.

7.  In the Schedule panel, update the date for the record in the **Valid to** field.

8.  Select **Save**.

9.  Select **Request approval**.

    The policy owner can request approval and complete the workflow on the policy record. For a given approval configuration on the policy record, the system applies the configured approval rules dynamically at each approval level. Once the **Awaiting approval** state is triggered and the **Use approval rule** option is selected as the approval method, the field gets populated with the details such as the configuration being used for the approvers.

    If the policy gets rejected at any level, it is reset to the **Draft** state. When all levels are approved, the policy moves to the **Published** state.


