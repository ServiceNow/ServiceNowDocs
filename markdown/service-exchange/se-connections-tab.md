---
title: Connections tab
description: The Connections tab in the Provider Center and Consumer Center lists your Service Exchange connections. Provider Center also shows registration requests that are created when a provider adds a consumer. After the provider completes registration and shares the onboarding URL, the consumer uses Consumer Center to continue onboarding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-connections-tab.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [connections tab, connection cards, Provider Center, Consumer Center, registration status]
breadcrumb: [Service Exchange Center, Explore, Service Exchange]
---

# Connections tab

The Connections tab in the Provider Center and Consumer Center lists your Service Exchange connections. Provider Center also shows registration requests that are created when a provider adds a consumer. After the provider completes registration and shares the onboarding URL, the consumer uses Consumer Center to continue onboarding.

The **Connections** tab displays all in-progress and onboarded connections . In Provider Center, in-progress registration requests appear first, followed by onboarded connections. In Consumer Center, in-progress onboarding entries appear first, followed by onboarded connections. Within each group, the most recently updated entry appears first.

Each card shows the company name, connection or registration request number, instance URL, current state, application version, and contact details. For onboarded connections, the card also displays location details. Fields with no value are hidden.

You can search by company name, connection number, instance URL, version, or state. Use the state filter to show connections in a specific state. The filter options like registration and connection states and the states that apply to your provider or consumer views.

The connection card status shows the registration or connection state and is independent of the health status \(Up, Slow, or Down\) shown on the **Health** tab.\[Omitted image "se-health-dashboard-connections.png"\] Alt text: The Connection tab displays list of registered connections with their details.

## How to access

The **Connections** tab is available in both the **Provider Center** and **Consumer Center**. Access it from the Administration menu within the respective applications. Use Provider Center to add a consumer, create and manage the registration task, and share the onboarding URL. Use Consumer Center after the provider shares the onboarding URL to start or resume onboarding. If the instance supports both roles, you can switch between the provider and consumer views.

## Benefits

-   Consolidated view of all connections across all stages of onboarding.
-   Quick visibility into connection states without navigating to individual records.
-   Simplified search and filtering to locate connections by name, version, or status.
-   Direct access to registration details and connection settings from each connection card.
-   Option to resume an interrupted registration as a consumer.

## Connection actions and states

The following table lists the connection actions. The available actions depend on the connection state and your instance role.

|Action|View|Description|
|------|----|-----------|
|New connection|Provider|Opens the **Create a new connection** form to add a consumer and create the provider-side registration task.|
|Setup connection|Consumer|Starts or resumes the consumer onboarding process after the provider completes registration and shares the onboarding URL. The entry point depends on the onboarding state.|
|View details|Provider and Consumer|Opens the connection details page. On the provider side, the default tab is **Registration task** if the connection isn't onboarded, and **Settings** if it is. On the consumer side, only the **Settings** tab appears.|
|Offboard Consumer|Provider|Offboards the consumer from the connection details page. If offboarding succeeds, the **Connections** tab opens with a confirmation message. If offboarding fails, an error message appears on the connection details page.|
|Offboard Provider|Consumer|Offboards the provider from the connection details page. If offboarding succeeds, the **Connections** tab opens with a confirmation message. If offboarding fails, an error message appears on the connection details page.|

The connection details page displays the name of the provider or consumer company name as the title and the date the connection was established as the subtitle. The page also displays connection details such as the connection number, contact, outbound and inbound status, and version.

-   **Connection states**

    Each connection card displays the current state of the connection. The state changes as the connection moves through registration and onboarding. The following table describes the connection states.

    |State|Description|
    |-----|-----------|
    |Pending|The provider has added the consumer and created the registration request. The consumer hasn't started onboarding because the onboarding URL hasn't been used yet.|
    |Awaiting Validation|The consumer has opened the onboarding URL and started onboarding. The system creates the connection record and runs the pre-onboarding checks.|
    |Validated|The pre-onboarding checks pass and the connection is ready for the consumer to continue onboarding.|
    |Validation Failed|One or more pre-onboarding checks fail. Resolve the issues to continue consumer registration.|
    |Onboarded|Onboarding is complete. The provider and consumer instances are connected.|


**Related topics**  


[Register a consumer from the Provider Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-provider-center-onboarding.md)

[Consumer registration from the Consumer Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-consumer-center-onboarding.md)

