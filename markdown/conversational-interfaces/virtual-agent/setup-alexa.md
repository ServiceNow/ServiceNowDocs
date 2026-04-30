---
title: Set up Conversational Integration with Alexa
description: Set up the Conversational Integration with Alexa application so that you can engage customers in conversations with bots.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Conversational Integration with Alexa, Integrating Virtual Agent with Alexa, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up Conversational Integration with Alexa

Set up the Conversational Integration with Alexa application so that you can engage customers in conversations with bots.

## Before you begin

-   Get ServiceNow entitlements for the following products and applications:

    -   Integration Hub
    -   Conversational Integration with Alexa
    For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

-   Install the following applications on your ServiceNow instance:
    -   Integration Hub
    -   Conversational Integration with Alexa
-   Complete the Alexa settings.
    1.  Create your Amazon Developer account.

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-GB/docs/alexa/ask-overviews/create-developer-account.html).

    2.  [Create an Alexa skill](create-alexa-skill.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-US/docs/alexa/custom-skills/steps-to-build-a-custom-skill.html).

    3.  [Build an Alexa skill model](build-alexa-skill.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-GB/docs/alexa/conversations/build-model.html).

    4.  Configure an Alexa skill.

        For more information, see [Configure an Alexa skill](confgure-alexa-for-snow-instance.md)

        .

    5.  [Test an Alexa skill on the developer console](test-alexa-skill.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-US/docs/alexa/devconsole/test-your-skill.html).

    6.  [Account linking with Alexa](../concept/account-linking-alexa.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-US/docs/alexa/account-linking/account-linking-for-custom-skills.html).


Role required: external\_app\_install\_admin, va\_admin, or admin

## Procedure

1.  Associate a provider channel identity record with your Alexa account.

    For more information, see [Create a provider channel identity record for Alexa](create-provider-channel-id-record-alexa.md).

2.  Associate inbound message records with a message auth record.

    For more information, see [Set up message authentication for Alexa](setup-message-auth-alexa.md).


