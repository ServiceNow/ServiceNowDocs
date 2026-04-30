---
title: Manage endpoint with OAuth 2.0 support
description: Manage endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication. The endpoint enables webhooks to connect with your ServiceNow instance.Configure endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication.Deactivate an active endpoint with OAuth 2.0 support while retaining the configurations to activate it later when needed.Deactivate an endpoint with OAuth 2.0 support to remove the existing configurations. Activate and configure the endpoint later when needed.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up external trigger endpoints, Conditional and event-driven inbound integration, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Manage endpoint with OAuth 2.0 support

Manage endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication. The endpoint enables webhooks to connect with your ServiceNow instance.

## Before you begin

Role required: flow\_designer and connection\_admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've installed the required spoke plugin.

Ensure that you have created an OAuth application endpoint for the external client applications to access the ServiceNow instance. For more information about creating an inbound OAuth application endpoint, see [OAuth Inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   If you want to create an OAuth application endpoint for external client applications to access the ServiceNow instance, see [Create an endpoint for clients to access the instance](https://www.servicenow.com/docs/access?context=t_CreateEndpointforExternalClients&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
-   If you want to create an OAuth JWT API endpoint for external clients to access the ServiceNow instance, see [Create an OAuth JWT API endpoint for external clients \(machine to machine integration\)](https://www.servicenow.com/docs/access?context=create-jwt-endpoint&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Parent Topic:**[Set up external trigger endpoints](set-up-external-webhook-endpoints.md)

## Configure endpoint with OAuth 2.0 support

Configure endpoint for webhooks in third-party applications that support the OAuth 2.0 authentication.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Under the Endpoints heading, select **Configure** for the connection to set up an endpoint with OAuth authentication support.

    ![Configure button for OAuth authentication.](../images/oauth-endpoint-ext-trigger.png)

2.  In the Configure endpoint form, click ![Select roles icon.](../images/select-roles-plus-icon.png) to add role in **Required roles**.

    To select one or more roles, select ![Select roles icon.](../images/select-roles-drop-down.png) or enter the name of one or more roles.

    ![Add required roles.](../images/oauth-endpoint-ext-trigger-user.png)

3.  Select the required application registry record.

4.  To generate the endpoint, select **Activate**.

    ![Activate the endpoint.](../images/oauth-endpoint-ext-trigger-2.png)

    The endpoint URL is generated in **URL**.

    ![Copy the endpoint URL.](../images/oauth-endpoint-ext-trigger-URL.png)

5.  To copy the endpoint, select the copy endpoint icon \(![Copy endpoint icon.](../images/copy-endpoint-icon.png)\)

    **Tip:** Keep the endpoint at a secure place to use later at the third-party application webhook.


## Deactivate endpoint with OAuth 2.0 support

Deactivate an active endpoint with OAuth 2.0 support while retaining the configurations to activate it later when needed.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Under the Endpoints heading, for the required endpoint, click **Edit**

2.  Click **Deactivate**.

    ![Deactivate the required endpoint.](../images/oauth-endpoint-ext-trigger-deactivate.png)

3.  To confirm deactivation, select **Deactivate**.

    ![Confirm to deactivate the required endpoint.](../images/oauth-endpoint-ext-trigger-deactivate-conf.png)

4.  To activate again, on the connection record, select **Edit**.

5.  Select **Activate**.

    ![Activate the required endpoint.](../images/oauth-endpoint-ext-trigger-activate.png)


## Deconfigure endpoint with OAuth 2.0 support

Deactivate an endpoint with OAuth 2.0 support to remove the existing configurations. Activate and configure the endpoint later when needed.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Under the Endpoints heading, click the more options icon \(![](../images/oauth-more-options-icon.png)\).

    ![Deconfigure the required endpoint.](../images/oauth-deconfigure.png)

2.  Click **Deconfigure**.

3.  When prompted, confirm your choice to deconfigure.

    ![Confirm to deconfigure.](../images/oauth-deconfigure-confirmation.png)

    The configuration for the endpoint is removed from the connection.


