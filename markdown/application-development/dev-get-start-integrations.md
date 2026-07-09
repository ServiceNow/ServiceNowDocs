---
title: Integrations
description: Integrations enable you to connect your custom app to external systems to send and receive data. The ServiceNow AI Platform supports multiple integration capabilities to fit your use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/dev-get-start-integrations.html
release: australia
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 2
keywords: [Integrations, low-code]
breadcrumb: [Standard app development, Getting Started guide for developers, Building applications]
---

# Integrations

Integrations enable you to connect your custom app to external systems to send and receive data. The ServiceNow AI Platform supports multiple integration capabilities to fit your use case.

Custom applications often exchange data with external systems. For example, you might need to pull data from a third-party API or send push notifications to an external service. An integration enables your custom app to connect to an external system to exchange data.

Integrations can enable your app to both send data out to other systems and receive data from other systems. Integrations also synchronize data across platforms and trigger workflows based on external events.

## Integration types

There are different types of integrations based on the data being exchanged. ServiceNow AI Platform supports the following types of integrations:

-   **[Inbound web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-inbound-web-services.md)**

    Receive data from external systems to your custom app. Use inbound web services to enable external services to push data to your app, such as form submissions, event notifications, or data synchronization from upstream systems.

-   **[Outbound web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-outbound-web-services.md)**

    Send data from your custom app to external systems. Use outbound web services to notify external services about events or updates in your app. Common use cases include triggering webhooks, sending alerts to collaboration tools, and updating external records.

-   **[Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-integration-hub.md)**

    Provides a low-code platform to build integrations with prebuilt connectors and reusable actions. Use Integration Hub to integrate your app with popular third-party applications without writing custom code.

-   **Remote tables**

    Displays and works with external data directly in your app without having to store information locally. Remote tables fetch data on-demand from external sources and cache it temporarily. Use remote tables when you need read-only access to external data with familiar ServiceNow AI Platform list and form interfaces.


## Decide which integration to use

When deciding which integrations to configure for your custom application, ask yourself the following questions:

-   Does your app send data out, receive data in, or both?
-   Is the external system a popular third-party app \(Salesforce, Slack, or similar tools\) or a custom system?
-   Do you need real-time synchronization, or is periodic data retrieval sufficient?
-   Does your app store external data, or can it cache temporary records?

-   **[Inbound web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-inbound-web-services.md)**  
Inbound web services enable external systems to read data from or write data to your custom application. External systems can query your data, create records, or exchange information.
-   **[Outbound web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-outbound-web-services.md)**  
Outbound web services send data from your custom app to external systems. With outbound web services, your app can notify, request, or update external platforms in real time or on a schedule.
-   **[Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-integration-hub.md)**  
Integration Hub is a prebuilt low-code platform for adding integrations to prebuilt connectors. Use Integration Hub to connect your custom app to third-party applications without having to write custom code.

**Parent Topic:**[Standard app development in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/overview-building-apps-in-servicenow.md)

