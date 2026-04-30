---
title: Configuring quick actions
description: Quick actions are shortcuts that perform Agent Chat tasks. Agents can work more efficiently with customers by using quick actions because they don't have to enter as many characters to perform a task.Create a quick action so that agents can use shortcuts for performing actions in Agent Chat.Define a quick action parameter to allow agents to further control a quick action in Workspace chat.Configure a quick action button so that agents can perform actions in Agent Chat with a single click.Customize the quick actions that appear on the chat toolbar.Activate context quick actions to enable agents to view context relevant to a chat interaction. When launched in a chat, display cards show: sysparm\_portal, sysparm\_page, table, sys\_id, or sysparm\_language.
locale: en-US
release: xanadu
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2024-11-12"
reading_time_minutes: 9
keywords: [Configuring, quick actions, Agent Chat, Virtual Agent]
breadcrumb: [Configure, Agent Chat, Conversational Interfaces]
---

# Configuring quick actions

Quick actions are shortcuts that perform Agent Chat tasks. Agents can work more efficiently with customers by using quick actions because they don't have to enter as many characters to perform a task.

## Activate quick actions

To enable your agents to use quick actions, you must activate the and [related plugins for Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-related-plugins&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US), which is required for chat in Workspace.

## Default quick actions

The following quick actions are available by default with Workspace chat:

<table id="table_i2p_vgc_shb"><thead><tr><th>

Command name

</th><th>

Toolbar button

</th><th>

Action

</th><th>

Default parameter

</th></tr></thead><tbody><tr><td>

autopilot

</td><td>

 

</td><td>

Starts a Virtual Agent topic \(Conversation Autopilot\).

</td><td>

Available topics

</td></tr><tr><td>

help

</td><td>

 

</td><td>

Indicates to the chat supervisor that an agent needs help with a conversation. To use this quick action, new customers must enable Agent Chat and Agent Whisper and update customers must enable Agent Whisper on chat setup.

</td><td>

 

</td></tr><tr><td>

r

</td><td>

 

</td><td>

Uses [Response templates](https://www.servicenow.com/docs/access?context=response-templates-templated-snippets&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) to insert as text in a conversation.**Note:** Only response templates that have a condition of **\[Type\]\[is\]\[Chat\]** are available in Agent Chat.

</td><td>

Available response templates

</td></tr><tr><td>

search-kb

</td><td>

 

</td><td>

Starts a KB article search. The agent is prompted to search for the relevant KB article. Based on the search term the agent enters, the agent is able to view the KB articles that match the search term. The agent can then select the KB article.

</td><td>

 

</td></tr><tr><td>

ta

</td><td>

![Add user icon](../../workspace/image/add-user-icon-big.png)

</td><td>

Transfers the conversation to another agent.

</td><td>

Available agents

</td></tr><tr><td>

tq

</td><td>

![Arrow icon](../../workspace/image/arrow-icon-big.png)

</td><td>

Transfers the conversation to another queue.

</td><td>

Available queues

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Agent Chat](ci-agent-chat-configuring.md)

## Creating a quick action

Create a quick action so that agents can use shortcuts for performing actions in Agent Chat.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Quick Actions** &gt; **Actions**, and then select **New**.

2.  On the form, fill in the fields.

<table id="table_vdc_3jc_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the quick action.

</td></tr><tr><td>

Active

</td><td>

Option for activating the quick action.

</td></tr><tr><td>

Description

</td><td>

Description of the quick action.

</td></tr><tr><td>

Command Name

</td><td>

Text that triggers the quick action when entered after the forward slash \(/\) in a conversation.

</td></tr><tr><td>

Applies to

</td><td>

Work item that the quick action is available for. Filter the table that you select in the **Table** field to qualify a certain kind of work item.

 For example, to make the quick action available only for conversations that are assigned to Beth Anglin, you would first select the Interaction \[interaction\] table in the **Table**. Then, in the **Applies to** field, you would create the following filter: **\[Assigned to\] \[is\] \[Beth Anglin\]**.

</td></tr><tr><td>

Table

</td><td>

Work item table that the quick action is available for.**Note:** Quick actions are supported only in the Interaction \[interaction\] table.

</td></tr><tr><td>

Apply to all groups

</td><td>

Option for making the quick action available to all user groups.

</td></tr><tr><td>

Apply to groups

</td><td>

List of which groups can use the quick action. This field appears only if you clear the **Apply to all groups** option.

</td></tr><tr><td>

Script

</td><td>

JavaScript code to control what the quick action does.

 In this script, you have access to:

-   The *record* variable, which for Agent Chat is the Interaction \[interaction\] record
-   The *params* array, if you defined quick action parameters
 If provided, all free-form text entered after all the other parameters are captured as the last item in the *params* array.

 Set the value of *answer* as follows:

```
answer = {
                success: <Boolean>,
                message: <success_or_error_message>
};
```

 **Note:** If you do not script a message, the agent receives a default message instead.

</td></tr><tr><td>

Application

</td><td>

Application scope of the quick action.

</td></tr><tr><td>

Accepts string parameter

</td><td>

Option to indicate that the script accepts text input after any defined parameters.

</td></tr><tr><td>

Parameter label

</td><td>

Parameter name that displays next to the quick action.

</td></tr><tr><td>

Parameter hint text

</td><td>

Text that displays as a hint when the agent enters a quick action.

</td></tr></tbody>
</table>3.  Select **Submit**.


### What to do next

If your quick action requires a secondary menu, define a quick action parameter so that agents can further control the quick action. For more information, see [Define a quick action parameter](ci-quick-actions-overview.md#).

Optionally, you can make the quick action available in Agent Chat as a button. For more information, see [Configuring a quick action button](ci-quick-actions-overview.md#).

## Defining a quick action parameter

Define a quick action parameter to allow agents to further control a quick action in Workspace chat.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Quick Actions** &gt; **Parameters**, and then click **New**.

2.  On the form, fill in the fields.

<table id="table_yjf_dhf_thb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the parameter.

</td></tr><tr><td>

Action

</td><td>

Quick action that uses the parameter.

</td></tr><tr><td>

No Matching Results Message

</td><td>

Message to agents if no records match the record query. If you do not create a **No Matching Results Message**, a default message is provided.

</td></tr><tr><td>

Display value field

</td><td>

Field from the parameter record that appears in Workspace chat.

 This field appears when you select **Basic** in the **Query mode** field.

</td></tr><tr><td>

Query mode

</td><td>

Type of query. You can select **Scripted** or **Basic**. To query records with a script, select **Scripted**. To query records by whichever table that you specify in the **Table name** field, select **Basic**.

</td></tr><tr><td>

Table name

</td><td>

Table to query for parameters.

 This field appears when you select **Basic** in the **Query mode** field.

</td></tr><tr><td>

No Results Message

</td><td>

Message to agents if there are no available records to query. If you do not create a **No Results Message**, a default message is provided.

</td></tr><tr><td>

Value field

</td><td>

Field from the parameter record that agents can enter in Workspace chat to invoke the parameter item. For example, to transfer a conversation to Beth Anglin, an agent would enter `/ta "beth.anglin"`. In this case, the **User ID** field in the User \[sys\_user\] record is the **Value field**.

 This field appears when you select **Basic** in the **Query mode** field.

</td></tr><tr><td>

Query Script

</td><td>

JavaScript code to determine which records qualify for your parameter.

 You are given a *query* variable that represents the search query that the agent provided. Set the value of the *answer* variable as follows:

```
answer = {
  items: [ { value: <value>, displayValue: <displayValue>} ]
};
```

 The array of items should contain objects with a *value* and a *displayValue*.

 **Note:** This field shows only if you select **Scripted** in the **Query mode** field.

</td></tr><tr><td>

Application

</td><td>

Application scope of the parameter.

</td></tr><tr><td>

Order

</td><td>

Order that the parameter is available for the quick action.

</td></tr></tbody>
</table>3.  Click **Submit**.


## Configuring a quick action button

Configure a quick action button so that agents can perform actions in Agent Chat with a single click.

### Before you begin

Role required: admin

### About this task

The toolbar of the Workspace chat window contains three buttons. Selecting the left button \(![Paperclip icon](../image/paperclip.png)\) attaches a file in a conversation, selecting the center button \(![Arrow icon](../image/arrow.png)\) initiates a queue transfer, and selecting the right button \(![Add user icon](../image/add-user.png)\) initiates an agent transfer. You can't configure the left button, but you can assign different quick actions to the center and right buttons.

![Toolbar in the Workspace chat window](../image/chat-toolbar.png "Toolbar in the Workspace chat window")

### Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Chat Settings** &gt; **Agent Chat**.

2.  In the Agent Experience section, select **View all** next to Quick actions.

    -   To configure the arrow button \(![Arrow icon](../image/arrow.png)\), select **Transfer to Queue**.
    -   To configure the add user button \(![Add user icon](../image/add-user.png)\), select **Transfer to Agent**.
    -   To create a new button, select **New**.
3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Quick Action|Action that is performed when the button is selected.|
    |Name|Name of the quick action|
    |Use custom icon|Select this if you want to specify what image should be used for the icon|
    |Icon|Button icon that appears on the toolbar of the Workspace chat window.|
    |Active|Select if you want this quick action to be active.|
    |Application|Name of the application for which the icon display on the toolbar.|
    |Order|Position of the button on the toolbar. If the value is 100, the button appears at the center of the toolbar. If the value is 101, the button appears at the right side of the toolbar. You can't change the button order.|
    |Available on private chat tab|Select this to have the icon display on the Agent Chat toolbar.|
    |Parameter value\(s\)| |
    |Auto-submit| |
    |Apply to all groups| |

4.  Save your changes.

    -   To update an existing record, select **Update**.
    -   To create a new record, select **Save**.

## Setting up quick action toolbar controls

Customize the quick actions that appear on the chat toolbar.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select **Agent Chat** and then on the Agent Experience card, select **View All** next to Quick actions.

3.  Do one of the following:

    -   To create a quick action workspace action, select **New**.
    -   To modify a quick action workspace action, select the quick action workspace action record you want to update.
4.  On the screen, fill in the fields.

<table id="table_m12_pyk_t2b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Quick Action

</td><td>

Quick action performed.

</td></tr><tr><td>

Name

</td><td>

Name of the quick actions workspace action.

</td></tr><tr><td>

Use custom icon

</td><td>

Option to display a custom, downloaded icon in the toolbar.

</td></tr><tr><td>

Icon

</td><td>

Image to display on the toolbar when **Use custom icon** is selected. Select **Click to add...** and on the Choose an image screen, select an image file. **Note:** Use an image with a square aspect ratio.

</td></tr><tr><td>

Active

</td><td>

Indicates whether this configurable toolbar control is active.

</td></tr><tr><td>

Application

</td><td>

Application scope of the quick action.

</td></tr><tr><td>

Order

</td><td>

Value of this quick action. Quick actions are executed from lowest order to highest order, so a quick action with an order of 100 is considered before a quick action of 200.

</td></tr><tr><td>

Available on private chat tab

</td><td>

Option that defines whether the quick action is available on the private chat tab.

</td></tr><tr><td>

Applies to

</td><td>

Condition that determines when the quick action is available.

 -   Add Filter Condition- Filter the table that you select in the **Table** field to qualify a certain type of work item.
-   Add "OR" Clause- Add an "or" clause to the condition.
 For example, to make the quick action available only for conversations assigned to Beth Anglin, you select the Interaction \[interaction\] table in the **Table**. Then, in the **Applies to** field, you create the following filter: **\[Assigned to\] \[is\] \[Beth Anglin\]**.

</td></tr><tr><td>

Parameter value\(s\)

</td><td>

Parameters needed for the quick action.

</td></tr><tr><td>

Auto-submit

</td><td>

Option for the agent to select a button and have the quick action and parameter post to the chat.

</td></tr><tr><td>

Apply to all groups

</td><td>

Option for making the quick action available to all user groups.

</td></tr></tbody>
</table>5.  Select **Submit** or **Update**.


## Activating chat context quick actions

Activate context quick actions to enable agents to view context relevant to a chat interaction. When launched in a chat, display cards show: sysparm\_portal, sysparm\_page, table, sys\_id, or sysparm\_language.

### Before you begin

Role required: admin

### About this task

Context quick actions are a default quick action, but require activation.

### Procedure

1.  Navigate to **All** &gt; **Quick Actions** &gt; **Actions**.

2.  In the **Get Chat Context Variables** record, use the list editor to set the **Active** value to true.![Get Chat Context Variable record, with Active value of True highlighted.](../image/quick-actions.png)


