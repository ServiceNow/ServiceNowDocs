---
title: \(Legacy\) Set up Conversational Integration with Alexa
description: Set up the Conversational Integration with Alexa application so that you can engage customers in conversations with bots.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/setup-alexa.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure Conversational Integration with Alexa, Conversational Integration with Alexa, Integrate VA for NLU with voice channels, Virtual Agent channel integrations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Set up Conversational Integration with Alexa

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

    2.  [\(Legacy\) Create an Alexa skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-alexa-skill.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-US/docs/alexa/custom-skills/steps-to-build-a-custom-skill.html).

    3.  [\(Legacy\) Build an Alexa skill model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/build-alexa-skill.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-GB/docs/alexa/conversations/build-model.html).

    4.  Configure an Alexa skill.

        For more information, see [\(Legacy\) Configure an Alexa skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/confgure-alexa-for-snow-instance.md)

        .

    5.  [\(Legacy\) Test an Alexa skill on the developer console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/test-alexa-skill.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-US/docs/alexa/devconsole/test-your-skill.html).

    6.  [\(Legacy\) Account linking with Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/account-linking-alexa.md).

        For more information, see the [Alexa documentation](https://developer.amazon.com/en-US/docs/alexa/account-linking/account-linking-for-custom-skills.html).


Role required: external\_app\_install\_admin, va\_admin, or admin

## Procedure

1.  Associate a provider channel identity record with your Alexa account.

    For more information, see [\(Legacy\) Create a provider channel identity record for Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-provider-channel-id-record-alexa.md).

2.  Associate inbound message records with a message auth record.

    For more information, see [\(Legacy\) Set up message authentication for Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/setup-message-auth-alexa.md).


-   **[\(Legacy\) Create an Alexa skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-alexa-skill.md)**  
Create an Alexa-hosted skill using the Alexa developer console. Creating an Alexa skill helps you prepare to use the Alexa app.
-   **[\(Legacy\) Configure an Alexa skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/confgure-alexa-for-snow-instance.md)**  
Configure your Alexa skill to talk to your ServiceNow instance.
-   **[\(Legacy\) Build an Alexa skill model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/build-alexa-skill.md)**  
Build your Alexa-hosted skill on the Alexa developer console. Building a saved Alexa skill model helps you prepare the skill for testing.
-   **[\(Legacy\) Get the Alexa skill ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/get-skill-id.md)**  
Get the Alexa Skill ID from your Alexa developer console after configuring the skill. The Skill ID is the Alexa identifier for the application.
-   **[\(Legacy\) Test an Alexa skill on the developer console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/test-alexa-skill.md)**  
Test your Alexa skill using the Alexa simulator and developer account once the installation is complete and the skill is built.
-   **[\(Legacy\) Test a skill on the Alexa mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/test-skill-mobile.md)**  
Test your Alexa skill using the Alexa mobile app.
-   **[\(Legacy\) Test a skill on the Alexa Echo or Echo Show screen device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/test-skill-echo-show.md)**  
Test your Alexa skill using the Alexa Echo or Echo Show screen device.
-   **[\(Legacy\) Supported Alexa intents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/alexa-intents.md)**  
Use the Alexa intents supported by Conversational Integration with Alexa to receive an appropriate response during custom chat integrations with Alexa.
-   **[\(Legacy\) Create a provider channel identity record for Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-provider-channel-id-record-alexa.md)**  
Create a provider channel identity record to connect to your Alexa account.
-   **[\(Legacy\) Set up message authentication for Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/setup-message-auth-alexa.md)**  
Define a token in your ServiceNow instance to set up a message authentication with your Alexa account.

**Parent Topic:**[Configure Conversational Integration with Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-amazon-alexa.md)

