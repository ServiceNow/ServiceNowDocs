---
title: Integration Hub
description: Integration Hub is a prebuilt low-code platform for adding integrations to prebuilt connectors. Use Integration Hub to connect your custom app to third-party applications without having to write custom code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/dev-get-start-integration-hub.html
release: australia
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 2
keywords: [Integrations, low-code]
breadcrumb: [Integrations, Standard app development, Getting Started guide for developers, Building applications]
---

# Integration Hub

Integration Hub is a prebuilt low-code platform for adding integrations to prebuilt connectors. Use Integration Hub to connect your custom app to third-party applications without having to write custom code.

Integration Hub provides a visual interface for building integrations with prebuilt connectors, reusable actions, and integration with ServiceNow Workflow Studio. Integration Hub handles both directions of communication: sending data out to external systems and receiving data from them.

Consider using Integration Hub in any of the following scenarios:

-   Your app requires integration with a third-party application, such as Salesforce, Slack, Jira, or Microsoft Teams.
-   You prefer a low-code visual interface over writing REST code.
-   You want prebuilt connectors that handle authentication and transformation for you.
-   You want to create reusable integration actions for multiple workflows.
-   Your organization has limited development resources.

## How does Integration Hub work?

Integration Hub wraps the complexity of calling external APIs into reusable building blocks called spokes and actions. A spoke is a reusable integration connector to a specific third-party application. An action is a component that tells Integration Hub what messages to send or receive from the designated spoke. Instead of writing REST calls or SOAP messages directly, you select an action from Integration Hub, configure it with your parameters, and the integration handles the technical details. For more information, see [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub.md).

## Spokes: prebuilt connectors

Integration Hub provides prebuilt spokes for popular platforms like Slack, Microsoft Teams, Jira, Salesforce, and others. Each spoke includes ready-to-use actions that simplify common tasks, such as posting a message, creating an issue, or updating a record, without you having to write the API code. If Integration Hub doesn't have a prebuilt spoke for your system, you can build a custom one. For more information, see [Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/spokes-list.md).

## Custom integrations

When you want to integrate your custom app with a system that doesn't have a prebuilt spoke, you can build a custom integration directly in Workflow Studio using REST steps, SOAP steps, or script steps. This approach gives you full control over how data is formatted and sent, but requires more technical knowledge than using a prebuilt spoke. For more information, see [Integration steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-steps.md).

**Parent Topic:**[Integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-integrations.md)

