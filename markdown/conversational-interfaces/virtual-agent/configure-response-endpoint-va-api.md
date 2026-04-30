---
title: Configure the output response REST endpoint and outbound authentication for the Virtual Agent API
description: Specify the outbound endpoint URL to which the Virtual Agent responses are posted. Configure outbound authentication.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configure the output response REST endpoint and outbound authentication for the Virtual Agent API

Specify the outbound endpoint URL to which the Virtual Agent responses are posted. Configure outbound authentication.

## Before you begin

If needed, specify the Message Authentication for token validation in the Provider Channel Identities \[sys\_cs\_provider\_application\] table.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message.**

2.  Select the **VA Bot to Bot** record to open it.

3.  In the **Endpoint** field, enter the response endpoint for the third-party bot, and then click **Update**.

    This is the endpoint for the primary bot server, where the response will have to be sent from the ServiceNow bot to another bot or another ServiceNow instance.

    For example: `http://<customer instance>/demo/rest/service/nowbot/processResponse`

4.  In the **Authentication** tab, set the **Authentication type** field to either **Basic** or **OAuth 2.0**, and then click **Update**.

    -   **Basic:** In the **Basic auth profile** field, select or create a Basic auth profile. It will contain a username and password.

        ![In the Basic auth profile field, the BotAdmin profile is selected. The profile information shows the name, username, and password.](../images/va-api-basic-auth-config.png)

    -   **OAuth:** In the **OAuth profile** field, select or create an OAuth profile. After saving your changes, click **Get OAuth Token** in the related links list.
    For details about configuring basic authentication, see [Configure a REST message with basic auth](https://www.servicenow.com/docs/access?context=t_ConfigureRESTMsgBasicAuth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US). For information about configuring OAuth 2.0, see [Configure a REST message with OAuth](https://www.servicenow.com/docs/access?context=t_ConfigureARESTMessageWithOAuth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

5.  Review the JSON response returned from the endpoint call.

    For a description of the Virtual Agent API response parameters and an example of a successful response, see [Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).


**Parent Topic:**[Using Virtual Agent API](../concept/virtual-agent-api.md)

