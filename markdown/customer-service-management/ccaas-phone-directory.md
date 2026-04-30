---
title: Phone directory
description: Agents can use the phone directory integrated into their ServiceNow instance to make outbound calls to queues, other agents, and external numbers. They can also enter a phone number directly in the global call list window or use the phone directory to make calls.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [icc\_search\_limit ServiceNow, icc\_search\_limit, ICC phone directory, ICC address book]
breadcrumb: [ICC for voice calls, Integrating with contact centers, Integrate, Customer Service Management]
---

# Phone directory

Agents can use the phone directory integrated into their ServiceNow instance to make outbound calls to queues, other agents, and external numbers. They can also enter a phone number directly in the global call list window or use the phone directory to make calls.

## Phone directory overview

![Telephone directory available in the call controls screen](../image/ccaas-phone-directory.png "Phone directory")

**Note:** The contact center admin must enable and configure the phone directory for the agents to view and use it in their global call list from their ServiceNow instance. Once the back end integration is done, the phone directory displays in CSM Configurable Workspace.

The following CCaaS Store Apps offer voice channel integration:

-   [Unified Experience from Genesys - Core](https://store.servicenow.com/store/app/6ebe67ea1b646a50a85b16db234bcb54)
-   [Unified Experience from Genesys](https://store.servicenow.com/store/app/cdff6b621ba46a50a85b16db234bcba3#linksAndDocuments)

The phone directory helps agents make outbound calls to contacts within their organization and external numbers. Organizations can integrate with any third-party CCaaS call integration feature that allows agents to access their contacts and queues via their integrated contact center. The phone directory displays tabs for queue, agent contacts, and external contacts, and the contact center admin can configure the number of contacts displayed. Use **Search** on the phone directory to display a list of a maximum of 25 results at a time. The limit can be set by configuring the system property setting called ‘icc\_search\_limit’ using an integer value. The default minimum value is 10, and a limit can be set to return a maximum of 25 results according to list of queues, agents, or external data.

When a call is made, a connecting screen displays with the call context details. If the context fails to display within a few seconds, the screen defaults back to the previous view with the phone directory tabs and dial pad.

For more information on ICC call features, see [Interaction Controls Component \(ICC\) call features](interaction-controls-component-icc-call-interaction-features.md) and [Implement the Interaction Controls Component \(ICC\) for contact center voice call and callback integration](../task/enable-icc-for-ccaas.md).

