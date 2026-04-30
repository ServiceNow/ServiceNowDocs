---
title: Set up external trigger endpoints
description: Generate an endpoint that the external webhook in the third-party application uses to connect to your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Set up external trigger endpoints

Generate an endpoint that the external webhook in the third-party application uses to connect to your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.

## Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've installed the required spoke plugin.

## About this task

The connections that enable you to set up endpoints become available as base system contents on your ServiceNow instance when you install the spoke plugin from the ServiceNow store. After that, you can generate endpoints with basic authentication, token, or hash authentication mechanisms based on the type of authentication the third-party application supports. When the webhook attempts to connect with your ServiceNow instance, it's first authenticated with the authentication method set up in the endpoint connection.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Connections**.

3.  In the Search all connections field, enter the name of the spoke.

    The spoke connection card appears with the **Inbound** tab selected by default.![Inbound tab for spokes.](../images/inbound-tab.png)

4.  Select **View Details**.

5.  Set up external trigger endpoints with different authentication types.

    1.  [Manage endpoint with Basic authentication support](set-up-endpoint-external-trigger-with-basic-authentication.md#).

    2.  [Manage endpoint with Hash message support](generate-endpoint-with-hash-message-support.md#).

    3.  [Manage endpoint with Token support](generate-endpoint-with-token-support.md#).

    4.  [Manage endpoint with OAuth 2.0 support](generate-endpt-oauth2.md#)


-   **[Manage endpoint with Basic authentication support](set-up-endpoint-external-trigger-with-basic-authentication.md#)**  
Generate endpoint for webhooks in third-party applications that support basic authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.
-   **[Manage endpoint with Hash message support](generate-endpoint-with-hash-message-support.md#)**  
Generate endpoint for webhooks in third-party applications that support hash message authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.
-   **[Manage endpoint with Token support](generate-endpoint-with-token-support.md#)**  
Generate endpoint for webhooks in the third-party applications that support token authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can optionally remove the configuration of the endpoint from the connection. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.
-   **[Manage endpoint with OAuth 2.0 support](generate-endpt-oauth2.md#)**  
Manage endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication. The endpoint enables webhooks to connect with your ServiceNow instance.

**Parent Topic:**[Conditional and event-driven inbound integration](../concept/conditional-and-event-driven-inbound-integration.md)

