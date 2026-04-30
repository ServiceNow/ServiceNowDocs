---
title: Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect
description: Virtual Agent Bot Interconnect enables you to use ServiceNow Virtual Agent as the primary bot with a ServiceNow Virtual Agent secondary bot.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect

Virtual Agent Bot Interconnect enables you to use ServiceNow® Virtual Agent as the primary bot with a ServiceNow Virtual Agent secondary bot.

## Prerequisites

In order to configure ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, you require the following setup:

-   Two Xanadu ServiceNow instances.
-   On the primary instance: Virtual Agent Bot Interconnect Store application
-   On the secondary instance:
    -   Virtual Agent API v3.8.x or later
    -   Virtual Agent API on the secondary instance must be in synchronous mode or asynchronous mode.

1.  [Use ServiceNow Virtual Agent as a secondary bot in synchronous or asynchronous mode](use-servicenow-virtual-agent-as-a-secondary-bot-in-synchronous-or-asynchronous-mode_0.md)  
Use ServiceNow Virtual Agent as a secondary bot in synchronous or asynchronous mode with Bot Interconnect.
2.  [Create a connection and credential in Virtual Agent Bot Interconnect](../task/create-connection-credential-two-sn-instances.md)  
To use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, configure the connection and credential records in the Bot Interconnect \(primary\) instance.
3.  [Create an auth token in the ServiceNow secondary instance](../task/create-auth-token-sn-secondary-instance.md)  
To use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, create an authentication token in the secondary instance.
4.  [Create a Virtual Agent Bot Interconnect shell topic to call Virtual Agent secondary topics](../task/create-va-topic-sn-primary-secondary-config.md)  
To use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, you must create at least one shell topic in Bot Interconnect.
5.  [Enable live agent connection on the primary instance](enable-live-agent-connection-on-the-secondary-instance.md)  
Enable live agent connection on the primary instance to route an interaction to a live agent on the secondary instance.
6.  [Debug Virtual Agent Bot Interconnect with a ServiceNow Virtual Agent secondary bot](../task/debug-bot-sn-sn-configuration.md)  
Debug Workflow Studio executions of your Virtual Agent Bot Interconnect and Virtual Agent secondary bot integration.

**Parent Topic:**[Using Virtual Agent Bot Interconnect in your configuration](using-sn-va-primary-bot-api.md)

