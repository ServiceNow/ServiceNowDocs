---
title: Define policy exception verification rules
description: The verification rule is used to verify the accuracy and completeness of a policy exception request prior to sending it out for approvals. You can define multiple levels of approvers for an application.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Allow policy exception requests from other applications, Policy and Compliance Management enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define policy exception verification rules

The verification rule is used to verify the accuracy and completeness of a policy exception request prior to sending it out for approvals. You can define multiple levels of approvers for an application.

## Before you begin

Role required:

-   sn\_compliance.manager to create the policy exception verification rules
-   survey\_reader to review and verify the questionnaire

## About this task

Defining verification rules is an optional step. If you do not define verification rules or define them and do not activate them, approvals from the requester's team will not be required.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policy Exceptions** &gt; **Verification Rule**.

2.  Click **New**.

    ![Verification rule](../image/verification-rule-new.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|Defaults to Verification Rule.|
    |Name|Enter a name for this approval configuration.|
    |Short description|Provide a brief description of the purpose of the configuration.|
    |Source application|Select the application for that applies to this verification rule. Only applications that have been previously added to the Integration Registry are listed.|
    |Active|If this is selected, this verification rule is active and the requester will have the option of requesting an initial approval prior to sending it to the compliance manager for approvals.|

4.  Click **Update**.

    The Approver Levels related list appears. This related list allows you to define multiple approver levels for a rule. One or more users, or a group of users can be selected as approvers for each level. Approvers must be assigned the survey\_reader role. You can make it mandatory for all selected users to approve the exception or optionally allow a single user to approve on behalf of all approvers.

    ![Approver levels](../image/approval-levels.png)

5.  Click **Submit**.

    When the policy exception record transitions to the Pending Verification state, the designated approvers are notified that their approval is required. If any fields in the policy exception request were not filled in by the requester \(for example, the Policy or Control Objective\), those fields become mandatory for the approvers. When the approvers have reviewed, completed, and approved the request, it transitions to the Analyze state and is assigned to the compliance manager for further analysis and approval.


**Parent Topic:**[Allow policy exception requests from other applications](../concept/allow-other-app-policy-except.md)

