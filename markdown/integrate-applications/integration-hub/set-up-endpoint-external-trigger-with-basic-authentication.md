---
title: Manage endpoint with Basic authentication support
description: Generate endpoint for webhooks in third-party applications that support basic authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.Configure the endpoint that listens to the webhook from a third-party application.Deactivate the endpoint so that it stops listening to a webhook. However, you can activate it again.Remove the configuration of the endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/set-up-endpoint-external-trigger-with-basic-authentication.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up external trigger endpoints, Conditional and event-driven inbound integration, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Manage endpoint with Basic authentication support

Generate endpoint for webhooks in third-party applications that support basic authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.

## Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've installed the required spoke plugin.

**Parent Topic:**[Set up external trigger endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/set-up-external-webhook-endpoints.md)

## Configure endpoint with Basic authentication support

Configure the endpoint that listens to the webhook from a third-party application.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Under the Endpoints heading, select **Configure** for the connection to set up an endpoint with basic authentication support.

    \[Omitted image "set-up-endpoint-basic-auth.png"\] Alt text: Configure button for basic auth.

2.  To display the Add Role field, select \[Omitted image "select-roles-plus-icon.png"\] Alt text: Select roles icon..

3.  To select one or more roles, select \[Omitted image "select-roles-drop-down.png"\] Alt text: Select roles icon. or enter the name of one or more roles.

    \[Omitted image "select-role-basic-auth.png"\] Alt text: Enter the roles.

4.  Select **Activate**.

    The endpoint for the third-party application webhook is generated in the URL field.

    \[Omitted image "basic-auth-endpoint-generated.png"\] Alt text: Endpoint is generated.

5.  To copy the endpoint, select the copy endpoint icon \(\[Omitted image "copy-endpoint-icon.png"\] Alt text: Copy endpoint icon.\)

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

    \[Omitted image "endpoint-deconfigure-edit-button.png"\] Alt text: Edit button.

2.  Remove the roles.

    \[Omitted image "deconfigure-edit-remove-roles.png"\] Alt text: Remove roles.

3.  Select **Update**.

4.  Select **Deconfigure**.

    The configuration for the endpoint is removed from the connection.


