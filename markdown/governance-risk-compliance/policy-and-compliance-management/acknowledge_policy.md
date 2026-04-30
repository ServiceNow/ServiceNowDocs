---
title: Respond to an acknowledgement request
description: After you have been identified as a member of an audience to provide a policy acknowledgement, you must open and review the record, and then acknowledge it.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Acknowledge a policy, Manage control objectives and policies, Use the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Respond to an acknowledgement request

After you have been identified as a member of an audience to provide a policy acknowledgement, you must open and review the record, and then acknowledge it.

## Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite

## Procedure

1.  After you have received a notification that you are required to acknowledge a policy, navigate to **Policy and Compliance** &gt; **Policy Acknowledgement** &gt; **My Acknowledgements**.

    ![My acknowledgement](../image/my_acknowledgement.png)

2.  To provide the acknowledgement, open the record and perform one of the following actions.

    The available options depend on how the acknowledgement request was configured.

    The available options depend on how the acknowledgement request was configured.

    -   The default status of the policy acknowledgement is **New**.
    -   The policy acknowledgement is set to **Pending Acknowledgement**, if:
        -   the policy acknowledgement has reached the time set as **Frequency**.
        -   the policy acknowledgement has reached the Valid From date, if it is the ad hoc acknowledgement
        -   you click the **Pending Acknowledgement** button to move its state manually.
    -   The policy acknowledgement is in Closed state, if:
        -   you move it manually to **Closed** state
        -   it reaches the **Valid to** date
    -   The state moves to **Cancel** if:
        -   you manually click **Cancel** button
        -   the policy exception is rejected, the acknowledgement is reset to Cancel
    Following options are available when the policy acknowledgement instance is set to different states:

    -   **Accept**

        If the policy is in compliance, click **Accept**.

    -   **Decline**

        If the policy is not in compliance and the request is configured in such a way that you are allowed to decline the request, click **Decline**.

    -   **Request Exception**

        If, for any reason, you do not want to respond, and the request is configured in such a way that you can opt out, click [**Request Exception**](../../grc-workspace-compliance/task/request-policy-exception-ws.md).


**Parent Topic:**[Acknowledge a policy](../concept/ack-policy.md)

