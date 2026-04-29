---
title: Conditional and event-driven inbound integration
description: Integration Hub enables both conditional and event-driven inbound integration with third-party applications.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build integrations, Integration Hub, Workflow Data Fabric]
---

# Conditional and event-driven inbound integration

Integration Hub enables both conditional and event-driven inbound integration with third-party applications.

Set up an inbound integration with a third-party application by setting up flows and endpoints that external webhooks in the third-party application use. Set up a conditional and event-driven flow by selecting an external trigger from the new trigger picker and then setting the actions from the action picker on Workflow Studio. After that, set up endpoints that configure the external webhook from the third-party application. You perform all of these actions on your ServiceNow instance.

For example, you’re setting an inbound integration between your ServiceNow instance and a third-party issue-tracking application. When you update a P1 priority issue on the issue-tracking application, an incident database record on the ServiceNow instance should be updated.

To set the integration, configure a flow by selecting an external trigger from the new trigger picker, set the priority as P1, and then setting the actions from the action picker on the Workflow Studio accordingly. The flow accepts the payload from the issue-tracking application and updates the incident table. Then, you generate an endpoint on a base system external event source on your ServiceNow instance from the Application tile in the Inbound Connections tab and provide the same endpoint in the external webhook of the issue-tracking application. Now, when you update a P1 issue on the issue-tracking application, its external webhook activates and acts as a trigger for the flow you had set on your ServiceNow instance. Before that, the ServiceNow instance authenticates the webhook based on the type of authentication the issue-tracking application supports. After successful authentication, the webhook triggers the flow and the flow executes.

-   **[Set up a flow with external trigger definition](../tasks/set-up-flow-ihub.md)**  
Set up a flow that responds to an event-driven external trigger from a third-party system and executes.
-   **[Set up external trigger endpoints](../tasks/set-up-external-webhook-endpoints.md)**  
Generate an endpoint that the external webhook in the third-party application uses to connect to your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.

**Parent Topic:**[Building integrations in Integration Hub](building-integrations-ih.md)

