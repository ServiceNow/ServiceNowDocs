---
title: Configure output response REST endpoint and outbound authentication for the Virtual Agent API \(v4.1 or following\)
description: Specify the outbound endpoint URL to which the Virtual Agent responses are posted. Configure outbound authentication.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [Configure, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Configure output response REST endpoint and outbound authentication for the Virtual Agent API \(v4.1 or following\)

Specify the outbound endpoint URL to which the Virtual Agent responses are posted. Configure outbound authentication.

## Before you begin

If needed, specify the Message Authentication for token validation in the Provider Channel Identities \[sys\_cs\_provider\_application\] table.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the **Bot to Bot Outbound Configurations** \[sn\_va\_as\_service\_outbound\_configuration\] table and open it.

3.  Select the **VA Bot to Bot Provider Application** record to open it.

4.  Navigate to the **Rest connection** field and open the record.

5.  In the **Connections** related tab, select **Bot Connection**.

6.  In the **Credential** field, select or create an authentication profile.

7.  In the **Connection URL** field, enter the response endpoint for the third-party bot.

    This is the endpoint for the primary bot server, where the response will have to be sent from the ServiceNow bot to another bot or another ServiceNow instance.

    For example: `http://<customer instance>/demo/rest/service/nowbot/processResponse`

8.  Customize Connection timeout if you want to.

    The default value for Connection timeout is 5000ms.

9.  In the **Attributes** related tab, add headers and its values.

    **Note:** You can add maximum 10 headers.

10. Select **Update**.


**Parent Topic:**[Configuring Virtual Agent API](../concept/configure-virtual-agent-api.md)

