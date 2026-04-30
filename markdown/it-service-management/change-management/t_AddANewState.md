---
title: Add a state to the state model
description: You can add a new state to the existing state model for different change types based on the requirements of your organization.Any modification to the state model may impact the default workflows for change requests.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [State model and transitions, Configure, Change Management, IT Service Management]
---

# Add a state to the state model

You can add a new state to the existing state model for different change types based on the requirements of your organization.

## Before you begin

Role required: script\_include\_admin, ui\_policy\_admin, ui\_action\_admin, or admin

## About this task

The [State model](t_ActivateStateModel.md) plugin is activated by default. For more information about base system states for change requests, see [State model and transitions](../concept/c_ChangeStateModel.md).

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Create New** and complete the following steps to add a choice to the choice list.

    1.  Right-click the **State** field and click **Configure dictionary**.

    2.  In the **Choices** related list, run a filter for **\[Table\] \[is\] \[change\_request\]**.

    3.  Click **New** and add the new state with the following information.

        -   **Table**: Change Request \[change\_request\]
        -   **Label**: name of your new state
        -   **Value**: numerical value that is not already assigned to an existing state choice
        -   **Sequence**: number corresponding to the location for it to appear in the list of states. If you assign it the same sequence number as another choice, it appears below the other choice.
    4.  Click **Submit**.

2.  Navigate to **System definition** &gt; **Script includes**.

    Script include records that contain **SNC** in the name are read-only. As you complete the following steps, ensure that you are selecting the correct script include to modify. For example, modify **ChangeRequestStateHandler** not **ChangeRequestStateHandlerSNC**.

    **Note:** Extended script includes \(without **SNC**\) include all of the functionality of their SNC counterparts. If you modify a base script include \(appended with **SNC**\), it is no longer updated during system upgrades.

3.  Open the **ChangeRequestStateHandler** script to perform the following edits.

    -   Update the **statehandler constants** section at the start of this script include to include values for the newly added state. For example:

        ```
        ChangeRequestStateHandler.MY_NEW_STATE = "mynewstate";
        ```

    -   Update the **STATE\_NAMES** map at the end of the initialize function to include the numeric value for the newly added state. For example:

        ```
        this.STATE_NAMES["-6"] = ChangeRequestStateHandler.MY_NEW_STATE;
        ```

        **Note:** The **STATE\_NAMES** map provides a mapping between the numeric values that are stored in the **State** field on a change request under a memorable name. This mapping enables the memorable name to be used in the state model script includes.

4.  Edit the appropriate script include to incorporate the new states into the model for the relevant change request types.

    Each type of change request has a corresponding script include named**ChangeRequestStateModel\_&lt;type&gt;** where **&lt;type&gt;** is the value of the change request type. For example, **ChangeRequestStateModel\_normal** defines the state model for change requests with a type of normal.

    Each state model script include defines objects that specify the following information.

    -   Which states are available.
    -   The next state or states for each available state.
    -   Functions for each state transition to decide whether that transition is available `(canMove)` along with a function to be executed as part of moving to that state `(moving)`.
    The following example is from the **ChangeRequestStateModel\_normal** script include.

    ![changing the change request state script](../image/state-script-normal.png)

5.  Create a UI action to provide a button to progress the change request to the new state.

    1.  Use **Insert and Stay** to make a copy of one of the default UI actions, such as **implement**.

    2.  Update the following fields on the form.

<table id="table_rgn_wmq_nv"><thead><tr><th>

Field name

</th><th>

Update

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Update to match the name of the new state.

</td></tr><tr><td>

Action name

</td><td>

Replace the state at the end of the name with the new state.

</td></tr><tr><td>

Hint

</td><td>

Update the text to refer to the new state.

</td></tr><tr><td>

Onclick

</td><td>

Rename the function to match the new state.

</td></tr><tr><td>

Condition

</td><td>

Update the call to the `isNext` function with the new state.

</td></tr><tr><td>

Script

</td><td>

-   Update the function name to match the one specified in the **Onclick** field.
-   Update the line that starts with `ga.addParam(“sysparm_state_name”,…` to enter the name of the new state as the second parameter of the `addParam` function.
-   Update the line starts with `gsftSubmit` and modify the third parameter of this function call to match the value entered in the **Action name** field.


</td></tr></tbody>
</table>        The following example uses the **Implement** UI action to show the values to update.

        ![Modified UI action](../image/ui-action-implement.png)

        The **ChangeRequestStateHandler** script include contains two functions that are used to determine if a UI action is displayed based on the current state of the change request.

        -   `isNext(stateName)`: This function only checks if the **stateName** passed as a parameter is available as a next state for the current state of the change request.
        -   `canMoveTo(stateName)`: This function performs the same check as the **isNext** function. However, it also checks the result of calling the appropriate **canMoveTo** function for the transition from the current state to the **stateName** passed as a parameter. This function is used if there are additional checks in the **canMove** functions such as checking that a field contains a particular value.
6.  Complete the following steps to update the process flow configuration to incorporate the new change state.

    The process flow is displayed at the top of the Change Request form and is configured in various process flow records.

    ![New state appears in the process flow](../image/AddNewStateProcFlow.png)

    1.  Navigate to **System UI** &gt; **Process Flow** module and filter for **\[Table\] \[is\] \[change\_request\]**.

    2.  Open a record and use **Insert and Stay** to make a copy.

    3.  Update the following fields on the form.

        |Field name|Update|
        |----------|------|
        |Name|Update to match the name of the new state.|
        |Label|Update to match the name of the new state. This value is included in the process flow at the top of the Change Request form.|
        |Order|Update this number so that the new state is in the correct sequence with the existing process flow records for other states.|
        |Condition|Update the filter to match the new state.|

    4.  Click **Update**.


## What to do next

To ensure that the new state works as expected, review the default workflows. Add the new state to the workflow as necessary.

**Parent Topic:**[State model and transitions](../concept/c_ChangeStateModel.md)

## Review default workflows

Any modification to the state model may impact the default workflows for change requests.

### Before you begin

Role required: admin

### About this task

Each change type has a default workflow. To ensure that any change to the state model has not adversely impacted workflows, you must review each of the default workflows.

### Procedure

1.  Review the workflow for each `ChangeRequestStateModel_<type>` script include that has been modified.

    |Change type|Script include name|Workflow|
    |-----------|-------------------|--------|
    |Normal|ChangeRequestStateModel\_normal|Change Request - Normal|
    |Standard|ChangeRequestStateModel\_standard|Change Request - Standard|
    |Emergency|ChangeRequestStateModel\_emergency|Change Request - Emergency|

    Modifications to the default workflow for each change type depend on where the new state is added in the sequences of states.


