---
title: Manage endpoint with Token support
description: Generate endpoint for webhooks in the third-party applications that support token authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can optionally remove the configuration of the endpoint from the connection. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.Configure an endpoint that listens to the webhook.Deactivate the endpoint to disable it from listening to the webhook. You can activate it back.Remove the endpoint configuration.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up external trigger endpoints, Conditional and event-driven inbound integration, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Manage endpoint with Token support

Generate endpoint for webhooks in the third-party applications that support token authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can optionally remove the configuration of the endpoint from the connection. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.

## Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've installed the required spoke plugin.

**Parent Topic:**[Set up external trigger endpoints](set-up-external-webhook-endpoints.md)

## Configure endpoint with Token support

Configure an endpoint that listens to the webhook.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Under the Endpoints heading, select **Configure** for the connection to set up an endpoint with token authentication support.

    ![Configure button for token authentication.](../images/configure-endpoint-token-support.png).

2.  In the Configure endpoint form, select Generate token.

    ![Generate token link.](../images/configure-endpoint-generate-token.png).

    The token is generated.

3.  To generate the endpoint, select **Activate**.

    ![Endpoint Activate button.](../images/configure-endpoint-token-click-activate.png)

    The endpoint URL is generated in the URL field.

    ![Endpoint is generated.](../images/configure-endpoint-endpoint-generated.png).

4.  To copy the endpoint, select the copy endpoint icon \(![Copy endpoint icon.](../images/copy-endpoint-icon.png)\)

    **Tip:** Keep the endpoint at a secure place to use later at the third-party application webhook.


## Deactivate endpoint with Token support

Deactivate the endpoint to disable it from listening to the webhook. You can activate it back.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  To deactivate the endpoint, do the steps.

2.  Select **Deactivate**.

3.  To confirm deactivation, select **Deactivate**.

4.  To activate again, on the connection record, select **Edit**.

5.  Select **Activate**.


## Deconfigure endpoint with Token support

Remove the endpoint configuration.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Select **Edit**.

    ![Edit button to edit the endpoint.](../images/endpoint-deconfigure-token-edit.png)

2.  Remove the token.

    ![Token field.](../images/endpoint-deconfigure-token-remove-token.png).

3.  Select **Update**.

4.  Select **Deconfigure**.

    The configuration for the endpoint is removed from the connection.


