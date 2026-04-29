---
title: Respond to an acknowledgement request using the Compliance Workspace
description: After you have been identified as a member of an audience to provide a policy acknowledgement, you must open and review the record in the Compliance Workspace, and then acknowledge it.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Acknowledge policy, Manage control objectives and policies, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Respond to an acknowledgement request using the Compliance Workspace

After you have been identified as a member of an audience to provide a policy acknowledgement, you must open and review the record in the Compliance Workspace, and then acknowledge it.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst

## Procedure

1.  After you have received a notification that you are required to acknowledge a policy, navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  To provide the acknowledgement, open the record in the **My pending tasks** section of the Tasks page and perform one of the following actions.

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

        If, for any reason, you do not want to respond, and the request is configured in such a way that you can opt out, click [**Request Exception**](request-policy-exception-ws.md).

    -   **Exempt**

        If the policy is approved


