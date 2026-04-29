---
title: Configure state model transitions
description: You can use script includes or UI policies to configure state models and the criteria for moving change requests from one state to another.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [State model and transitions, Configure, Change Management, IT Service Management]
---

# Configure state model transitions

You can use script includes or UI policies to configure state models and the criteria for moving change requests from one state to another.

## Before you begin

Role required: script\_include\_admin, ui\_policy\_admin, or admin

## Procedure

1.  Complete the following steps to add state change criteria in a script include that enables a state transition.

    1.  Navigate to **System Definitions** &gt; **Script Includes**.

    2.  Open the script include for the state transition model that you want to edit.

        |State transition model|Script include|
        |----------------------|--------------|
        |Normal|ChangeRequestStateModel\_normal|
        |Standard|ChangeRequestStateModel\_standard|
        |Emergency|ChangeRequestStateModel\_emergency|

    3.  Modify the appropriate method **canMove** method in the script include.

        For example, to add a condition for a normal change to transition from the New state to the Authorized state, modify the **draft.authorized.canMove\(\)** method in the **ChangeRequestStateModel\_normal** script include. In the script, the GlideRecord you are acting on can be referenced using the **this.\_gr** variable.

        The **canMove** method is part of a structure that defines the transitions available to the change type. The **canMove** method is contained in the **currentState.nextState.canMove\(\)** structure.

2.  Complete the following steps to use a UI policy to add new criteria for state transitions.

    1.  Navigate to **System UI** &gt; **UI Policies**.

    2.  Open a default UI policy to edit or click **New** to create a new policy.

        The following are the default UI policies.

        |UI Policy|Description|
        |---------|-----------|
        |Show|CAB fields for normal and emergency changes from the **Authorize** state and onwards.|
        |Mandatory|**Assignment Group** field.|
        |Mandatory|**Close notes** and **Code** fields when in the **Closed** state.|

        **Note:** In both of the mandatory UI policies, the state of the change request determines the mandatory fields. For **Show - CAB** fields, the type of change is also taken into account because standard changes do not require approval.

    3.  Complete and save the UI policy.


**Parent Topic:**[State model and transitions](../concept/c_ChangeStateModel.md)

