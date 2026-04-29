---
title: Create a signal in Proactive Prompts
description: Configure signals to determine what prompts to send, whom to send them to, where and when to send them, and to generate them to send to your user.
locale: en-US
release: australia
product: Proactive Prompts
classification: proactive-prompts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Proactive Prompts, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Create a signal in Proactive Prompts

Configure signals to determine what prompts to send, whom to send them to, where and when to send them, and to generate them to send to your user.

## Before you begin

**Note:** You must install and activate both the Proactive Prompts application and Now Assist for HRSD application so that you can use the capability and prompts from the base system. The two signals that are available for use are the Approvals pending prompt, and the High leave balance prompt.

Role required: sn\_pp.admin

## Procedure

1.  Navigate to **All** &gt; **Proactive Prompts** &gt; **Signal Configurations**.

2.  Select **New**.

3.  In the **Name** field, enter a name for the signal configuration.

4.  In the **Description** field, enter a brief description about the signal.

5.  Activate the signal by selecting the **Active** option.

6.  In the **Schedule** field, select a schedule that determines the frequency of sending the prompt to the user.

    For more information on schedules, see [Configure signal schedules in Proactive Prompts](proactive-prompts-signal-schedules.md).

7.  In the **Priority** field, select the priority to determine the display order of the prompts on the prompt widget.

    The available values are High, Low, or Medium.

8.  In the **Order** field, select the order that is related to the signal.

9.  In the **Category tags** field, select the category for the signal, which is used to pull the specific prompts on the prompt widget.

    For more information, see [Configure signal categories in Proactive Prompts](proactive-prompts-signal-catergories.md).

10. In the **Channels and actions** field, select the channel where you want the prompts to be displayed and the actions that you want to associate with the channel.

    For more information, see [Configure delivery channels in Proactive Prompts](proactive-prompts-config-channels.md).

11. In the **Receiving user** field, select the user that you want to receive the prompt, either the manager or an employee.

    **Note:**

    -   The employee value is taken from the **User** field of the data source that is specified in the **Datasource** field.
    -   The manager of an employee is derived from the **Manager** field in the User \[sys\_user\] table.
12. On the **Signal Source** tab, select the data source method to retrieve the data in the **Datasource** field.

    For more information, see [Types of data sources in Proactive Prompts](../reference/proactive-prompts-data-source.md).

13. On the **Prompt template** tab, fill in the fields.

    The content in the template is displayed as the content of the prompt to your user.

<table id="table_cyt_kyc_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Prompt header

</td><td>

Header for the prompt or create a header. For information on adding a new header, see [Add a new prompt header to identify the prompt](proactive-prompts-add-header.md).The header is an icon and a label that is displayed on the prompt to identify the type of prompt on the Employee Portal. For example, you could have headers for Skills, Learning, Roles, and so on.

**Note:** If no header is selected, then the header that's marked as default is added to the prompt and displayed.

</td></tr><tr><td>

Title

</td><td>

Title of the message when the prompt is displayed to the user.

</td></tr><tr><td>

Single record display

</td><td>

Template for the message to be displayed to the user when the prompt is generated for a single record.

</td></tr><tr><td>

Multiple record display

</td><td>

Template for the message to display to users when the prompt is generated for multiple records.For more information, see [Tokens in Proactive Prompts](../reference/proactive-prompts-tokens.md).

</td></tr><tr><td>

URL

</td><td>

URL that the user can access in the **View details** option on the Employee Portal or **Take action** option for Virtual Agent.For more information, see [Actions and action groups in Proactive Prompts](../reference/proactive-prompts-actions.md).

</td></tr></tbody>
</table>    You've created a template that is delivered as a message in the prompt to the user.

14. Select **Submit**.

    You've configured a signal that delivers the prompt message to the user in the frequency that you scheduled.


