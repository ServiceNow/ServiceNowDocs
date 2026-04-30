---
title: Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect
description: With Bot Interconnect, you can use ServiceNow Virtual Agent as the primary bot with a Google Dialogflow secondary bot. All of the skills and topics available to Google Dialogflow are made available to and executable from channels that are configured for ServiceNow Virtual Agent.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect

With Bot Interconnect, you can use ServiceNow® Virtual Agent as the primary bot with a Google Dialogflow secondary bot. All of the skills and topics available to Google Dialogflow are made available to and executable from channels that are configured for ServiceNow® Virtual Agent.

## Prerequisites

This bot configuration requires the following:

-   A Yokohama ServiceNow instance
-   Virtual Agent Bot Interconnect Store application
-   A Google Dialogflow account

1.  [Create a new agent in Google Dialogflow](../task/create-new-agent-google-dialogflow.md)  
To use Google Dialogflow with Virtual Agent Bot Interconnect, you must first create a new agent in Google Dialogflow.
2.  [Create a service account and private key for the Google Dialogflow project](../task/create-srvc-acct-key-dialogflow.md)  
To use Google Dialogflow with Virtual Agent Bot Interconnect, the second step is to create a service account and private key for the new agent in Google Dialogflow.
3.  [Generate a Java Keystore file from the JSON private key file](../task/generate-jks-from-json-dialogflow.md)  
To use Google Dialogflow with Virtual Agent Bot Interconnect, the third step is to generate a JKS file from the JSON private key you created in the previous step.
4.  [Configure connections to Google Dialogflow in your Virtual Agent Bot Interconnect instance](../task/configure-sn-instance-google-dialogflow.md)  
To use Google Dialogflow with Virtual Agent Bot Interconnect, the fourth step is to configure the connection in your ServiceNow® instance.
5.  [Create a Virtual Agent Bot Interconnect shell topic to call Google Dialogflow topics](../task/link-ggl-dialogflow-intents-va.md)  
To access topics in the Google Dialogflow secondary bot, you must create at least one Virtual Agent Bot Interconnect topic.

**Parent Topic:**[Using Virtual Agent Bot Interconnect in your configuration](using-sn-va-primary-bot-api.md)

