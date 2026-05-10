---
title: Action utility
description: Use the Action utility in a Virtual Agent topic to select the flow action properties that the node should create. The Action utility integrates Virtual Agent with the ServiceNow Workflow Studio product.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assistant Designer utilities, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Action utility

Use the Action utility in a Virtual Agent topic to select the flow action properties that the node should create. The Action utility integrates Virtual Agent with the ServiceNow Workflow Studio product.

## Action utility properties

Specify the flow action properties for the node you want to create.

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

Workflow Studio component type. Select one of the following:

-   **Action**: A reusable operation.
-   **Subflow**: An automated process that consists of a sequence of reusable actions, data inputs, and outputs.

</td></tr><tr><td>

Spoke

</td><td>

Name of the scoped application that contains Workflow Studio content that is dedicated to a particular application or record type.

 For a list of default spokes, see [Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/spokes.md).

</td></tr><tr><td>

Action/Subflow

</td><td>

The Workflow Studio action or subflow to be performed in the instance. The **Input mapping** and **Output mapping** areas change depending on your selection.

 For details about the action, click the link beneath your selection to view it in Workflow Studio.

</td></tr><tr><td>

Wait for response?

</td><td>

Toggle switch that determines whether Virtual Agent waits for a response from the specified action before continuing.

</td></tr><tr><td>

Input mapping

</td><td>

The variables to be used as input to the selected action. The contents of this area change according to the action you selected. Options may include string input, referenced records, scripts, and so forth. For options that require a password, enable the **Include a password input** toggle switch to prompt the user for a password. Secure inputs must use the password2 data type. Input is securely masked and not viewable by others.

**Note:**

If a field is locked and you can’t enter a string, the pill picker value must match the field type. For example, if the field type is document\_id, the referenced value type must also be document\_id. If no matching field exists, reference a field created in another FDIH action output or use a script.

</td></tr><tr><td>

Output mapping

</td><td>

The variables to be output by the selected action. The contents of this area change according to the action you selected.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

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
</table>## Example Action utility

![Action utility properties.](../images/flow-designer-action-properties.png)

**Parent Topic:**[Assistant Designer utilities](va-utilities.md)

