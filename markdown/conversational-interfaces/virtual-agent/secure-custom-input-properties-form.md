---
title: Secure custom input properties sheet
description: Use this sheet to specify secure inputs, such as a password, in a custom input control in Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Virtual Agent, Secure, Input, Custom, Control]
breadcrumb: [Customizing Virtual Agent with custom controls, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Secure custom input properties sheet

Use this sheet to specify secure inputs, such as a password, in a custom input control in Virtual Agent.

**Important:** To implement secure \(password2\) inputs in your Virtual Agent custom control, you must adhere to the scoped application requirements in Workflow Studio. For details, see [Workflow Studio scoped application requirements for secure inputs](../concept/va-fd-app-reqs-secure-inputs.md).

## Secure custom input properties sheet

<table id="table_jmw_bn2_dmb"><thead><tr><th>

Secure custom input property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom Control Definition

</td><td>

List of custom control definitions for the controls.Select the definition that defines how the control is rendered for the channel in which it runs.

</td></tr><tr><td>

Generate Control Data Function

</td><td>

Script function that provides the data used to render the custom control. For example, if you're asking for one or more passwords, you would define the values for each password.

</td></tr><tr><td>

Transcript Function

</td><td>

Script function that provides the message recorded in the transcript. For example, a message for an input control could confirm that the control is rendered with specific data values.

</td></tr><tr><td>

Non-supported channel response message

</td><td>

Default fallback message that is displayed when a user is running the control on an unsupported channel.

</td></tr><tr><td>

Invoke Workflow Studio asset

</td><td>

The Workflow Studio action or subflow that secure inputs from the custom control can be passed into.

 For more information about Workflow Studio actions and subflows, see Actions and Subflows.

</td></tr><tr><td>

Spoke

</td><td>

Name of the scoped application that contains Workflow Studio content that is dedicated to a particular application or record type.

 For a list of default spokes, see Spokes.

</td></tr><tr><td>

Action / Subflow

</td><td>

The Workflow Studio action or subflow to be performed in the instance. The **Input mapping** and **Output mapping** areas change depending on your selection.

 For details about the action or subflow, click the link beneath your selection to view it in Workflow Studio.

</td></tr><tr><td>

Input mapping

</td><td>

Specifies the variables to be used as input to the selected action. The check boxes for secure fields \(password2 type\) are selected automatically, which makes them mandatory. If you select the check box for a String field, it will be mandatory, but not secure. Only fields that use the password2 data type are secure. For each selected field, provide the corresponding input response variable name that is specified in the action or subflow. For example, a Workflow Studio action contains an **oldPassword** input and a **newPassword** input. The input response object looks like this:

```
{ 
   “old_password”: “1234”,
   “new_password”: “5678”  
} 
```

 In this example, enter `old_password` for the **oldPassword** property, and then enter `new_password` for the **newPassword** property.

</td></tr><tr><td>

Output mapping

</td><td>

Specifies the variables to be output by the selected action. The contents of this area change according to the action you selected.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced \(optional\)

</td></tr><tr><td class="sub-head" colspan="2">

Permissions

</td></tr><tr><td>

Run as

</td><td>

Permissions to use for the action. Select one of the following options:

-   **User who initiates session**: When selected, the action runs using the same permissions that the current user has.
-   **System User**: When selected, the action runs using system privileges, some of which may be unavailable to the current user.

</td></tr><tr><td class="sub-head" colspan="2">

Hide or skip this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr><tr><td>

Allow user to skip this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip this node in the conversation. The condition must evaluate to true. You can set this field using either the condition builder or a script.

</td></tr></tbody>
</table>**Related topics**  


[bundle-crworkflow.flow-actions]

[bundle-crworkflow.subflows]

[bundle-crworkflow.password-2-data]

