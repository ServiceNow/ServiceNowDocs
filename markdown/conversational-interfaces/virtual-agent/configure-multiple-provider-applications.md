---
title: Configure multiple provider applications
description: You can configure multiple provider applications to support AI agents where there are multiple primary bots using Virtual Agent API and you need to distinguish between them.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configure multiple provider applications

You can configure multiple provider applications to support AI agents where there are multiple primary bots using Virtual Agent API and you need to distinguish between them.

## Before you begin

Role required: admin

Be sure you are in Virtual Agent API application scope.

## Procedure

1.  Navigate to **All** &gt; **sys\_cs\_provider\_application**.

2.  Click **New** to create a new provider application.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the provider application, such as `VA API Custom Bot`.|
    |Provider|Select the provider as **VA Bot to Bot Provider**.|
    |Inbound Id|Unique inbound Id used in the request message, for example, custom\_1.|
    |Message Auth|Configure Message Authentication with a token for inbound communication. See [Configure Message Authentication for inbound communication](../task/set-up-message-auth-va-api.md) for more details.|

4.  Click **Submit**.

5.  Navigate to **All** &gt; **System Web Services** &gt; **REST Message**.

6.  Click **New** to create a new REST Message record.

7.  In the REST Message record, fill in the form fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the REST Message record. This should be the same as the newly created provider application.|
    |Endpoint|The response endpoint of the primary bot.|

8.  Click **Submit**.

9.  In the HTTP Methods section, click New to create a new method or you can override the default GET method.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the HTTP Method. Enter `postMessage`.|
    |HTTP method|Select **POST**.|
    |Endpoint|Enter the response endpoint of the primary bot.|
    |Authentication Type|Configure Basic or OAuth 2.0 authentication as per your requirement. For details about configuring basic authentication, see [Configure a REST message with basic auth](https://www.servicenow.com/docs/access?context=t_ConfigureRESTMsgBasicAuth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US). For information about configuring OAuth 2.0, see [Configure a REST message with OAuth](https://www.servicenow.com/docs/access?context=t_ConfigureARESTMessageWithOAuth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).|

10. To use the newly created provider application, pass the Inbound Id of the provider application in the **appInboundId** parameter of the Virtual Agent API request.

    You need to pass the Inbound Id of the provider application in the **appInboundId** parameter for every Virtual Agent API request. The following is a sample Virtual Agent API request that uses the newly created provider application.

    ```
    
    {
        "userId": "adminuser1",
        "emailId": "admin@example.com",
        "action": "START_CONVERSATION",
        "message": {
            "text": "",
            "typed": true
        },
        "appInboundId": "custom_1",
        "contextVariables": {
            "app_name": "test"
        }
    }
    
    ```

    You can test the configuration by viewing the outbound HTTP logs to verify that your response endpoint was called.


**Parent Topic:**[Using Virtual Agent API](virtual-agent-api.md)

