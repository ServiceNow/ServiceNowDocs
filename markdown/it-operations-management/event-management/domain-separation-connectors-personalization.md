---
title: Event Management Connectors domain personalization
description: Create events in different domains for all Event Management connectors using just a single connector instance by personalizing domain separation of Event Management connectors.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management Connectors domain personalization

Create events in different domains for all Event Management connectors using just a single connector instance by personalizing domain separation of Event Management connectors.

## How the domain is identified

In a ServiceNow instance, events are created within the logged-in or MID Server user domains. However, you can create events in a different domain by providing metadata values in the event HTTP request, including the URL, headers, request body \(payload\), and connector parameters.

The logged-in user or the MID Server user must have access to the provided domain. The connector resolves the domain based on the provided identifier and creates events in that domain.

System properties provide the default metadata that sets the domain-separated table to identify the domain. For more information, see [Domain properties installed with Event Management](../reference/installed-domain-properties.md).

## Connector Exceptions

You cannot personalize domain separation for the following pull connectors:

-   SCOM
-   IBM Netcool \(supports only IBM Netcool\_v2\)
-   HPOM
-   Hyperic

You cannot personalize domain separation for the following push connectors:

-   SAP SolMan Transform Script
-   bmcTrueSight Transform Script
-   Transform Generic Events MID
-   TransformEvents\_xmlSample

-   **[Personalize domains for pull connector events to use in event creation](../task/personalize-domain-separation-pull-connectors.md)**  
Configure pull connectors to personalize domain separation of events so you can use them to create events in domains other than the user's currently logged-in or MID Server domain.
-   **[Personalize domains for push connector events to use in event creation](../task/personalize-domain-separation-push-connectors.md)**  
Configure push connectors to personalize domain separation of events so you can use them to create events in different domains other than the user's currently logged-in or MID Server domain.

**Parent Topic:**[Event Management Integrations](c_EMEvent.md)

**Related topics**  


[Domain separation and Event Management](domain-separation-event-management.md)

