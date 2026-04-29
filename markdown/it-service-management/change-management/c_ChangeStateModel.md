---
title: State model and transitions
description: Change Management offers a state model to move and track change requests through several states.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Change Management, IT Service Management]
---

# State model and transitions

Change Management offers a state model to move and track change requests through several states.

![State transitions in a normal change request](../image/change-state-model.png "Example of state transitions for a normal change request")

The following table provides a list of all the states that a change request can progress through. Email notifications can be sent to the user who requested the change when it progresses to the following states: **Scheduled**, **Implement**, **Review**, and **Canceled**.

<table id="table_stq_kft_zs"><thead><tr><th>

State

</th><th>

Description

</th><th>

State value

</th></tr></thead><tbody><tr><td>

New

</td><td>

Change request is not yet submitted for review and authorization. A change requester can save a change request as many times as necessary while building out the details of the change prior to submission.

</td><td>

-5

</td></tr><tr><td>

Assess

</td><td>

Peer review and technical approval of the change details are performed during this state.

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

The planned start date has approached and the actual work to implement the change is being conducted. An email notification is sent to the user, who requested the change.

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
-   Standard changes are considered to be pre-authorized, so they bypass the **Assess** and **Authorize** states that trigger approval records. Approving these changes progress the change to the next appropriate state. Rejecting these changes send them back to **New** state.
-   Emergency changes are similar to standard changes, except that they must be authorized.

## Revert a change request to a New change

Change Management allows the Emergency and Normal change types to be reverted to the new state which is the first approval state using the **Revert to New** action from the **Context** Menu. This action is performed if the approval was requested and the submitter recognizes that not all configuration item in the scope of the change is included before submitting for approval.

-   To modify the Normal change request to the New state, modify the state of a change request from **Assess** state to **New** state by clicking **Revert to New** from the Context menu.
-   To modify the Emergency change request to the New state, modify the state of a change request from **Authorized** state to **New** state by clicking **Revert to New** from the Context menu.

    **Note:** When you revert to **New** from the **Assess** state or the **Authorized** state, the workflow is restarted and all pending approvals are cancelled.


## Modify change request type

-   A new ACL for change\_request.type has been added that allows modification of the **Type** field in change request when the change request is in a **New** state and no approvals have been generated yet for it.
-   In case of **Standard** change request, you can modify the type of the change request from Standard to **Normal** or **Emergency**, if the state of a change request is **New**.
-   In case of **Normal** or **Emergency** change request, you can modify the type of the change request from **Normal** to **Emergency** or vice versa if the state of a change request is **New**.
-   If a **Normal** or **Emergency** change request is rejected, the state of the change request is set to **New**. As the state of the change request is **New**, you can modify the type of the change request again. For example, if your **Emergency** change request is rejected on the grounds that the change request is **Normal**, you can modify the **Type** of the change request to **Normal** and resubmit the change request.

## Disabled Cancel change action

The Cancel option for a change request in the Review state is disabled. This restricts cancelling the request when the work is complete and is waiting for review.

## Change model attributes

The Change Manager has the option to mandate specific actions when a Change Request is moved to a specific state. Attributes assigned to that state determine what actions can take place.

By default, there are two attributes to manage a change request:

-   allow\_ci\_modification – Allows to modify the CI. Attributes are only considered if they are included in a model. If the `allow_ci_modification` attribute is not added to a model, it defaults to its initial state.
-   allow\_implementation – Indicates that the change will be implemented. By enabling `allow_implementation`, this feature replaces the implementation states field currently present on the Change model. Both the states listed in the implementation states field and the attribute will be respected.

-   **[Add a state to the state model](../task/t_AddANewState.md#)**  
You can add a new state to the existing state model for different change types based on the requirements of your organization.
-   **[Configure state model transitions](../task/t_ConfigStateModelTransit.md)**  
You can use script includes or UI policies to configure state models and the criteria for moving change requests from one state to another.

**Parent Topic:**[Configuring Change Management](configure-change-management.md)

