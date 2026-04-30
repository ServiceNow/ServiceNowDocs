---
title: Define topic context intent configurations
description: Use pre-chat survey information to determine the appropriate Virtual Agent conversation topic automatically displayed to end users \(requesters\), rather than prompting them to choose from a list of conversation topics.
locale: en-US
release: xanadu
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using pre-chat surveys with context variables for topic discovery, General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Define topic context intent configurations

Use pre-chat survey information to determine the appropriate Virtual Agent conversation topic automatically displayed to end users \(requesters\), rather than prompting them to choose from a list of conversation topics.

## Before you begin

-   [Configure the chat context variables](ac-configure-context-variables.md) for storing user answers to specific questions in your chat surveys.
-   As you [create your chat survey](create-chat-surveys.md), map a survey question to a new or existing chat context variable. The variable stores the user response that Virtual Agent uses to determine topic context intent and the conversation topic displayed.
-   Role required: virtual\_agent\_ admin or admin

## About this task

Create a context topic intent to specify conditions that determine which Virtual Agent conversation topic is displayed after a user answers a pre-chat survey. The context topic intent uses data collected by the survey to find an appropriate topic for the user.

For example, a pre-chat survey asks the user “What problem are you having with your computer?” and maps their answer to a context variable called “problem” in the survey. The variable passes from the survey to the topic context intent. Instead of the chat going directly to topic discovery, the variable stored in the intent is used as an utterance to feed into the Virtual Agent for topic discovery.

You can define conditions in a topic context intent to limit topic discovery, such as restricting the “problem” variable in the preceding example to only feed to ITSM VA conversations. The Context Topic \[sys\_cs\_context\_topic\] table is used to map your variables for intent discovery, after the pre-chat survey has been executed.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under **Topic context intent**, select **View All**.

3.  In the Context Topic page, select **New** or the configuration to be modified.

4.  On the form, fill in the fields.

<table id="table_kvs_rwh_tjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the configuration for topic context intent \(topic discovery\).

</td></tr><tr><td>

Active

</td><td>

Option that activates this topic intent configuration.

</td></tr><tr><td>

Order

</td><td>

Order in which Virtual Agent evaluates topic intent configurations to find a matching condition for displaying the topic. Virtual Agent reviews the configuration that has the lowest order value first.

</td></tr><tr><td>

Condition mode

</td><td>

Type of condition that determines how the topic intent configuration is to be applied.

 -   Simple: Specify a condition using the condition builder.
-   Advanced: Specify a JavaScript scripted condition.


</td></tr><tr><td>

Condition

</td><td>

Condition for applying the specified context variable that displays the corresponding conversation topic. Select **Set conditions** to enter the condition filter.If no condition is specified, the specified context variable applies to all conversations.

</td></tr><tr><td>

Script\[Displayed when **Condition mode** is set to Advanced\]

</td><td>

JavaScript condition statement for applying the specified context variable that displays the corresponding conversation topic. The condition must evaluate to true.

</td></tr><tr><td>

Context

</td><td>

Chat context variable that stores the user response to a specific survey question and used to determine the topic intent.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

The context topic intent configuration is added to the Context Topic \[sys\_cs\_context\_topic\] table. Virtual Agent displays the appropriate conversation topic to users based on the context intent configuration.

**Parent Topic:**[Using pre-chat surveys with context variables for topic discovery](../concept/using-context-intent-prechat-survey.md)

