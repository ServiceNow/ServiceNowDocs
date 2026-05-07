---
title: Set up the Microsoft Teams Graph spoke
description: Integrate the ServiceNow instance and Microsoft Teams account by creating a custom OAuth application in Microsoft Azure portal to authenticate ServiceNow requests.Provide authorization to the ServiceNow instance by registering an application in Microsoft Entra ID \(formerly Microsoft Azure Active Directory\).Add and configure the Microsoft Teams connections to authenticate ServiceNow requests in the Microsoft Teams Graph spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Microsoft Teams Graph Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Teams Graph spoke

Integrate the ServiceNow instance and Microsoft Teams account by creating a custom OAuth application in Microsoft Azure portal to authenticate ServiceNow requests.

Demonstrates how to set up the Microsoft Teams Graph spoke.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Teams Graph spoke.
-   Role required: admin.

## Register an application using the Microsoft Azure portal

Provide authorization to the ServiceNow instance by registering an application in Microsoft Entra ID \(formerly Microsoft Azure Active Directory\).

### Before you begin

Role required: Microsoft Entra ID admin

### About this task

Complete these steps from the Microsoft Azure portal.

### Procedure

1.  In the Microsoft Azure portal, copy and record the **Directory ID** for later use.

    For more information, see [Get tenant and app ID values for signing in](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal#get-tenant-and-app-id-values-for-signing-in) in [Microsoft Entra ID documentation](https://docs.microsoft.com/en-gb/).

2.  Register your application in Azure portal. For instructions on registering an application, see [Tutorial: Register an app with Microsoft Entra ID](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/walkthrough-register-app-azure-active-directory) in the [Microsoft Docs](https://docs.microsoft.com/en-us/).

3.  Copy and record the **Application ID** for later use.

4.  Add the **Redirect URL** in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

    For more information, see [Authentication and authorization for Azure Time Series Insights API](https://docs.microsoft.com/en-us/azure/time-series-insights/time-series-insights-authentication-and-authorization) in [Microsoft Docs](https://docs.microsoft.com/en-us/).

5.  For the **Required Permissions**, select **Microsoft Graph**.

    For more information, see [Permissions and consent in the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-permissions-and-consent) in [Microsoft Docs](https://docs.microsoft.com/en-us/).

    For information about the permissions required to use the spoke actions, see the Spoke actions section in [Microsoft Teams Graph Spoke](../concept/msteams-spoke.md). Provide permissions as per your requirement. For more information about the permissions, see [Microsoft Graph REST API v1.0 reference](https://docs.microsoft.com/en-us/graph/api/overview?view=graph-rest-1.0) in [Microsoft Docs](https://docs.microsoft.com/en-us/).

6.  Record the **Client Secret** for use in later configurations.


### Result

The ServiceNow application is created with Microsoft Entra ID.

## Configure connections for the Microsoft Teams Graph spoke

Add and configure the Microsoft Teams connections to authenticate ServiceNow requests in the Microsoft Teams Graph spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Configure the **Microsoft Teams Spoke** connection.

    1.  Locate the **Microsoft Teams Spoke** connection alias and select **View Details**.

        -   To configure the default connection and credential alias record that is shipped along with the Microsoft Teams spoke, select **View Details**.

            ![Connection for the Microsoft Teams Spoke](../image/ms-teams-spoke-tile.jpg)

        -   To manage more than one Microsoft Teams spoke connection records, you should create a child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
        If you're configuring the spoke for the first time, select **Configure**. Otherwise, select **Edit**.

        ![Initial connection configuration](../image/ms-teams-spoke-configure.jpg)

    2.  On the form, fill in these fields:

<table id="table_shd_vqw_byb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the alias record associated with this connection.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL. Enter `https://graph.microsoft.com`.

</td></tr><tr><td>

API Version

</td><td>

The value is set to **v1.0** by default.If you're using any other API version, update the version number here.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`.

</td></tr><tr><td>

Token Revocation URL

</td><td>

OAuth server token revocation endpoint.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application ID created during application registration.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret created during application registration.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>        ![Configure a connection for the Microsoft Teams spoke](../image/ms-teams-spoke-conf-connection.jpg)

    3.  Select **Save and Get OAuth Token**.

5.  Configure the **Microsoft Teams Graph Client Credentials** connection.

    Except the Look up Schedules action, all the other calendar and webhook management spoke actions use this connection record.

    1.  Locate the **Microsoft Teams Graph Client Credentials** connection alias and select **View Details**.

        -   To configure the default connection and credential alias record that is shipped along with the Microsoft Teams Graph Client Credentials, select **View Details**.

            ![Connection for the Microsoft Teams Graph Client Connection](../image/ms-teams-gphcc-tile.jpg)

        -   To manage more than one Microsoft Teams Graph Client Credentials connection records, you should create a child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
        If you're configuring the spoke for the first time, select **Configure**. Otherwise, select **Edit**.

        ![Initial connection configuration](../image/ms-teams-gphcc-configure.jpg)

    2.  On the form, fill in these fields:

<table id="table_bwd_xpw_byb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the alias record associated with this connection.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL. Enter `https://graph.microsoft.com`.

</td></tr><tr><td>

API Version

</td><td>

The value is set to **v1.0** by default.If you're using any other API version, update the version number here.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application ID created during application registration.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret created during application registration.

</td></tr></tbody>
</table>        ![Configure a connection for the Microsoft Teams Graph Client Credentials](../image/ms-teams-gphcc-conf-connection.jpg)

    3.  Select **Save and Get OAuth Token**.


### Result

The Microsoft Teams Graph spoke is set up and Microsoft Teams account is integrated with your ServiceNow instance.

