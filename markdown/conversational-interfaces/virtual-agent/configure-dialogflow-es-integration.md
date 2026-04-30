---
title: Configure Google Dialogflow ES as the NLU provider for Virtual Agent
description: Use the intents, entities, and utterances defined in Google Dialogflow ES. Apply them as an NLU model for your Virtual Agent conversations.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Natural Language Understanding in Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configure Google Dialogflow ES as the NLU provider for Virtual Agent

Use the intents, entities, and utterances defined in Google Dialogflow ES. Apply them as an NLU model for your Virtual Agent conversations.

Configuring the Google Dialogflow ES integration involves providing Google Dialogflow credentials for authentication. You can set only one NLU service provider for your instance.

## Requirements

This NLU configuration requires the following:

-   A Yokohama ServiceNow instance
-   A Google Dialogflow ES agent with defined intents, entities, and utterances

    For more information, see the [Google Dialogflow ES documentation](https://cloud.google.com/dialogflow/es/docs/console).

    **Note:** A Google Dialogflow agent is similar to a ServiceNow model. Currently, Virtual Agent only supports one Google Dialogflow ES agent per instance.

-   Access to the Google Cloud platform
-   The Glide Virtual Agent \[com.glide.cs.chatbot\] plugin must be installed on your ServiceNow instance.

    The following plugins are installed with Glide Virtual Agent by default:

    -   com.snc.integration.sso.multi.installer: Integration - Multiple Provider Single Sign-On Installer
    -   com.glide.nlu.googledialogflow.es.intent.discovery: Proxy agent to the Google Dialogflow ES Natural Language Understanding server

1.  [Create a service account and private key in Google Dialogflow ES](../task/vad-create-srvc-acct-key-dialogflow.md)  
To use Google Dialogflow as your NLU provider for Virtual Agent, create a service account and private key for your agent in Google Dialogflow.
2.  [Generate a Java Keystore \(JKS\) file and configure security on your ServiceNow instance](../task/vad-configure-dialogflow-security.md)  
To use Google Dialogflow as your NLU provider for Virtual Agent, use the private key you downloaded to generate a JKS file and set up authentication in your ServiceNow instance.
3.  [Activate the Google Dialogflow ES service and enable it in your instance](../task/activate-ggl-df-es-service.md)  
When you activate the Google Dialogflow ES service in the Open NLU Drivers \[open\_nlu\_driver\] table, the service becomes available as an option in Virtual Agent NLU settings.
4.  [Test Virtual Agent with Google Dialogflow ES NLU in Virtual Agent Designer](../task/test-va-nlu-dialogflow.md)  
Test topic discovery with Google Dialogflow and Virtual Agent in the Virtual Agent Designer interface.

**Parent Topic:**[Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md)

