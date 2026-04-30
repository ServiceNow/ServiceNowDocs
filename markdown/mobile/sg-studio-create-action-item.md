---
title: Configure an action item
description: For an action function to work, you must create an action item to associate with the action function. Action items define what the action function is and how it works.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an action item

For an action function to work, you must create an action item to associate with the action function. Action items define what the action function is and how it works.

## Before you begin

Before creating an action item, create an action function.

Role required: admin

## About this task

Most action items use parameters.

Use action items to define what an action function does when a user uses that function. The following steps detail creating an action without parameters. To create a parametrized action item, see [Configure an action item with parameters](sg-create-action-item-param.md).

**Note:** ServiceNow mobile apps are unable to perform any actions that cannot be performed in the platform web-based interface. For example, if you use ACLs to prevent a user from closing an incident without adding a resolution code and notes, the user cannot close an incident in the app without the same requirements. Keep this in mind when creating actions, so that you can add the correct parameters.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** from the menu, and then select **New**.

4.  Select **New** in the Action item section, and then complete the following fields as needed.

<table id="table_dcb_qzh_2fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A name for the action item. You can have multiple action items with the same name. Make sure you choose a name that is easily identifiable.

</td></tr><tr><td>

Description

</td><td>

More information to help you identify the action item.

</td></tr><tr><td>

Type

</td><td>

The kind of action item. Choose from the following:-   New
-   Update
-   Delete
-   Script
-   MultiStep. For more information, see [Configure action steps within an action item](configure-action-steps.md).
Different fields appear on the action item form depending on the type of action you select.

</td></tr><tr><td>

Table

</td><td>

The table the action item applies to, for example, Incident.

</td></tr><tr><td>

Execution Script

</td><td>

The script executed by the action. This field only appears if you select **Script** as the type. For more information, see the example below.

 To make use of an input from a parameter screen in your scripts, use `parm_input.<InputName>`

 To make use of a variable from a parameter screen in your scripts, use `parm_variable.<VariableName>`

</td></tr><tr><td>

Use current record as condition

</td><td>

Whether you want a separate set of query conditions for the action item. If selected, the Query conditions field is disabled. For update or delete actions, you must define the record you are updating or deleting by providing a Sys ID. Marking **Use current record as condition** as true allows you to do this without creating a parameter.

</td></tr><tr><td>

Query Condition

</td><td>

Filter conditions that apply to the action item.

</td></tr><tr><td>

Set field values

</td><td>

Determine the field values for an action. For example, if you want to create an action that updates an incident with a state of Resolved, use the field values State = Resolved. You can also create parametrized items to pass into the field value.

</td></tr><tr><td>

Input Form Screen

</td><td>

Select an input form screen to use for this action item. See [Configure an input form screen](parameter-screen-config.md).

</td></tr></tbody>
</table>5.  Select **Save**.


## Example

The following example uses a script to assign a task to the current user, using the SMTask object. The first `if` statement checks to see that the input is a valid `wm_task` record and ends the script if it is not. The second `if` statement contains code that assigns the task to the current user, if the user has permission, as determined by the `canAssignToSelf` method. This action was done as a script rather than an update so that these checks could be included.

```
(function WriteBackAction(parm_input, parm_variable) {
	var smTask = new global.SMTask();
       var work_order_task_id = parm_variable['sys_id'];
	var wotGR = new GlideRecord("wm_task");
	if (!wotGR.get(work_order_task_id)) {
		gs.error("wot_assign_to_me write-back action - failed to find work order task");
		gs.addErrorMessage(gs.getMessage("Task assignment failed."));
		return;
	}
	
	if (smTask.canAssignToSelf(wotGR))
		smTask.assignToMe(gs.getUserID(), work_order_task_id);
	else
		gs.addErrorMessage(gs.getMessage("Not a valid task assignment."));
})(parm_input, parm_variable);
```

The following example uses a script to perform a navigation completion functionality after an action is performed. Enter `actionResult` as the function and then define `setRedirectionInfo(gr.getUniqueValue(), gr.getTableName()` to specify where to navigate to, once the action is performed.

```
(function WriteBackAction(parm_input, parm_variable, actionResult) {​
            var gr = new GlideRecord('incident');​
            gr.get(parm_variable['sys_id']);​
            gr.short_description = 'Updated by Scripted Action';​
            gs.addInfoMessage(gs.getMessage("This is the First success message"));​
            gs.addInfoMessage(gs.getMessage("This is the Second success message"));​
            gs.addInfoMessage(gs.getMessage("This is the Third success message"));​
            gr.update();​
        actionResult.setRedirectionInfo(gr.getUniqueValue(), gr.getTableName());         ​
})(parm_input, parm_variable, actionResult);
```

The following example uses a script to determine where the attachment\(s\) selected by the user in the attachment input type are stored. The script attaches the selected file to a specific incident record with the `sys_id` in the Incident \[incident\] table.

```
(function WriteBackAction(parm_input, parm_variable, actionResult) { 
var targetTableName = "incident";
var targetTableRecordSysId = "37aa099533b352102ed2923fad5c7b09";
var inputName = "input2"; // input2 stands for the input's name. The input type must be "Attachment" 
actionResult.addAttachment(inputName, targetTableName, targetTableRecordSysId);
})(parm_input, parm_variable, actionResult);

```

If you use parameters for the action item, you can call them in the script. The call in the script must match the parameter name exactly. For example, if the parameter name is wb\_wot\_reject\_work\_note, as in the first script above, you can call it in the script using `gr.work_notes = input.wb_wot_reject_work_note;`.

The following example uses a script to determine where attachments selected by the user, in the attachment input type, are stored.

```
(function WriteBackAction(parm_input, parm_variable, actionResult) { 
var targetTableName = "incident";
var targetTableRecordSysId = "37aa099533b352102ed2923fad5c7b09";
var inputName = "input2"; // input2 stands for the input's name. The input type must be "Attachment" 
actionResult.addAttachment(inputName, targetTableName, targetTableRecordSysId);
})(parm_input, parm_variable, actionResult);

```

## What to do next

Associate the action item with an action function, see [action function](sg-studio-config-action-function.md).

Associate action steps to an action item, see [Configure action steps within an action item](configure-action-steps.md).

