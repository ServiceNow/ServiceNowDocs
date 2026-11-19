---
title: Manage endpoint with Hash message support
description: Generate endpoint for webhooks in third-party applications that support hash message authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.Configure the endpoint that listens to the webhook.Deactivate the endpoint so that it stops listening to a webhook. However, you can activate it again.Remove the configuration of the endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/generate-endpoint-with-hash-message-support.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up external trigger endpoints, Conditional and event-driven inbound integration, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Manage endpoint with Hash message support

Generate endpoint for webhooks in third-party applications that support hash message authentication. The endpoint enables webhooks to connect with your ServiceNow instance. You can deactivate or remove the configuration of the endpoint from the connection when you want the endpoint to no longer listen to the external webhook.

## Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've installed the required spoke plugin.

**Parent Topic:**[Set up external trigger endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/set-up-external-webhook-endpoints.md)

## Configure endpoint with Hash message support

Configure the endpoint that listens to the webhook.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Under the Endpoints heading, select **Configure** for the connection to set up an endpoint with hash message authentication support.

    \[Omitted image "configure-hash-message-auth.png"\] Alt text: Configure button for hash message authentication.

2.  In the Configure endpoint form, select Generate secret.

    \[Omitted image "configure-endpoint-generate-secret.png"\] Alt text: Generate secret link.

    The secret is generated in the Secret field.

3.  To generate the endpoint that the external webhook uses to connect to your ServiceNow instance, select **Activate**.\[Omitted image "configure-endpoint-activate-endpoint.png"\] Alt text: Activate button.

    The value in the Header parameter name field becomes available after you generate the endpoint.\[Omitted image "configure-hash-auth-generate-endpoint.png"\] Alt text: Endpoint generated.

4.  To copy the endpoint, select the copy endpoint icon \(\[Omitted image "copy-endpoint-icon.png"\] Alt text: Copy endpoint icon.\)

    **Tip:** Keep the endpoint at a secure place to use later at the third-party application webhook.


## Deactivate endpoint with Hash message support

Deactivate the endpoint so that it stops listening to a webhook. However, you can activate it again.

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


## Deconfigure endpoint with Hash message support

Remove the configuration of the endpoint.

### Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: Integration Hub Enterprise pack

Ensure that you've installed the required spoke plugin.

### Procedure

1.  Select **Edit**.

    \[Omitted image "endpoint-deconfigure-hash-edit-button.png"\] Alt text: Edit button..

    1.  Select **Update**.

    2.  Select **Deconfigure**.

        The configuration for the endpoint is removed from the connection.

2.  Remove the secret.

    \[Omitted image "endpoint-deconfigure-hash-remove-secret.png"\] Alt text: Secret field..

3.  Select **Update**.

4.  Select **Deconfigure**.


