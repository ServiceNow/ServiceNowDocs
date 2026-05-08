---
title: Configure a contextual link to Virtual Agent
description: Use Mobile App Builder to create a contextual link in your mobile application so that your users can connect to Virtual Agent and receive information that pertains to their issues. By using a contextual link, your users automatically receive the information that you define about the relevant record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a contextual link to Virtual Agent

Use Mobile App Builder to create a contextual link in your mobile application so that your users can connect to Virtual Agent and receive information that pertains to their issues. By using a contextual link, your users automatically receive the information that you define about the relevant record.

## Before you begin

Role required: admin

Before you can create a virtual link to a Virtual Agent feature, you must have the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) installed on your instance. For more details, see Virtual Agent.

Perform the following steps in Mobile App Builder.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Functions** category, and then select **New**.

4.  Select the **Action Item**, and then select **New**.

5.  Complete the following fields as needed.

<table id="table_lvf_xd1_n2b"><thead><tr><th>

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

Use current record as a condition

</td><td>

Whether you want a separate set of query conditions for the action item. If selected, the Query conditions field is disabled. For update or delete actions, you must define the record you are updating or deleting by providing a Sys ID. Marking **Use current record as condition as true** allows you to do this without creating a parameter.

</td></tr><tr><td>

Execution script

</td><td>

The script executed by the action. This field only appears if you select **Script** as the type. For more information, see the example below.

 To make use of an input from an input form screen in your scripts, use `parm_input.<InputName>`

 To make use of a variable from an input form screen in your scripts, use `parm_variable.<VariableName>`.

</td></tr><tr><td>

Data

</td><td>

The table the action item applies to. For example, Incident.

</td></tr><tr><td>

Field Values

</td><td>

Determine the field values for an action. For example, if you want to create an action that updates an incident with a state of Resolved, use the field values State = Resolved. You can also create parametrized items to pass into the field value.

</td></tr><tr><td>

Input form screen

</td><td>

Select an input form screen to use for this action item. See [Configure an input form screen](parameter-screen-config.md).

</td></tr><tr><td>

Data parameters

</td><td>

Determines the information you are passing into the action to ensure you are changing the correct record and to enforce required fields as needed.

</td></tr><tr><td>

Action item step

</td><td>

Allows an action item to perform multiple processes.

 For more information, see [Configure action steps within an action item](configure-action-steps.md).

</td></tr></tbody>
</table>6.  Select **Save**.


-   **[Create UI parameters for your Virtual Agent link](sg-av-context-2.md)**  
Create UI parameters to pass information from your record into Virtual Agent so that your users get the information they need for their issues.
-   **[Enable Virtual Agent for mobile applications](sg-mobile-virtual-agent.md)**  
Give your users the ability to chat with a virtual agent through a ServiceNow mobile application.

