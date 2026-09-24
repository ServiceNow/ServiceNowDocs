---
title: \(Legacy\) Configure Google Dialogflow ES as the NLU provider for Virtual Agent
description: Use the intents, entities, and utterances defined in Google Dialogflow ES. Apply them as an NLU model for your Virtual Agent conversations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/configure-dialogflow-es-integration.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure NLU in Virtual Agent, Configure NLU, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Configure Google Dialogflow ES as the NLU provider for Virtual Agent

Use the intents, entities, and utterances defined in Google Dialogflow ES. Apply them as an NLU model for your Virtual Agent conversations.

Configuring the Google Dialogflow ES integration involves providing Google Dialogflow credentials for authentication. You can set only one NLU service provider for your instance.

## Requirements

This NLU configuration requires the following:

-   A Brazil ServiceNow instance
-   A Google Dialogflow ES agent with defined intents, entities, and utterances

    For more information, see the [Google Dialogflow ES documentation](https://cloud.google.com/dialogflow/es/docs/console).

    **Note:** A Google Dialogflow agent is similar to a ServiceNow model. Currently, Virtual Agent only supports one Google Dialogflow ES agent per instance.

-   Access to the Google Cloud platform
-   The Glide Virtual Agent \[com.glide.cs.chatbot\] plugin must be installed on your ServiceNow instance.

    The following plugins are installed with Glide Virtual Agent by default:

    -   com.snc.integration.sso.multi.installer: Integration - Multiple Provider Single Sign-On Installer
    -   com.glide.nlu.googledialogflow.es.intent.discovery: Proxy agent to the Google Dialogflow ES Natural Language Understanding server

