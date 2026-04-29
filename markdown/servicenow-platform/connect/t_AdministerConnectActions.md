---
title: Administer Connect actions
description: You can create or modify Connect actions to provide custom functionality in Connect Chat or Connect Support conversations.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect administration, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Administer Connect actions

You can create or modify Connect actions to provide custom functionality in Connect Chat or Connect Support conversations.

## Before you begin

**Important:**

Core UI is required to use Connect Chat. Connect Chat is not supported in Next Experience. If you turn on Next Experience, Connect Chat will no longer work. See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) for more information.

If you want to customize the icon for a Connect action, navigate to **Collaborate** &gt; **Administration** &gt; **Action Icons** to view the available icons and their class names. Note the class name of the icon you want to use.

Role required: admin

## About this task

The Connect action menu appears by the message entry field when one or more Connect actions are available for a conversation, based on defined conditions. When a user selects a Connect action, the system runs the script defined for that action.

## Procedure

1.  Navigate to **Connect** &gt; **Administration** &gt; **Actions**.

2.  Click **New** or open an existing record to edit a table.

3.  On the form, fill in the fields.

<table id="table_xzf_1sg_cv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition

</td><td>

JavaScript condition statement that must return true for the action to be available in a conversation. For example, to show the action in Connect Support conversations only, enter `conversation.type === "support"` or `conversation.table === 'chat_queue_entry'`.For information about the conversation object, see the [GlideConversation](https://www.servicenow.com/docs/access?context=c_GlideConversationAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) API reference documentation.

</td></tr><tr><td>

Hint

</td><td>

This field is not used.

</td></tr><tr><td>

Icon Class Name

</td><td>

Class name of the icon to use. To view all available icons and their class names, navigate to **Collaborate** &gt; **Administration** &gt; **Action Icons**.

</td></tr><tr><td>

Order

</td><td>

Order of the action relative to other items in the Connect action menu.

</td></tr><tr><td>

Script

</td><td>

Script to execute when the action is run. For example, to create a new incident that is based on the conversation, enter the following code:```
response.newRecord("incident",{
    short_description: conversation.document.short_description ||"",
    caller_id: conversation.document.opened_by
});
```

For information about the response object, see the [ConnectActionResponse](https://www.servicenow.com/docs/access?context=c_ConnectActionResponseAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) API reference documentation.**Note:** You can only create a Connect action that is based on a task table.

</td></tr><tr><td>

Shortcut

</td><td>

Text that triggers the action when entered after the "/" character in a conversation.

</td></tr><tr><td>

Title

</td><td>

Text that appears in the Connect action menu. The title for each Connect action should be unique.

</td></tr></tbody>
</table>
## Result

![Connect Actions form with the condition conversation.table === 'chat_queue_entry'](../image/ConnectActionsForm.png "Connect Actions form")

