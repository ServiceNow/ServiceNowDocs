---
title: Configure context variables for storing chat-related information
description: Specify chat context variables, also called Live Agent chat variables, for storing chat-related information, such as pre-chat survey responses. These variables contain contextual information that can be used to determine topic intent or control how chats are routed to live agents. You can also define variables to capture contextual information passed in Virtual Agent topic scripts to share with live agents.
locale: en-US
release: zurich
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Configure context variables for storing chat-related information

Specify chat context variables, also called Live Agent chat variables, for storing chat-related information, such as pre-chat survey responses. These variables contain contextual information that can be used to determine topic intent or control how chats are routed to live agents. You can also define variables to capture contextual information passed in Virtual Agent topic scripts to share with live agents.

## Before you begin

Virtual Agent provides pre-built context variables. Before you add a variable, review the list of [available Live Agent context variables](../../virtual-agent/reference/live-agent-chat-context-vars.md).

Role required: virtual\_agent\_admin or admin

## About this task

You can use context variables in scripts or with the condition builder. For example, you can reference context variables in the **Live agent** area in the topic **Properties** tab when creating a topic. When a condition is applied to a topic, it must return as true to display to the user.

For details about using context variables in topic scripts, see [Virtual Agent scripts](../../virtual-agent/concept/virtual-agent-scripts.md). For information about learning to use context variables, see [Tutorial: Route interactions by context](../../advanced-work-assignment/task/context-routing-tutorial.md). For descriptions of Live Agent context variables, see [Live agent chat context variables](../../virtual-agent/reference/live-agent-chat-context-vars.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under **Context variables**, select **View All**.

3.  On the Context Variables page, select **New** to add a variable.

4.  On the form, fill in the fields.

<table id="table_aqv_sxv_csb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the context variable to be created.

</td></tr><tr><td>

Script Variable Name

</td><td>

Live Agent variable name, which is automatically created from the **Name**. The variable name begins with `LiveAgent`.

</td></tr><tr><td>

Table

</td><td>

Name of the ServiceNow table associated with the context variable. Select a table from the list.

</td></tr><tr><td>

Record

</td><td>

Option to associate the context variable to a record in the specified table. If you selected a table, this option is automatically selected.

</td></tr><tr><td>

Value

</td><td>

Script that determines the information stored in the context variable.

</td></tr></tbody>
</table>5.  Select **Save**.

    The context variable is now available for use.


-   **[Live agent chat context variables](../../virtual-agent/reference/live-agent-chat-context-vars.md)**  
Use chat context variables to pass certain information from the topic to share with a live agent or to control how bot conversations are routed to live agents. Virtual Agent includes some default variables, and you can define new ones.

**Parent Topic:**[General chat settings](../concept/ci-configuring-chat-features.md)

