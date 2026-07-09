---
title: Set up Microsoft Exchange Online spoke
description: Integrate the ServiceNow instance and Microsoft Exchange Online account by creating a custom OAuth application in Microsoft Exchange Online to authenticate ServiceNow requests.Provide authorization to the ServiceNow instance by registering an application with Azure AD.Perform actions in Microsoft Exchange Online by configuring connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.Create a credential record for the Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential alias uses these credentials to authorize Mailbox actions.Configure a connection record for your Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential aliases use these connections to perform only Mailbox actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/setup-ms-exch-ol.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Microsoft Exchange Online Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Microsoft Exchange Online spoke

Integrate the ServiceNow instance and Microsoft Exchange Online account by creating a custom OAuth application in Microsoft Exchange Online to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Exchange Online spoke.
-   Role required: admin.

## Register an application using the Microsoft Azure portal

Provide authorization to the ServiceNow instance by registering an application with Azure AD.

### Before you begin

Role required: Azure Active Directory admin

### About this task

Complete these steps from the Microsoft Azure portal. For instructions on registering an application, see the [Microsoft Azure documentation](https://docs.microsoft.com/en-gb/).

### Procedure

1.  In the Microsoft Azure portal, add the **Redirect URIs** in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`

2.  For the **Required Permissions**, select **Microsoft Graph**.

    **Note:** The permissions displayed here are needed to use all the spoke actions. However if you want to use only some of the actions, you can add only the required permissions. For more information about the required permissions for each action, see [Spoke actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/ms-exch-online-spoke.md).

    \[Omitted image "ms-exchange-online-spoke-permissions.png"\] Alt text: Permissions required for Microsoft Exchange Online spoke

3.  Record the **Client Secret** for use in later configurations.


### Result

The ServiceNow application is created with Microsoft Azure AD.

## Configure connection records for the Microsoft Exchange Online spoke

Perform actions in Microsoft Exchange Online by configuring connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Locate the **Microsoft\_Exchange\_Online** connection alias.

3.  For **Configuration Template**, ensure that **Microsoft Exchange Online Authorization Code** is selected.

4.  Click the Create New Connection &amp; Credential related link.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Name|Name to uniquely identify the connection. For example, `Microsoft_Exchange_Online`.|
    |Connection URL|Enter `https://graph.microsoft.com`.|
    |API Version|Enter `v1.0`.|
    |Credential Information|
    |Name|Name to identify the credential record. For example, `Exchange_Online Creds`.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`|
    |Token Revocation URL|OAuth server token revocation endpoint.|
    |OAuth Client ID|Application ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|
    |OAuth Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`|

6.  Click **Create and Get OAuth Token**.

7.  Click the **Child Aliases** tab.

8.  Click the **Microsoft\_Exchange\_Online\_clientCred** connection record.

9.  Click the Create New Connection &amp; Credential related link.

10. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Name|Name to uniquely identify the connection. For example, `Microsoft_Exchange_Online_ClientCred`.|
    |Connection URL|Enter `https://graph.microsoft.com`.|
    |Credential Information|
    |Name|Name to identify the credential record. For example, `Exchange_Online_ClientCred Creds`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`|
    |OAuth Client ID|Application ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|

11. Click **Create and Get OAuth Token**.


### Result

The Microsoft Exchange Online spoke is set up and integrated with the ServiceNow instance.

## Create a credential record for the Microsoft Exchange Online spoke Mailbox actions

Create a credential record for the Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential alias uses these credentials to authorize Mailbox actions.

### Before you begin

-   Make sure that MID Server is setup and configured
-   Make sure that Power Shell with EXO V2 module is installed. This module is required for executing Mailbox management actions.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **Windows Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, MS Exchange Online Mailbox Cred.|
    |Active|Option to actively use the credential record.|
    |User name|UPN or login ID of the Entra ID user.|
    |Password|Password of the Entra ID user.|
    |Applies to|Option to specify if the credential applies to all MID Servers in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use this credential in the **MID servers** field.|
    |Order|Order to apply this credential. For example, `100`.|
    |Credential alias|Credential alias associated with the spoke.|

5.  Right-click the form header and click **Submit**.


### Result

A Windows Credential record is created for the Microsoft Exchange Online spoke Mailbox actions.

## Configure a connection record for the Microsoft Exchange Online spoke Mailbox actions

Configure a connection record for your Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential aliases use these connections to perform only Mailbox actions.

### Before you begin

-   Make sure that MID Server is setup and configured
-   Make sure that Power Shell with EXO V2 module is installed. This module is required for executing Mailbox management actions.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the **Microsoft Exchange Online MID** record.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `MS Exchange Online Mailbox Connection`.|
    |Credential|Credential record created for Microsoft Exchange Online spoke Mailbox actions. For example, `MS Exchange Online Mailbox Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |Connection URL|Base URL to connect to **Microsoft Exchange Online**. Enter: `127.0.0.1`|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use MID Servers for this connection. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.|

5.  Click **Submit**.


### Result

A connection record is created for Microsoft Exchange Online spoke Mailbox actions.

