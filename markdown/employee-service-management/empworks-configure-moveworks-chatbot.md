---
title: Configure the Moveworks chat bot for Employee Slate
description: Configure the Moveworks web chat bot in the Moveworks Setup application. Employee Slate for Moveworks then renders the Moveworks AI Assistant, ingests identity from ServiceNow, and authenticates employees seamlessly.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-24"
reading_time_minutes: 2
keywords: [Moveworks chat bot, Moveworks Setup, trusted issuer, chat bot configuration]
breadcrumb: [Employee Slate for Moveworks, Employee Slate setup flow, Employee Slate, Employee Service Management]
---

# Configure the Moveworks chat bot for Employee Slate

Configure the Moveworks web chat bot in the Moveworks Setup application. Employee Slate for Moveworks then renders the Moveworks AI Assistant, ingests identity from ServiceNow, and authenticates employees seamlessly.

## Before you begin

Before you configure the Moveworks chat bot, verify the following prerequisites:

-   You have the System administrator role.
-   The Moveworks Setup application is available under **Manage Applications**.
-   You have the ServiceNow instance URL that you want to register as a trusted issuer.

Role required: System administrator.

## About this task

The Moveworks chat bot configuration captures two related setups. The first is the chat bot record itself. The second is the internal connector that connects the chat bot to ServiceNow identity. For field definitions, see [Moveworks chat bot configuration fields](../reference/empworks-moveworks-chatbot-fields.md).

## Procedure

1.  In **Manage Applications**, open **Moveworks Setup**.

2.  Select **Manage Chat Bots**.

    The list shows the chat bots configured for the organization. To edit an existing chat bot, select the record. To add a new chat bot, select **Create**.

3.  Set the chat bot fields for the Employee Slate surface.

    For each field and the value to use, see the chat bot record table in [Moveworks chat bot configuration fields](../reference/empworks-moveworks-chatbot-fields.md). The required value is **Surface** = **Unified Front Door**, which lets Employee Slate render the chat bot.

4.  Select **Submit** to save the chat bot record.

    The new chat bot appears in the chat bot list with a generated **Channel configuration** value.

5.  From the Moveworks Setup navigation, open **Moveworks Setup** and select the chat bot that you created.

    The internal setup experience opens for the chat bot.

6.  Set the internal setup fields for User Inbox, the ServiceNow connector, the trusted issuer, and the Universal Assistance suggested prompts.

    For each field and the value to use, see the internal setup table in [Moveworks chat bot configuration fields](../reference/empworks-moveworks-chatbot-fields.md).

    To verify the correct connector label for the instance, open the core platform connector list under **Manage Applications**. The default Moveworks label is **snow**.

7.  Select **Submit** to save the internal setup.

8.  Open the Employee Slate URL and verify that the Moveworks assistant responds.

    Open the Employee Slate home page. Enter a greeting in the chat, such as `Hi`. The Moveworks assistant responds, which verifies connectivity and authentication.


## Result

Employee Slate renders the Moveworks chat bot with the configured suggested prompts. The trusted issuer authenticates employees, and the connector that you selected ingests identity.

