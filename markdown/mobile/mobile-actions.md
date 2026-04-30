---
title: Action functions
description: Action functions make changes to records on your instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Action functions

Action functions make changes to records on your instance.

Use action functions to perform tasks such as assigning a task to yourself or adding a comment to a record. Action items can optionally include an input parameter, which collects input from your user to update a record.

## Action items

Each action function includes an action item, which defines what the action function is and how it works. Learn more about action items at [Configure an action item](../task/sg-studio-create-action-item.md).

## Action function types

<table id="table_zc3_c1n_rlb"><tbody><tr><td>

Non-parametrized action function

 Actions functions allow the user to change something in the database. For example, making an update or adding a comment to a record requires an action function. Use non-parametrized action function in situations where no user input is required.

 For details on configuring these actions, see [Configure an action function](../task/sg-studio-config-action-function.md).

</td><td>

![Action function for a record assignment.](../image/action-functions-2.png)

</td></tr><tr><td>

Parametrized action function

 Use parametrized action functions to request additional information from your end users when they interact with an action. For example, you can allow your end users to provide a reason for rejecting an approval by adding a text input parameter to a Reject button. When you create an action item that has parameters, you must also configure the UI parameters for the action function.

 For details on configuring these actions, see [Create an action function with parameters](../task/sg-studio-param-action-function.md).

</td><td>

![Action function.](../image/param-action-function.png)

</td></tr><tr><td>

Chat launcher action function

 Create a contextual link in your mobile application so that your users can connect to Virtual Agent or Live Agent, and receive information that pertains to their issues. By using a contextual link, your users automatically receive the information that you define about the relevant record.

 For details on configuring these actions, see [Configure a contextual link to Virtual Agent](../task/sg-av-context-action.md).

 **Note:** Connect chat is not supported in the native chat launcher.

</td><td>

![Virtual agent conversation.](../image/ExampleConversation.png)

</td></tr></tbody>
</table>