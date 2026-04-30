---
title: Review the inbound REST endpoint and configure inbound authentication
description: After you install the Virtual Agent API, navigate to the Scripted REST API resource to review the endpoint and set up authentication.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Review the inbound REST endpoint and configure inbound authentication

After you install the Virtual Agent API, navigate to the Scripted REST API resource to review the endpoint and set up authentication.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  Select the **VA Bot Integration** record to open it.

3.  In the **Resources** tab, open the **BOT Integration** record.

4.  Review the inbound REST API resource details.

    The format is: https://&lt;customer instance&gt;/api/sn\_va\_as\_service/bot/integration

    ![Review the Resource path value for the REST endpoint.](../images/scripted-rest-api-endpoint.png)

    For a description of the request parameters and an example send request, see [Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

5.  In the **Security** tab on the same page, select the **Requires authentication** check box.

    ![Select the Requires authentication check box.](../images/scripted-rest-api-botinteg.png)

6.  Set up Provider Authentication using any of these methods: Basic, OAuth, Hash, or Static Token.

    **Note:** Guest usage via Basic or OAuth is already supported out-of-box when you select **Requires authentication**. To support user account linking, you must use Static or Hash token-based authentication. You can use token-based authentication \(Static or Hash\) with or without Basic or OAuth authentication. The token can be passed in either the request body or the header. If the token is specified in both places, the one in the header is accepted.

    Do one of the following:

    -   Set up Basic or OAuth authentication.

        To learn more about OAuth authentication and the possible security configurations for scripted REST APIs, see [Enable OAuth with inbound REST](https://www.servicenow.com/docs/access?context=t_EnableOAuthWithREST&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

    -   Set up Message Authentication, which involves configuring either Static or Hash tokens, setting up Provider Authentication, and setting the channel identity. For details, see [Configure Message Authentication for inbound communication](set-up-message-auth-va-api.md).

## What to do next

If you are using Message Authentication, [Configure Message Authentication for inbound communication](set-up-message-auth-va-api.md).

[Configure the output response REST endpoint and outbound authentication for the Virtual Agent API](configure-response-endpoint-va-api.md).

**Parent Topic:**[Using Virtual Agent API](../concept/virtual-agent-api.md)

