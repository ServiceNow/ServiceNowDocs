---
title: Configure an Alexa skill
description: Configure your Alexa skill to talk to your ServiceNow instance.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Conversational Integration with Alexa, Configure Conversational Integration with Alexa, Conversational Integration with Alexa, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure an Alexa skill

Configure your Alexa skill to talk to your ServiceNow instance.

## Before you begin

**Note:** Linking your Alexa account with your ServiceNow instance is optional and only the Virtual Agent topics with the public role are accessible with guest user access.

Role required: admin

## Procedure

1.  Log in to the Alexa developer console with your Amazon developer account.

2.  Click the **Code** tab.

3.  Click **Import Code**.

    **Note:** Browse for the `lambda_funtion_sn_va_alexa.zip` file that you downloaded from the Supporting Documents section of the Conversational Integration with Alexa application on the ServiceNow Store and click **Import**.

4.  In the **endpoint** field, replace the hostname with the host name from your ServiceNow instance URL where your Alexa store app is installed.

    Example endpoint: `xxxxxxxxx.service-now.com/api/v1/alexa/message`.

5.  In the **secretkey** field, replace `<Provide secret key>` with your token \(static or hash-based\).

    Use the following tokens as per your authentication type.

    -   Hash-based token

        If you are using hash-based authentication, provide the hash token which you provided during the ServiceNow instance setup.

        ```
        `"var security = <Token>
                  "var genratedHash = generateHmac(eventJSON, secretKey);
                  'X-Voice-Type': 'hash',
                  'X-Voice-Token': genratedHash,"
        ```

        **Note:** Hash-based authentication is provided by default.

    -   Static token

        If you are using static authentication, provide the static token.

        ```
        `"var security = <Token>
                  'X-Voice-Type': 'static',
                 `'X-Voice-Token': <Token>,`
        ```

6.  Click **Deploy**.


**Parent Topic:**[Set up Conversational Integration with Alexa](setup-alexa.md)

