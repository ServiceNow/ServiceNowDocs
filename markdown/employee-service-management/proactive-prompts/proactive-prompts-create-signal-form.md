---
title: Signal configuration form
description: Form to create a signal in Proactive Prompts.
locale: en-US
release: xanadu
product: Proactive Prompts
classification: proactive-prompts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference for Proactive Prompts, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Signal configuration form

Form to create a signal in Proactive Prompts.

<table id="table_i32_kgc_pvb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the signal configuration.

</td></tr><tr><td>

Description

</td><td>

Brief description of the signal configuration.

</td></tr><tr><td>

Active

</td><td>

Option to activate the signal configuration.

</td></tr><tr><td>

Schedule

</td><td>

Determines how frequently to send the prompt to the user.For more information, see [Configure signal schedules in Proactive Prompts](../task/proactive-prompts-signal-schedules.md).

</td></tr><tr><td>

Priority

</td><td>

Determines the display order of prompts on the prompt widget. The available values are High, Low, or Medium.

</td></tr><tr><td>

Order

</td><td>

Stores the order related to the signal.

</td></tr><tr><td>

Category tags

</td><td>

The category for the signal, which is used to pull specific prompts on the prompt widget. For more information, see [Configure signal categories in Proactive Prompts](../task/proactive-prompts-signal-catergories.md).

</td></tr><tr><td>

Channels and actions

</td><td>

The channel where the prompts should be displayed and the actions associated with the channel. For more information, see [Configure delivery channels in Proactive Prompts](../task/proactive-prompts-config-channels.md).

</td></tr><tr><td>

Receiving user

</td><td>

The user to receive the prompt, either the manager or an employee.**Note:**

-   The employee value is taken from the **User** field of the data source specified in the **Datasource** field.
-   The manager of an employee is derived from the **Manager** field in the User \[sys\_user\] table.

</td></tr><tr><td class="sub-head" colspan="2">

Signal Source

</td></tr><tr><td>

Datasource

</td><td>

The data source method to retrieve the data.For more information, see [Types of data sources in Proactive Prompts](proactive-prompts-data-source.md).

</td></tr><tr><td class="sub-head" colspan="2">

Prompt Template

</td></tr><tr><td>

Prompt header

</td><td>

Icon and label displayed on the Employee Portal to identify the type of prompt. For example, you could have headers for Skills, Learning, Roles, and so on.For information on adding headers, see [Add a new prompt header to identify the prompt](../task/proactive-prompts-add-header.md).

</td></tr><tr><td>

Title

</td><td>

Title of the message when the prompt is displayed to the user.

</td></tr><tr><td>

Single record display

</td><td>

A template for the message to be displayed to the user when the prompt is generated for a single record.

</td></tr><tr><td>

Multiple record display

</td><td>

A template for the message to display to users when the prompt is generated for multiple records.For more information on tokens, see [Tokens in Proactive Prompts](proactive-prompts-tokens.md).

</td></tr><tr><td>

URL

</td><td>

A URL that the user can access in the **View details** action on the Employee Portal or **Take action** action for Virtual Agent.For more information, see [Actions and action groups in Proactive Prompts](proactive-prompts-actions.md).

</td></tr></tbody>
</table>**Parent Topic:**[Reference for Proactive Prompts](proactive-prompts-reference.md)

**Related topics**  


[Components installed with Proactive Prompts](proactive-prompts-components.md)

[Tokens in Proactive Prompts](proactive-prompts-tokens.md)

[Types of data sources in Proactive Prompts](proactive-prompts-data-source.md)

[Actions and action groups in Proactive Prompts](proactive-prompts-actions.md)

[Signal data source form](proactive-prompts-signal-datasource-form.md)

