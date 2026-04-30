---
title: Redirect user authentication to a Service Portal
description: After installing a pre-built Conversational Integration \(for messaging apps, Consumer apps or voice apps\), you can specify a Service Portal in which unauthenticated end users complete the user authentication step \(user account linking\), instead of in their ServiceNow instance. Users who do not have linked accounts complete authentication before continuing with the virtual agent in the messaging application.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Redirect user authentication to a Service Portal

After installing a pre-built Conversational Integration \(for messaging apps, Consumer apps or voice apps\), you can specify a Service Portal in which unauthenticated end users complete the user authentication step \(user account linking\), instead of in their ServiceNow instance. Users who do not have linked accounts complete authentication before continuing with the virtual agent in the messaging application.

## Before you begin

Install the Virtual Agent messaging integrations for your instance. The system creates a record in the Provider Auth \[provider\_auth\] table for each integration that you install \(Slack, Microsoft Teams, and Workplace, LINE, Twilio, WhatsApp, Facebook Messenger, Alexa, Google Assistant, Amazon Connect\). You use the Provider Auth table to specify the Service Portal in which user authentication occurs.

Role required: admin

## Procedure

1.  In the navigation filter, type `provider_auth.list`.

2.  In the Provider Auth table, open the record for the messaging integration you installed.

3.  In the **Service Portal** field, select the Service Portal in which user authentication occurs.

4.  Click **Update**.


## Result

When unauthenticated users start a conversation with the virtual agent for the first time in the messaging integration, they are redirected to the Service Portal specified for the provider in the Provider Auth table. After they log in to the Service Portal, they are prompted to [link their ServiceNow account to the messaging application](../../notification/task/link-accounts-with-virtual-agent.md).

**Parent Topic:**[Virtual Agent integration with messaging apps](../concept/va-integration-messaging-apps.md)

