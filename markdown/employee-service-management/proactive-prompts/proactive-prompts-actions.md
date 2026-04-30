---
title: Actions and action groups in Proactive Prompts
description: Actions provide the user the ability to act on the prompt.
locale: en-US
release: yokohama
product: Proactive Prompts
classification: proactive-prompts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference for Proactive Prompts, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Actions and action groups in Proactive Prompts

Actions provide the user the ability to act on the prompt.

The types of actions available differ based on the channel. Unless otherwise noted, the actions in the following table are available for Employee Portal and Virtual Agent.

<table id="table_wcw_5fg_vvb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View details

</td><td>

Enables the user to see more details about the prompt, including any URL provided in the signal configuration. Users can also access links directly to the items/tasks/records based on the URL configured in the Script data source. For more information see, [Create a signal in Proactive Prompts](../task/proactive-prompts-signal-create.md).**Note:**

-   The display of links to items/tasks/records only works with the Script data source.
-   The details displayed are influenced by the selection in the Collect records field.
-   This action is available only for the Employee Portal. In Virtual Agent, the details are displayed by default.

</td></tr><tr><td>

Send email

</td><td>

The user can send an email directly from the prompt. This action takes the user directly to the compose window depending on the default mail client configured in your organization. Users can choose to send the email to one user or all users at the same time.**Note:** Only active users with their email configured in the User \[sys\_user\] table can be selected to send the email.

</td></tr><tr><td>

Set up meeting

</td><td>

The user can schedule a meeting via the default mail client like Outlook or Gmail based on your organization's configuration.**Note:**

-   This action has a configurable action parameter **mailClient** of type string. By default, the mail client is Outlook. You can change it to Gmail.
-   Only active users with their email configured in the User \[sys\_user\] table can be selected to set up a meeting.
-   This parameter is applicable only for Employee Portal actions.

</td></tr><tr><td>

Start chat

</td><td>

The user can talk to the stake holder one-on-one via Microsoft Teams.**Note:**

-   The Start chat action requires the com.snc.ms\_teams plugin to have been installed.
-   Only active users with their email configured in the User \[sys\_user\] table can be selected to start a chat.

</td></tr></tbody>
</table>**Note:** The configurable action parameter **selectindividual** under Actions in the Employee Center Action framework determines whether you can select all employees or one individual employee for the Send email, Set up meeting, and Start chat actions. The default value is false. This parameter is applicable only for actions in Employee Portal.

## Action groups

Action groups are a collection of frequently used actions in a framework for quick access. Action groups are used only in Employee Portal. For Proactive Prompts, the action groups available are:

-   Chat action group
-   Email action group

For more information, see [Action group](../../employee-center/concept/action-group-framework.md).

**Parent Topic:**[Reference for Proactive Prompts](proactive-prompts-reference.md)

**Related topics**  


[Components installed with Proactive Prompts](proactive-prompts-components.md)

[Tokens in Proactive Prompts](proactive-prompts-tokens.md)

[Types of data sources in Proactive Prompts](proactive-prompts-data-source.md)

[Signal data source form](proactive-prompts-signal-datasource-form.md)

[Signal configuration form](proactive-prompts-create-signal-form.md)

