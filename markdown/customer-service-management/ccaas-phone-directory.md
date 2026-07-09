---
title: Phone directory
description: The phone directory enables agents to make outbound calls to queues, other agents, and external numbers from their ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ccaas-phone-directory.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [icc\_search\_limit ServiceNow, icc\_search\_limit, ICC phone directory, ICC address book]
breadcrumb: [ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Phone directory

The phone directory enables agents to make outbound calls to queues, other agents, and external numbers from their ServiceNow instance.

## Phone directory overview

\[Omitted image "ccaas-phone-directory.png"\] Alt text: Telephone directory available in the call controls screen

The phone directory helps agents make outbound calls to contacts within their organization and external numbers. Organizations can integrate with any third-party CCaaS call integration feature that enables agents to access their contacts and queues through their integrated contact center. The phone directory displays tabs for queue, agent contacts, and external contacts, and the contact center admin can configure the number of contacts displayed.

The contact center admin must enable and configure the phone directory for the agents to view and use it in their global call list from their ServiceNow instance. After the back-end integration is complete, the phone directory displays in CSM Configurable Workspace.

## Configuration

The contact center admin can configure the number of contacts displayed in each tab of the phone directory. The number of search results displayed can be configured and limited using the **icc\_search\_limit** system property. This property controls the maximum number of search results returned when agents perform searches, ensuring that search performance remains optimal while providing agents with relevant contact options. The search limit can be configured to return a maximum of 25 results.

The following CCaaS Store Apps offer voice channel integration:

-   [Unified Experience from Genesys - Core](https://store.servicenow.com/store/app/6ebe67ea1b646a50a85b16db234bcb54)
-   [Unified Experience from Genesys](https://store.servicenow.com/store/app/cdff6b621ba46a50a85b16db234bcba3#linksAndDocuments)

For more information on ICC call features, see [Interaction Controls Component \(ICC\) call features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/interaction-controls-component-icc-call-interaction-features.md) and [Implement the Interaction Controls Component \(ICC\) for contact center voice call and callback integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/enable-icc-for-ccaas.md).

## Phone directory Search

When a user performs a search in the phone directory search box, the system triggers a search event and exchanges data with your CCaaS provider. For example, when an agent enters a search query \(such as "John"\) and initiates a search, the **getSearchTarget** event triggers and is sent to your integrated CCaaS system. The system processes the search request and returns a response containing the **searchTargetList** parameter, which is a list of contact records that match the search criteria. If the **icc\_search\_limit** is set to 10, the **searchTargetList** will return up to 10 contact records matching the agent's search. The following diagram illustrates the technical interaction between the phone directory, the **getSearchTarget** event, and the CCaaS system.

For details on the s**earchTargetList** parameter, see [openFrameAPI - setICContext\(String Type, Object &lt;Context&gt;\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_openFrameAPI.md).

\[Omitted image "example-interaction-control-action-event.png"\] Alt text: This example illustrates the OpenFrame API technical interaction between the phone directory, the getSearchTarget event, and the CCaaS system.

For documentation on the search events and response structures, see the following OpenFrame API resources:

-   **getSearchTarget**

    [openFrameAPI - subscribe\(openFrameAPIEVENT event, function eventCallback\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_openFrameAPI.md)

-   **searchTargetList**

    [openFrameAPI - setICContext\(String Type, Object &lt;Context&gt;\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_openFrameAPI.md)


