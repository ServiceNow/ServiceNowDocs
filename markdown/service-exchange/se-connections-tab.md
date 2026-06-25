---
title: Connections
description: Use the Connections tab in the Provider Center and Consumer Center to add, monitor, and manage your Service Exchange connections from a single location.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-connections-tab.html
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-06-03"
reading_time_minutes: 2
keywords: [connections tab, connection cards, Provider Center, Consumer Center, registration status]
breadcrumb: [Service Exchange Center, Explore, Service Exchange]
---

# Connections

Use the Connections tab in the Provider Center and Consumer Center to add, monitor, and manage your Service Exchange connections from a single location.

The **Connections** tab displays each connection as a card. Each card shows the company name, connection number, instance URL, and the current state of the connection. For onboarded connections, the card also displays the application version and location details.

You can search various details from the search bar. You can filter the connection by the available connection status.

## How to access

The **Connections** tab is available in both the **Provider Center** and **Consumer Center**, depending on your instance role. Access it from the Administration menu within the respective center. The view reflects your role entry point, with the option to switch between provider and consumer views when both roles are supported.

## Benefit

-   Consolidated view of all connections across all stages of onboarding.
-   Quick visibility into connection states without navigating to individual records.
-   Simplified search and filtering to locate connections by name, version, or status.
-   Direct access to registration details and connection settings from each connection card.
-   Resume onboarding as a consumer when the process is interrupted.

## Connection card

Apart from viewing connection details, you can perform several actions from the connection card. The available actions depend on the connection state and your instance role.

|Action|View|Description|
|------|----|-----------|
|Setup connection|Consumer|Resumes the registration process from its current state.|
|View details|Provider and Consumer|Displayed when the connection is onboarded. On the provider side, this shows two tabs: **Registration** and **Settings**. On the consumer side, only the **Settings** tab is displayed.|

-   **Connection states**

    Each connection card displays one of the following states.

    |State|Description|
    |-----|-----------|
    |Awaiting Validation|The connection request has been created but pre-onboarding checks have not started.|
    |Validated|Pre-onboarding checks have passed and the connection is ready for registration.|
    |Validation Failed|One or more pre-onboarding checks have failed. The issues must be resolved before registration can proceed.|
    |Onboarded|Registration is complete and the connection between the provider and consumer instances is established.|


**Related topics**  


[Register a consumer from the Provider Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-provider-center-onboarding.md)

[Consumer registration from the Consumer Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-consumer-center-onboarding.md)

