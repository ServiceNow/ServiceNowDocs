---
title: Configure the Moveworks chatbot for Employee Slate
description: Configure the Moveworks chatbot in the Moveworks Setup application. Employee Slate for Moveworks then renders the Moveworks AI Assistant, ingests identity from ServiceNow, and authenticates employees seamlessly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/empworks-configure-moveworks-chatbot.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-04-24"
reading_time_minutes: 2
keywords: [Moveworks chatbot, Moveworks Setup, trusted issuer, chatbot configuration]
breadcrumb: [Employee Slate for Moveworks, Configuration flow, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure the Moveworks chatbot for Employee Slate

Configure the Moveworks chatbot in the Moveworks Setup application. Employee Slate for Moveworks then renders the Moveworks AI Assistant, ingests identity from ServiceNow, and authenticates employees seamlessly.

## Before you begin

Before you configure the Moveworks chatbot, verify the following prerequisites:

-   You have the System administrator role.
-   The Moveworks Setup application is available under **Manage Applications**.
-   You have the ServiceNow instance URL that you want to register as a trusted issuer.

Role required: System administrator.

## About this task

The Moveworks chatbot configuration captures two related setups. The first is the chatbot record itself. The second is the internal connector that connects the chatbot to ServiceNow identity. For field definitions, see [Moveworks chatbot configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-moveworks-chatbot-fields.md).

## Procedure

1.  In **Manage Applications**, open **Moveworks Setup**.

2.  Select **Manage Chat Bots**.

    The list shows the chatbots configured for the organization. To edit an existing chatbot, select the record. To add a new chatbot, select **Create**.

3.  Set the chatbot fields for the Employee Slate surface.

    For each field and the value to use, see the chatbot record table in [Moveworks chatbot configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-moveworks-chatbot-fields.md). The required value is **Surface** = **Unified Front Door**, which lets Employee Slate render the chatbot.

4.  Select **Submit** to save the chatbot record.

    The new chatbot appears in the list with a generated **Channel configuration** value.

5.  From the Moveworks Setup navigation, open **Moveworks Setup** and select the chatbot that you created.

    The internal setup experience opens for the chatbot.

6.  Set the internal setup fields for User Inbox, the ServiceNow connector, the trusted issuer, and the Universal Assistance suggested prompts.

    To verify the correct connector label for the instance, open the core platform connector list under **Manage Applications**. The default Moveworks label is **snow**.

7.  Select **Submit** to save the internal setup.

8.  Open the Employee Slate URL and verify that the Moveworks assistant responds.

    Open the Employee Slate home page. Enter a greeting in the chat, such as `Hi`. The Moveworks assistant responds, which verifies connectivity and authentication.


## Result

Employee Slate renders the Moveworks chatbot with the configured suggested prompts. The trusted issuer authenticates employees, and the connector that you selected ingests identity.

