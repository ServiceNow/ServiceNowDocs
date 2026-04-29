---
title: Add a new change request type
description: You can add a new change type to your change process. There are several processes involved with adding a change type. These processes include managing script includes and workflows.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Add a new change request type

You can add a new change type to your change process. There are several processes involved with adding a change type. These processes include managing script includes and workflows.

## Before you begin

Role required: admin

## About this task

In addition to the three types of change available by default, you can add new change types based on your organization requirements. For example, you can create a change type **Expedited** for changes that you require to be processed immediately.

## Procedure

1.  Complete the following steps to add a new choice to the **Type** field.

    1.  Open an existing change request.

    2.  Right-click the **Type** field and select **Show Choice List**.

    3.  Click **New** and fill in the following fields.

        |Field Name|Description|
        |----------|-----------|
        |Table|Select the **Change Request** table.|
        |Label|Enter a value for the new change type. For example, `Expedited`.|
        |Value|Enter a value for the new change type. For example, `expedited`.|
        |Sequence|Enter a sequence for the change type. For example, `4`.|

    4.  Submit the form.

2.  Complete the following steps to add the new change type to the change request interceptor.

    1.  Navigate to **System Definition** &gt; **Interceptors**.

    2.  Open the **Change Request** interceptor.

    3.  Click **New** in the **Answers** related list.

    4.  Complete the form, as appropriate.

        |Field|Description|
        |:----|:----------|
        |Question|Change Request|
        |Name|Enter a name for the new change type. For example, `Direct to Expedited Change`.|
        |User Prompt|Enter a description that is displayed to the end user when they click **Create New** under **Change**.|
        |Target URL|Set the appropriate target URL. For example, `change_request.do?sys_id=-1&sysparm_query=type=expedited`.|
        |Order|Set the appropriate order level for the change type. For example, `400`.|

    5.  Submit the form.

3.  Complete the following steps to create the script include for the new change type.

    1.  Navigate to **System Definition** &gt; **Script Includes**.

    2.  Search for a change type script include on which to base the workflow for the new change type.

        For example, to base it on Emergency change type, search for ChangeRequestStateModelSNC\_emergency and open the script include.

    3.  Copy the script of the ChangeRequestStateModelSNC\_emergency script include from the **Script** field.

    4.  Navigate to **System Definition** &gt; **Script Includes** and click **New**.

    5.  Name the new script include to match the value of the new type.

        For example, ChangeRequestStateModelCust\_expedited.

    6.  Paste the copied script in the **Script** field of the new script include.

    7.  Update any references in the pasted script include from ChangeRequestStateModelSNC\_emergency to ChangeRequestStateModelCust\_expedited.

    8.  Click **Submit**.

        **Note:** An existing script include contains the implementation for all the *moving* and *canMove* functions. The *moving* function is used to pre-populate any fields that are required for the new state. The *canMove* function is used to check for any additional requirements and to validate whether a task can move to the next state.

4.  Complete the following steps to create the script include to define state transitions and control the transitioning between states for the new change type.

    1.  Navigate to **System Definition** &gt; **Script Includes**.

    2.  Search for change type script include on which to base the transitioning controls for the new change type on.

        For example, to base it on Emergency change type, search for ChangeRequestStateModel\_emergency and open the script include.

    3.  Update the name of the script include to match the value of the new type.

        For example, ChangeRequestStateModel\_expedited.

    4.  Update the reference to the base script include for the new change type as created in step 3.

        Change the extended Object in line 2 to the base script include name. For example, ChangeRequestStateModelCust\_expedited, so the reference is similar to the following string.

        `ChangeRequestStateModel_expedited.prototype = Object.extendsObject(ChangeRequestStateModelCust_expedited,`

        Ensure that the reference of the type is similar to the script include that is created. For example, `type:"ChangeRequestStateModel_expedited"});`. The type is present at the bottom of the script.

    5.  Click **Insert and Stay** create a copy of the script include ChangeRequestStateModel\_emergency with the new name ChangeRequestStateModel\_expedited.

5.  Complete the following steps to modify the script include that controls the transition between states using one of the defined models for the new change type.

    1.  Navigate to **System Definition** &gt; **Script Includes**.

    2.  Search for and open the ChangeRequestStateHandler script include, which controls the transitioning between states using one of the defined models.

    3.  Create a property to reference the new change request type value.

        For example, *EXPEDITED:"expedited"*.

    4.  Override the base method *\_resetModel* to be able to include the new model.

        For example, if the change request type is *expedited*, then the new state model ChangeRequestStateModel\_expedited is included. You must include the string EXPEDITED:"expedited" after initialize: function\(changeRequestGr\) \{ as shown in the screen.

    5.  Save the script include.

6.  Complete the following steps to create a workflow for the new change request type.

    1.  Navigate to **Workflow** &gt; **Workflow Editor**.

    2.  Open an existing change request workflow.

        For example, **Change Request – Emergency**.

    3.  Select **Copy** from the **Actions** menu to copy the workflow and name the new workflow.

        For example, `Change Request - Expedited`.

    4.  Select **Properties** from the **Actions** menu to update the condition under which the new workflow executes.

        For example, **\[Type\] \[is\] \[Expedited\]** in the condition.

    5.  Open the matching change tasks workflow that is called by the main workflow.

        For example, **Change Request - Emergency change tasks**.

    6.  Select **Copy** from the **Actions** menu to copy the workflow and name the new workflow.

        For example, `Change Request - Expedited change tasks`.

    7.  Select **Publish** from the **Actions** menu to publish the new change tasks workflow and make it available for use.

    8.  Go back to the first workflow you created and update the Workflow activity to reference the new change tasks workflow.

        For example, **Change Request - Expedited change tasks**.

    9.  Select **Publish** from the **Actions** menu to publish the new workflow and make it available for use.


**Parent Topic:**[Configuring Change Management](../concept/configure-change-management.md)

**Related topics**  


[Change types](../concept/change-types.md)

[Add a state to the state model](t_AddANewState.md#)

