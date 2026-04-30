---
title: Configure Pre-chat after upgrading
description: If you have upgraded, some settings need to be configured to use Pre-chat effectively.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the chat channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Configure Pre-chat after upgrading

If you have upgraded, some settings need to be configured to use Pre-chat effectively.

## Before you begin

Role required: admin

## About this task

For information about using pre-chat surveys to capture preliminary information from a customer, see [Pre-chat surveys](../concept/csm-pre-chat-overview.md). If you have upgraded, you must manually adjust some settings to use Pre-chat most effectively.

## Procedure

1.  Make the predefined pre-chat surveys active.

    1.  Navigate to **Conversational Interfaces** &gt; **Pre-Chat Survey**.

    2.  Select the CSP Pre-Chat Survey, which collects preliminary information for logged-in customers.

    3.  In the form, select **Active**.

    4.  Click **Submit**.

    5.  Repeat this process for the CSP Anonymous Pre-Chat Survey, which collects preliminary information for users who are not logged in.

2.  Disable the legacy form-based chat widget from appearing in the portal header.

    1.  Type **sys\_properties\_list.do** from your instance.

    2.  Search for the **csp.legacy\_chat** property.

    3.  Set the property value to **true**.

    4.  Click **Update**.

    The **Chat** option from the portal header is disabled.

3.  Include the chat widget to appear on the Consumer Service Portal page.

    1.  Navigate to **Service Portal** &gt; **Agent Chat**.

    2.  Click **CSP Chat**.

    3.  Select **Active**.

    4.  Click **Submit**.

    The Open chat window icon that customers can use to initiate the pre-chat survey and connect with an agent will appear in the portal header.


