---
title: Create or modify a response template
description: Create or modify a response template \(formerly known as a templated snippet\) to define a reusable message that can be copied to case or task forms or used in Agent Chat sessions to provide quick and consistent messages to users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Response templates, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create or modify a response template

Create or modify a response template \(formerly known as a templated snippet\) to define a reusable message that can be copied to case or task forms or used in Agent Chat sessions to provide quick and consistent messages to users.

## Before you begin

Role required: sn\_templated\_snip.template\_snippet\_writer

## About this task

Each response template is associated with a table that is an extension of the Task \[task\] table or, if using Agent Workspace, the Interaction \[interaction\] table. The template can be configured to include variables pulled from that table. You can also use a condition builder to specify the conditions that a case must meet for the template to be available for use, such as for a specific HR service or for chat. For chat response templates, you specify a short name \(shortcut\) that is used with the slash command as a quick way to present the response message to a user.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Response template configuration**.

2.  Select **New** to create a response template.

    Or, select an existing response template to modify from the list.

3.  Fill in the fields on the form.

<table id="table_wtn_xd3_ldb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the response template.

</td></tr><tr><td>

Short Name

</td><td>

Short description that identifies the response template when using chat in Agent Workspace.Use the short name with a quick command \(/\) to show the text from the template body of the response template while in chat. This feature provides a fast and consistent way to populate text while in chat.

 For example, the short name `gm` identifies the chat response template for a Good Morning greeting. Enter **/gm** in a chat window to show the text from this response template.

</td></tr><tr><td>

Table

</td><td>

Name of the table that the response template is associated with.If you are creating a response template for Agent Workspace chat, the associated table is the Interaction \[interaction\] table. For other response templates, the table must be an extension of the Task \[task\] table.

 **Note:** Creating custom COE tables do not allow you to add the Copy to Clipboard UI action. Users can still use the copy and paste function.

</td></tr><tr><td>

Condition

</td><td>

Conditions that determine when the response template is available for use.When defining conditions like case sensitivity or null values, see API GlideFilter - Scoped, Global.

 **Note:** The conditions available depend on the table you select. For chat response templates, specify the condition: **\[Type\] \[is\] \[Chat\]**

</td></tr><tr><td>

Application

</td><td>

The application that created the response template.

</td></tr><tr><td>

Group visibility

</td><td>

Indicates what groups have access to the response template.Adding groups filters who can view the response template.

 **Note:** Leaving this field empty makes the response template available to all groups.

</td></tr><tr><td>

Template body

</td><td>

Text of the response template providing instructions to the agent on how to respond to a specific case or task.You can reference field values by selecting variables from the variables list based on the table you select.

 You can manually enter custom variable references:

-   Current user: `${current_user}`
-   Current date: `${Date}`
 Or, place your mouse where you want the custom variable reference to appear and select the **Insert Current User** or **Insert Current Date** buttons.

 **Note:** Response templates do not support rich text.

</td></tr><tr><td>

Select variables

</td><td>

Variables you can add to the template body. For example, if you choose the HR Case \(sn\_hr\_core\_case\) table, you can select the Subject person variable to appear in the Template body and it will replace the variable with the actual name of the subject person when the response template is used.**Note:** The variables available depend on the table you select.

</td></tr></tbody>
</table>    The following GIF shows an example of an HR manager in the HR Service Delivery application creating a response template to escalate payroll discrepancy cases. The template is associated with the HR Payroll Case \[sn\_hr\_core\_case\_payroll\] table, and a condition is set to filter on cases that match the Payroll Discrepancy HR service. The template text is pasted into the body, and then a variable for the subject person is added to the salutation.

    ![Response Template](../image/response-template.png)

    ![How you can create a response template with conditions and variables.](../image/response-template-example.gif)

4.  Click **Submit** or **Update**.

    Channels limit the response template to only the channels you add. If you leave this blank, the response template is available to no channels. This feature allows you to have different messages for chats, emails, or form. For more information, see Create a response template channel.

    The Channels related list appears.


## What to do next

You can copy response template content to any field on a form that meets the specified conditions.

The following GIF shows an example of an HR case writer in the HR Service Delivery application opening a payroll discrepancy case and copying a payroll discrepancy escalation template to the comments field in the HR case form for the employee to read.

![How you can copy response template content to a field on a case form.](../image/response-template-example-2.gif)

