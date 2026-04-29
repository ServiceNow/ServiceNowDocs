---
title: Configure custom assistant
description: Configure a custom telephony provider to use instead of the out-of-the-box voice assistant.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 1
breadcrumb: [Create an AI voice assistant, Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Configure custom assistant

Configure a custom telephony provider to use instead of the out-of-the-box voice assistant.

## Before you begin

Role required: admin

## Procedure

1.  Configure the token by doing one of the following, depending on the token type:

    -   Static token:
        1.  Navigate to **All**, and then enter `token_verification.list` in the navigation filter.
        2.  Select **New**.
        3.  On the form, fill in the fields.

<table id="table_lml_hbq_kqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the authentication token, such as `AI voice token`.

</td></tr><tr><td>

Description

</td><td>

Description of the authentication token, such as `Voice Agent Auth Token`.

</td></tr><tr><td>

Token

</td><td>

Authentication token that is used to authenticate the provider application. Enter the authentication token that you generated using any general programming or scripting language, or select the **Generate Secure Token** related link.

</td></tr></tbody>
</table>        4.  Select **Submit**.
    -   Hash token:
        1.  Navigate to **All**, and then enter `hash_message_verification.list` in the navigation filter.
        2.  Select **New**.
        3.  On the form, fill in the fields.

            |Fields|Description|
            |------|-----------|
            |Name|Name of the authentication token, such as `AI voice token`.|
            |Description|Description of the authentication token, such as `Voice Agent Auth Token`.|
            |Secret|Authentication token \(random string\).|

        4.  Select **Submit**.
2.  Set up Provider Authentication for token-based authentication.

    1.  Navigate to **All**, and then enter `message_auth.list` in the navigation filter.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the message authentication, such as `AI voice token`.|
        |Provider|Name of the provider, for example, AI Voice provider.|
        |Group name|Not required.|
        |Service Portal|Not required.|
        |Inbound message verification|Select the Static token or Hash message token that you created.|
        |Outbound message creation|Select the Static token or Hash message token that you created.|
        |Outbound service token|This field is not supported.|

    4.  Select **Submit**.

3.  Set the channel identity.

    1.  Navigate to **All**, and then enter `sys_cs_provider_application.list` in the navigation filter.

    2.  Select the **AI Voice Agent Provider Application** record to open it.

        If you want to use an existing application or create a new provider application, be sure to update the existing configuration according to the values mentioned in [Configuration for custom AI voice agent provider](../reference/voice-agent-reference.md#section_ip2_fpw_jgc) before proceeding further.

    3.  In the Provider Channel Identity form, locate the **Message auth** field and select the message auth that you set up previously.

        ![Provider Channel Identity form for the AI Voice Agent Provider Application record, with the Message auth field highlighted.](../image/voice-agents-provider-application-config.png)

    4.  Select **Update**.


