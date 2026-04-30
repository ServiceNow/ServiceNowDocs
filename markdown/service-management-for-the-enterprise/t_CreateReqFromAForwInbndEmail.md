---
title: Create a request from a forwarded inbound email
description: Requests can be automatically created from the information in forwarded inbound emails as long the functionality has been enabled on the configuration screen of SM application. The emails are also to be sent to a mailbox defined by criteria in the appropriate inbound email action.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request creation using inbound email actions, Request creation, Request Management in a Service Management application, Service Management]
---

# Create a request from a forwarded inbound email

Requests can be automatically created from the information in forwarded inbound emails as long the functionality has been enabled on the configuration screen of SM application. The emails are also to be sent to a mailbox defined by criteria in the appropriate inbound email action.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Inbound Actions**.

2.  Select the inbound email action called **Create \[application name\] Request \(Forwarded\)**.

    The forwarded inbound email action record opens and displays the default conditions that trigger the inbound email action.

    When an email is forwarded to the mail list defined by the criteria in **Action**, a request is created with the following information:

    -   The **Contact type** is set to **Email**.
    -   The email sender \(if found\) populates the **opened\_by** and **Caller** fields for a newly created sm\_order based item.
    -   The email subject populates the **Short description** field.
    -   The email body populates the **Description** field.
    -   The email senders company \(Sender-&gt;Company\) populates the **Company** field.
    -   The email senders location \(Sender-&gt;Location\) populates the **Location** field.
    -   The entire email is copied into the **Work notes** field.
3.  You can use the email action as it is or modify it to meet the needs of your organization.


**Parent Topic:**[Request creation using inbound email actions](../reference/r_ReqCreateUseInboundEmailAct.md)

