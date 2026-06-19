---
title: Manage endpoint with OAuth 2.0 support
description: Manage endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication. The endpoint enables webhooks to connect with your ServiceNow instance.Configure endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication.Deactivate an active endpoint with OAuth 2.0 support while retaining the configurations to activate it later when needed.Deactivate an endpoint with OAuth 2.0 support to remove the existing configurations. Activate and configure the endpoint later when needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/generate-endpt-oauth2.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up external trigger endpoints, Conditional and event-driven inbound integration, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Manage endpoint with OAuth 2.0 support

Manage endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication. The endpoint enables webhooks to connect with your ServiceNow instance.

## Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've installed the required spoke plugin.

Ensure that you have created an OAuth application endpoint for the external client applications to access the ServiceNow instance. For more information about creating an inbound OAuth application endpoint, see .

-   If you want to create an OAuth application endpoint for external client applications to access the ServiceNow instance, see .
-   If you want to create an OAuth JWT API endpoint for external clients to access the ServiceNow instance, see .

**Parent Topic:**[Set up external trigger endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/set-up-external-webhook-endpoints.md)

## Configure endpoint with OAuth 2.0 support

Configure endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Under the Endpoints heading, select **Configure** for the connection to set up an endpoint with OAuth authentication support.

    \[Omitted image "oauth-endpoint-ext-trigger.png"\] Alt text: Configure button for OAuth authentication.

2.  In the Configure endpoint form, click \[Omitted image "select-roles-plus-icon.png"\] Alt text: Select roles icon. to add role in **Required roles**.

    To select one or more roles, select \[Omitted image "select-roles-drop-down.png"\] Alt text: Select roles icon. or enter the name of one or more roles.

    \[Omitted image "oauth-endpoint-ext-trigger-user.png"\] Alt text: Add required roles.

3.  Select the required application registry record.

4.  To generate the endpoint, select **Activate**.

    \[Omitted image "oauth-endpoint-ext-trigger-2.png"\] Alt text: Activate the endpoint.

    The endpoint URL is generated in **URL**.

    \[Omitted image "oauth-endpoint-ext-trigger-URL.png"\] Alt text: Copy the endpoint URL.

5.  To copy the endpoint, select the copy endpoint icon \(\[Omitted image "copy-endpoint-icon.png"\] Alt text: Copy endpoint icon.\)

    **Tip:** Keep the endpoint at a secure place to use later at the third-party application webhook.


## Deactivate endpoint with OAuth 2.0 support

Deactivate an active endpoint with OAuth 2.0 support while retaining the configurations to activate it later when needed.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Under the Endpoints heading, for the required endpoint, click **Edit**

2.  Click **Deactivate**.

    \[Omitted image "oauth-endpoint-ext-trigger-deactivate.png"\] Alt text: Deactivate the required endpoint.

3.  To confirm deactivation, select **Deactivate**.

    \[Omitted image "oauth-endpoint-ext-trigger-deactivate-conf.png"\] Alt text: Confirm to deactivate the required endpoint.

4.  To activate again, on the connection record, select **Edit**.

5.  Select **Activate**.

    \[Omitted image "oauth-endpoint-ext-trigger-activate.png"\] Alt text: Activate the required endpoint.


## Deconfigure endpoint with OAuth 2.0 support

Deactivate an endpoint with OAuth 2.0 support to remove the existing configurations. Activate and configure the endpoint later when needed.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Under the Endpoints heading, click the more options icon \(\[Omitted image "oauth-more-options-icon.png"\] Alt text:\).

    \[Omitted image "oauth-deconfigure.png"\] Alt text: Deconfigure the required endpoint.

2.  Click **Deconfigure**.

3.  When prompted, confirm your choice to deconfigure.

    \[Omitted image "oauth-deconfigure-confirmation.png"\] Alt text: Confirm to deconfigure.

    The configuration for the endpoint is removed from the connection.


