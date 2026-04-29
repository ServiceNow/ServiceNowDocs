---
title: Configure close condition
description: Configure the condition to exclude the chat conversation from auto importing.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Import messages from Microsoft Teams to ServiceNow, HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure close condition

Configure the condition to exclude the chat conversation from auto importing.

## Before you begin

Role required: admin

## About this task

When a ticket is set to inactive, the system does one final poll for any messages in the chat, removes the participants such that no further messages about the ticket can be exchanged in the chat, and then stops polling that chat. This is determined by the "active" field on a table being set to "false".

For any table with an active field, this behavior works automatically. If your custom application does not use an "active" field for determining whether the ticket remains active, define an alternate condition that can be used to denote the ticket as being closed or inactive.

Alternately, to adhere to platform standards, consider adding an active field to your custom application and maintaining the state of that field in accordance with the business logic of your application.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Chat Administration** &gt; **Close Conditions**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |:----|:----------|
    |Table|Option to select a table to which the requester mapping \(auto-import feature\) should be applicable.|
    |Inherit|Extend and apply the auto-import feature to the child tables.|
    |Active|Option to activate the requester-mapping record.|
    |Close conditions|Condition builder to define a condition that the record is closed.|

4.  Click **Submit**.

    **Note:**

    If you are creating a close condition for a new table, ensure to create business rule for close condition. For more information, refer [Configure business rule for close condition](business-rule-close-condition.md).


**Parent Topic:**[Configure Request-based chats to import messages from Microsoft Teams to ServiceNow](../concept/auto-import-messages.md)

