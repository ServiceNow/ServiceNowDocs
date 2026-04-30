---
title: Manage endpoint with Basic authentication support
description: Generate endpoint for webhooks in third-party applications that support basic authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.Configure the endpoint that listens to the webhook from a third-party application.Deactivate the endpoint so that it stops listening to a webhook. However, you can activate it again.Remove the configuration of the endpoint.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up external trigger endpoints, Conditional and event-driven inbound integration, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Manage endpoint with Basic authentication support

Generate endpoint for webhooks in third-party applications that support basic authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.

## Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've installed the required spoke plugin.

**Parent Topic:**[Set up external trigger endpoints](set-up-external-webhook-endpoints.md)

## Configure endpoint with Basic authentication support

Configure the endpoint that listens to the webhook from a third-party application.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Under the Endpoints heading, select **Configure** for the connection to set up an endpoint with basic authentication support.

    ![Configure button for basic auth.](../images/set-up-endpoint-basic-auth.png)

2.  To display the Add Role field, select ![Select roles icon.](../images/select-roles-plus-icon.png).

3.  To select one or more roles, select ![Select roles icon.](../images/select-roles-drop-down.png) or enter the name of one or more roles.

    ![Enter the roles.](../images/select-role-basic-auth.png)

4.  Select **Activate**.

    The endpoint for the third-party application webhook is generated in the URL field.

    ![Endpoint is generated.](../images/basic-auth-endpoint-generated.png)

5.  To copy the endpoint, select the copy endpoint icon \(![Copy endpoint icon.](../images/copy-endpoint-icon.png)\)

    **Tip:** Keep the endpoint at a secure place to use later at the third-party application webhook.


## Deactivate endpoint with Basic authentication support

Deactivate the endpoint so that it stops listening to a webhook. However, you can activate it again.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Select **Deactivate**.

2.  To confirm deactivation, select **Deactivate**.

3.  To activate again, on the connection record, select **Edit**.

4.  Select **Activate**.


## Deconfigure endpoint with Basic authentication support

Remove the configuration of the endpoint.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Select **Edit**.

    ![Edit button.](../images/endpoint-deconfigure-edit-button.png)

2.  Remove the roles.

    ![Remove roles.](../images/deconfigure-edit-remove-roles.png)

3.  Select **Update**.

4.  Select **Deconfigure**.

    The configuration for the endpoint is removed from the connection.


