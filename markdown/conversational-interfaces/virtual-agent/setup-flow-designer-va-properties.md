---
title: Add actions or subflows to Virtual Agent topics
description: Use the Action utility to integrate ServiceNow Workflow Studio workflows in Virtual Agent topics. The Action utility node triggers the required Workflow Studio workflows used in the Virtual Agent conversation.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-07"
reading_time_minutes: 4
keywords: [Virtual Agent, Designer, Actions, Subflows, Workflow Studio, conversation, topic, utilities, conversational]
breadcrumb: [Integrating Virtual Agent with Workflow Studio workflows, Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Add actions or subflows to Virtual Agent topics

Use the Action utility to integrate ServiceNow Workflow Studio workflows in Virtual Agent topics. The Action utility node triggers the required Workflow Studio workflows used in the Virtual Agent conversation.

## Before you begin

If you don't already have a Virtual Agent topic, create one. For more information, see [Create a Virtual Agent topic](create-virtual-agent-topic.md).

Become familiar with the following features:

-   Workflow Studio concepts and tasks. For more information, see [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Virtual Agent Designer utilities, such as the Lookup utility, and the Script Action utility.

    Use these utilities to control the actions within the Virtual Agent conversation. For more information about these utilities, see [Virtual Agent Designer utilities](../reference/va-utilities.md).

-   Virtual Agent controls. You may be asked to enter any of the following:

    -   Text strings
    -   Data pills
    -   Strings with embedded data pills
    -   Scripts that return strings
    For more information, see [Virtual Agent Designer controls](../concept/virtual-agent-controls.md).


**Note:** If you have turned on and set up Now Assist in Virtual Agent, you can work with conversational actions and subflows from the Virtual Agent Designer home page. For more information on conversational actions and subflows, see [Conversational actions](https://www.servicenow.com/docs/access?context=conversational-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) and [Conversational subflows](https://www.servicenow.com/docs/access?context=conversational-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US). You can still integrate actions and subflows that are not conversational from Workflow Studio into Virtual Agent topics via Virtual Agent Designer. The following content is only relevant to actions or subflows that can't be made conversational in Workflow Studio.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, and on the home page, select the topic that you want to use.

2.  From the Utilities section of the palette, drag the Action utility icon ![Action utility icon](../images/action-icon.png) onto the canvas at the appropriate location on the conversation flow.

    The Action utility is now a node in the conversation flow, and the Action utility properties panel appears.

3.  On the properties sheet, fill in the fields.

<table id="action-utility-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

The name of this Action node.

</td></tr><tr><td>

Invoke Workflow Studio asset

</td><td>

Select one of the following Workflow Studio components:

-   **Action**: A reusable operation.
-   **Subflow**: An automated process that consists of a sequence of reusable actions, data inputs, and outputs.


</td></tr><tr><td>

Spoke

</td><td>

Name of the scoped application that contains Workflow Studio content that is dedicated to a particular application or record type.

 For a list of default spokes, see [Spokes](https://www.servicenow.com/docs/access?context=spokes&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Action/Subflow

</td><td>

The Workflow Studio action or subflow to be performed in the instance. The **Input mapping** and **Output mapping** areas change depending on your selection.

 For details about the action, select the link beneath your selection to view it in Workflow Studio.

</td></tr><tr><td>

Wait for response?

</td><td>

Toggle switch that determines whether Virtual Agent waits for a response from the specified action before continuing.

</td></tr><tr><td>

Input mapping

</td><td>

Specifies the variables to be used as input to the selected action. The contents of this area change according to the action that you selected. Options may include string input, referenced records, scripts, and so on. For options that require a password, enable the **Include a password input** toggle switch to prompt the user for a password. Secure inputs must use the password2 data type. Input is securely masked and not viewable by others.

 **Note:** The **Array.Reference** input data type in Virtual Agent Designer corresponds to the **List.\[Table\]** input data type in Workflow Studio. For more information, see [Action input and output data types](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Output mapping

</td><td>

Specifies the variables to be output by the selected action. The contents of this area change according to the action that you selected.

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

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>4.  Select **Save**.


**Parent Topic:**[Integrating Virtual Agent with Workflow Studio workflows](../concept/va-flow-designer-integration.md)

