---
title: Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect
description: With Bot Interconnect, you can use ServiceNow Virtual Agent as the primary bot with a Microsoft Power Virtual Agents secondary bot. All of the skills and topics available to Power Virtual Agents are made available to and executable from channels that are configured for ServiceNow Bot Interconnect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/using-va-api-ms-powerva.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect

With Bot Interconnect, you can use ServiceNow® Virtual Agent as the primary bot with a Microsoft Power Virtual Agents secondary bot. All of the skills and topics available to Power Virtual Agents are made available to and executable from channels that are configured for ServiceNow® Bot Interconnect.

## Prerequisites

This bot configuration requires the following:

-   A Zurich ServiceNow instance
-   Virtual Agent Bot Interconnect Store application
-   A Microsoft Power Virtual Agents account for testing

1.  [Create a JavaScript function in Microsoft Azure using Visual Studio Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-js-function-azure-mspv-sec-bot.md)  
To use Power Virtual Agents with Virtual Agent Bot Interconnect, you must create a JavaScript function in Microsoft Azure using the sample code files in Bot Interconnect.
2.  [Locate and copy the Direct Line secret key in Microsoft Power Virtual Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/get-dl-secret-key-mspva.md)  
To use Power Virtual Agents with Virtual Agent Bot Interconnect, you must locate and copy the Direct Line security key in your Power Virtual Agents account.
3.  [Add the Direct Line secret key to your Virtual Agent Bot Interconnect instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/add-dl-secret-key-sn-instance.md)  
To use Power Virtual Agents with Virtual Agent Bot Interconnect, you must add the Direct Line security key as a credential in your Bot Interconnect instance.
4.  [Create a Virtual Agent Bot Interconnect shell topic to call Microsoft Power Virtual Agents topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-primary-va-topic-ms-pva.md)  
To access topics in the Power Virtual Agents secondary bot, you must create at least one Virtual Agent Bot Interconnect topic.

**Parent Topic:**[Using Virtual Agent Bot Interconnect in your configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/using-sn-va-primary-bot-api.md)

