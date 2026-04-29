---
title: Configure Message Authentication for inbound communication
description: You can configure Message Authentication for the Virtual Agent API instead of Basic or OAuth. Message Authentication involves configuring either Static or Hash tokens, setting up Provider Authentication, and setting the channel identity.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Review inbound response REST endpoint and configure inbound authentication, Configure, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Configure Message Authentication for inbound communication

You can configure Message Authentication for the Virtual Agent API instead of Basic or OAuth. Message Authentication involves configuring either Static or Hash tokens, setting up Provider Authentication, and setting the channel identity.

## Before you begin

Follow the steps in [Review the inbound REST endpoint and configure inbound authentication](configure-send-request.md).

Role required: admin

## Procedure

1.  Configure the token by doing one of the following, depending on the token type:

    -   Static token:
        1.  Navigate to **All**, and then enter `token_verification.list` in the filter.
        2.  Click **New**.
        3.  On the Token Verifications form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the authentication token, such as `B2BTestAppAuthToken`.|
            |Description|Description of the authentication token, such as `B2B Testing application Auth Token`.|
            |Token|Enter an authentication token that you generated using any general programming or scripting language, or click **Generate Secure Token** in the Related Links.|

        4.  Click **Submit**.
    -   Hash token:
        1.  Navigate to **All**, and then enter `hash_message_verification.list` in the filter.
        2.  Click **New**.
        3.  On the Hash Message Verification form, fill in the fields.

            |Fields|Description|
            |------|-----------|
            |Name|Name of the authentication token, such as `B2BTestAppAuthToken`.|
            |Description|Description of the authentication token, such as `B2B Testing application Auth Token`.|
            |Secret|Authentication token \(random string\).|

        4.  Click **Submit**.
2.  Set up Provider Authentication for token-based authentication.

    1.  Navigate to **All**, and then enter `message_auth.list` in the filter.

    2.  Click **New**.

    3.  On the Message Auths form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the message authentication, such as `B2B Auth token`.|
        |Provider|Name of the provider.|
        |Group name|Not required.|
        |Service Portal|Not required.|
        |Inbound message verification|Select the Static token or Hash message token that you created.|
        |Outbound message creation|This field is currently not supported in the Virtual Agent API. Select the Static token or Hash message token that you created.|
        |Outbound service token|This field is currently not supported in the Virtual Agent API.|

    4.  Click **Submit**.

3.  Set the channel identity.

    1.  Navigate to **All**, and then enter `sys_cs_provider_application.list` in the filter.

    2.  Select the **VA Bot to Bot Provider Application** record to open it.

    3.  In the Provider Channel Identity form, locate the **Message auth** field and select the message auth that you set up previously.

        ![Provider Channel Identify form for VA Bot-to-Bot Provider Application record, with Message auth field highlighted.](../images/b2b-provider-identity_brand2.0.png)

    4.  Click **Update**.

4.  For Hash token-based authentication only, send the **x-b2b-signature** in the request headers.

    The value is the **HmacSHA1** encoded value of the request payload, which uses the token created in the ServiceNow instance. For example, in Postman, follow these steps:

    1.  In the Headers, set the **x-b2b-signature** to `{{hashValue}}`.

        ![Example Postman encoding in Headers.](../images/postman-encoding-example.png)

    2.  In the Pre-request Script area, set the token as follows:

        ```
        pm.environment.set('hashValue', CryptoJS.HmacSHA1(JSON.stringify(JSON.parse(request.data)), '<insert your token>').toString(CryptoJS.enc.Hex));
        ```

        ![Example Postman pre-request script that shows where to enter the token.](../images/postman-prerequest-script.png)


## What to do next



**Parent Topic:**[Review the inbound REST endpoint and configure inbound authentication](configure-send-request.md)

