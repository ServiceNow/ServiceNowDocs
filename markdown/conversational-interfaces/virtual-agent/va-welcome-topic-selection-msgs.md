---
title: Change the Virtual Agent greeting messages in the Greeting setup topic
description: The Virtual Agent greeting setup topic provides default greeting messages for your conversations. Customize these greetings by adding system properties that change the default welcome message and the top selection message prompting users to enter an issue or request.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [getgreetingmessage, define greeting, live chat automated greetings, greeting message for customers, live chat greetings, greeting words, servicenow virtual agent greeting message, facebook messenger greeting examples, custom greetings and setup servicenow]
breadcrumb: [Working with setup topics, Setting up chat experiences for Virtual Agent users, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Change the Virtual Agent greeting messages in the Greeting setup topic

The Virtual Agent greeting setup topic provides default greeting messages for your conversations. Customize these greetings by adding system properties that change the default welcome message and the top selection message prompting users to enter an issue or request.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Starting with the Orlando release, the **com.glide.cs.general.welcome\_message** and **com.glide.cs.general.top\_selection\_message** properties are no longer automatically installed with Virtual Agent. These properties define the greeting messages used in the Greeting setup topic.

In the Orlando release, the default Greeting setup topic was updated. If you upgraded from the New York release, these properties are retained so that you can continue using the original Greeting setup topic. If you want to use the updated Greeting setup topic, delete the **com.glide.cs.general.welcome\_message** and **com.glide.cs.general.top\_selection\_message** system properties that contain the original Greeting messages.

**Note:** These properties aren't present in the base system, but creating them enables you to override these messages.

For new customers, the updated Greeting setup topic \(see the following example\) is the default. If you want to change the default message text in the Greeting setup topic, add these system properties to the System Property \[sys\_properties\] table:

-   **com.glide.cs.general.welcome\_message**: Change the default welcome message
-   **com.glide.cs.general.top\_selection\_message**: Change the top selection message that displays after the welcome message

![Greeting setup topic displaying the various default greeting messages for your conversations.](../images/va-setup-msgs.png "Default messages in Greeting setup topic (starting with the Orlando release)")

## Procedure

1.  Navigate to **All**, and then enter `sys_properties.list` in the filter.

2.  Select **New** to add the **com.glide.cs.general.welcome\_message** property.

    1.  On the form, complete the following fields.

<table id="table_k4d_c1t_wlb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the system property name: `com.glide.cs.general.welcome_message`

</td></tr><tr><td>

Description

</td><td>

Enter an explanation for this property: `Welcome message`

</td></tr><tr><td>

Type

</td><td>

Select `string`.

</td></tr><tr><td>

Value

</td><td>

Enter the greeting text. For example: `How can I help you?`

</td></tr></tbody>
</table>    2.  Select **Submit**.

3.  In the System Properties table, select **New** to add the **com.glide.cs.general.top\_selection\_message** property.

    1.  On the form, complete the following fields.

<table id="table_lfb_13d_ymb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the system property name: `com.glide.cs.general.top_selection_message`

</td></tr><tr><td>

Description

</td><td>

Enter an explanation for this property: `Top selection message`

</td></tr><tr><td>

Type

</td><td>

Select `string`.

</td></tr><tr><td>

Value

</td><td>

Enter the text that specifies the next selection action that the user can make after the welcome message is presented to the user. For example: `You can enter your request below, or use the button to see everything that I can help with.`

</td></tr></tbody>
</table>    2.  Select **Submit**.


**Parent Topic:**[Working with setup topics](../concept/working-setup-topics.md)

