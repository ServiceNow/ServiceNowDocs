---
title: State model and transitions
description: Change Management offers a state model to move and track change requests through several states.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/c\_ChangeStateModel.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Configure, Change Management, IT Service Management]
---

# State model and transitions

Change Management offers a state model to move and track change requests through several states.

\[Omitted image "change-state-model.png"\] Alt text: State transitions in a normal change request

The following table lists the states that a change request can progress through. Email notifications can be sent to the user who requested the change when it progresses to the following states: **Scheduled**, **Implement**, **Review**, and **Canceled**.

<table id="table_stq_kft_zs"><thead><tr><th>

State

</th><th>

Description

</th><th>

State value

</th></tr></thead><tbody><tr><td>

New

</td><td>

Change request is not yet submitted for review and authorization. A change requester can save a change request as many times as necessary while building out the details of the change before submission.

</td><td>

-5

</td></tr><tr><td>

Assess

</td><td>

Peer review and technical approval of the change details take place during this state.

</td><td>

-4

</td></tr><tr><td>

Authorize

</td><td>

Change Management and the CAB schedule the change and provide final authorization to proceed.

</td><td>

-3

</td></tr><tr><td>

Scheduled

</td><td>

The change is fully scheduled and authorized, and is waiting for the planned start date. An email notification is sent to the user who requested the change.

</td><td>

-2

</td></tr><tr><td>

Implement

</td><td>

The planned start date has approached and the actual work to implement the change is being conducted. An email notification is sent to the user who requested the change.

</td><td>

-1

</td></tr><tr><td>

Review

</td><td>

The work has been completed. The change requester determines whether the change was successful. A post-implementation review can be conducted during this state. An email notification is sent to the user who requested the change.**Note:** You cannot cancel the change request if it is in the Review state.

</td><td>

0

</td></tr><tr><td>

Closed

</td><td>

All review work is complete. The change is closed with no further action required.

</td><td>

3

</td></tr><tr><td>

Canceled

</td><td>

A change can be canceled at any point when it is no longer required. However, a change cannot be canceled from a **Closed** state. An email notification is sent to the user who requested the change.

</td><td>

4

</td></tr></tbody>
</table>Normal, standard, and emergency changes progress through states in different ways.

## State progress for different changes

-   Normal changes progress through all states.
-   Standard changes are considered to be pre-authorized, so they bypass the **Assess** and **Authorize** states that trigger approval records. Approving these changes progresses the change to the next appropriate state. Rejecting these changes sends them back to the **New** state.
-   Emergency changes are similar to standard changes, except that they must be authorized.

## Reverting a change request to the New state

You can revert emergency and normal change requests to the New state, which is the first approval state, by using the **Revert to New** action in the form context menu. Use this action when approval was requested but the submitter recognizes that some configuration items in the scope of the change weren't included.

-   To modify the Normal change request to the New state, modify the state of a change request from **Assess** state to **New** state by selecting **Revert to New** from the form context menu.
-   To modify the Emergency change request to the New state, modify the state of a change request from **Authorized** state to **New** state by selecting **Revert to New** from the form context menu.

    **Note:** When you revert to **New** from the **Assess** state or the **Authorized** state, the workflow is restarted and all pending approvals are canceled.


## Modifying the change request type

-   An ACL for change\_request.type enables you to modify the **Type** field of a change request when the change request is in the **New** state and has no approvals.
-   For a **Standard** change request, you can modify the type of the change request from Standard to **Normal** or **Emergency**, if the state of a change request is **New**.
-   For a **Normal** or **Emergency** change request, you can modify the type of the change request from **Normal** to **Emergency** or vice versa if the state of a change request is **New**.
-   If a **Normal** or **Emergency** change request is rejected, the state of the change request is set to **New**. Because the change request is in the **New** state, you can modify the type of the change request again. For example, if your **Emergency** change request is rejected because it is actually a **Normal** change, modify the **Type** to **Normal**. Then resubmit the change request.

## Disabled Cancel change action

The Cancel option for a change request in the Review state is disabled. This restricts cancelling the request when the work is complete and is waiting for review.

## Change model attributes

Change managers can require specific actions when a change request moves to a specific state. Attributes assigned to that state determine what actions can take place.

By default, there are two attributes to manage a change request:

-   allow\_ci\_modification – Allows to modify the CI. Attributes are only considered if they are included in a model. If the `allow_ci_modification` attribute is not added to a model, it defaults to its initial state.
-   allow\_implementation – Indicates that the change will be implemented. By enabling `allow_implementation`, this feature replaces the implementation states field currently present on the Change model. Both the states listed in the implementation states field and the attribute will be respected.

-   **[Add a state to the state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_AddANewState.md)**  
Add a state to the state model for different change types to meet the requirements of your organization.
-   **[Configure state model transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ConfigStateModelTransit.md)**  
Use script includes or UI policies to configure state models and the criteria for moving change requests from one state to another.

**Parent Topic:**[Configuring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/configure-change-management.md)

