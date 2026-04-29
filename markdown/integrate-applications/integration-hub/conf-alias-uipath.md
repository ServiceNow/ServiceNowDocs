---
title: Set up the UiPath spoke
description: Integrate the ServiceNow instance with your UiPath account to authenticate ServiceNow requests.Integrate the ServiceNow instance with your UiPath account using OAuth to authenticate ServiceNow requests.Integrate the ServiceNow instance with your UiPath account using API key to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [UiPath Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the UiPath spoke

Integrate the ServiceNow instance with your UiPath account to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the UiPath spoke.
-   Role required: admin.

## About this task

You can set up the UiPath spoke using OAuth authentication or API key as per your requirement.

-   See [Option 1: Using OAuth authentication](conf-alias-uipath.md#) to set up the UiPath spoke using OAuth authentication.
    -   This authentication is available from UiPath spoke v2.2.1.
    -   You can't use MID Server if you set up the spoke using OAuth authentication.
-   See [Option 2: Using API key](conf-alias-uipath.md#) to set up the UiPath spoke using API key.

## Option 1: Using OAuth authentication

Integrate the ServiceNow instance with your UiPath account using OAuth to authenticate ServiceNow requests.

### Before you begin

Role required: admin

**Note:**

-   This authentication is available from UiPath spoke v2.2.1.
-   You can't use MID Server if you set up the spoke using OAuth authentication.

### Procedure

1.  Register an application in your UiPath account.

    1.  Log in to your UiPath account as an admin.

    2.  Navigate to **Admin** &gt; **External Applications**.

    3.  Click **+ Add Application**.

    4.  On the form, fill these values.

<table id="table_nc5_4kg_q5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application Name

</td><td>

Name of the OAuth application.

</td></tr><tr><td>

Application Type

</td><td>

Type of OAuth application. Select **Confidential application**.

</td></tr><tr><td>

Resources

</td><td>

Required resource and scopes.1.  Click **+ Add Scopes**.
2.  Select **Orchestrator API Access** from the **Resource** list.
3.  Select these application scopes:
    -   OR.Robots.Read
    -   OR.Robots.Write
    -   OR.Jobs.Read
    -   OR.Jobs.Write
    -   OR.Machines.Read
    -   OR.Execution.Read
    -   OR.Queues.Read
    -   OR.Queues.Write
    -   OR.Folders.Read
4.  Click **Save**.


</td></tr><tr><td>

Redirect URL

</td><td>

ServiceNow instance redirect URL in this format: `https://<ServiceNow-instance>.service-now.com/oauth_redirect.do`

</td></tr></tbody>
</table>    5.  Click **Add**.

        The application is registered and values of App ID and App Secret are displayed.

    6.  Copy and record the values of app ID and app secret.

2.  In your ServiceNow instance, configure the required connection and credential alias.

    1.  Log in to your ServiceNow instance as an admin.

    2.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    3.  Open the record for **UiPath**.

    4.  For **Configuration Template**, select **UiPath Configuration Template - OAuth Client Credentials**.

    5.  Click the **Create New Connection &amp; Credential** related link.

    6.  On the form, fill these fields.

        |Field|Description|
        |-----|-----------|
        |Connection information|
        |Name|Name to identify the OAuth application registry record.|
        |Connection URL|Connection URL in this format: `https://{base_url}/{organization_name}/{tenant-name}/orchestrator_`. This URL depends on the type of UiPath deployment.|
        |Credential information|
        |Name|Name to identify the credential record.|
        |Token URL|Location of the token endpoint that the instance uses to retrieve and refresh tokens. This URL depends on the type of UiPath deployment.|
        |OAuth Client ID|App ID you had copied after registering application in your UiPath account.|
        |OAuth Client Secret|App secret you had copied after registering application in your UiPath account.|
        |OAuth Redirect URL|ServiceNow instance redirect URL in this format: `https://<ServiceNow-instance>.service-now.com/oauth_redirect.do`.|

    7.  Click **Create**.

    8.  Click **Submit**.

        Connection and credential records are created.

    9.  Open the UiPath Connection record, from the **Connections** tab.

    10. Select a value for the **Orchestrator Feature Enabled** field.


### Result

The Connection and Credential alias is configured and the UiPath spoke is set up using OAuth authentication.

## Option 2: Using API key

Integrate the ServiceNow instance with your UiPath account using API key to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  From your UiPath cloud account, obtain the values of the required API refresh tokens.

    **Note:** These steps are applicable to UiPath cloud account.

    1.  Log in to your UiPath account as an admin.

    2.  Navigate to **Preferences** &gt; **Privacy &amp; Security**.

    3.  For the required tenant, click **View API access**.

        The values of **User Key**, **Organization ID**, **Tenant Name**, and **Client ID** are displayed.

    4.  Copy and record these values.

2.  In your ServiceNow instance, configure the required connection and credential alias.

    1.  Log in to your ServiceNow instance as an admin.

    2.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    3.  Open the record for **UiPath**.

    4.  For **Configuration Template**, select **UiPath Configuration Template - UiPath Cloud** or **UiPath Configuration Template - Private/Public Cloud** as per your requirement.

    5.  Click the **Create New Connection &amp; Credential** related link.

    6.  On the form, fill these fields.

        -   If you have selected **UiPath Configuration Template - UiPath Cloud** for **Configuration Template**, fill these fields.

            **Note:** This option is applicable if you are using UiPath cloud account.

            |Field|Description|
            |-----|-----------|
            |Connection Name|Name to identify the connection record. For example, `UiPath Connection`.|
            |Connection URL|Connection URL in this format: `https://platform.uipath.com/<account-logical-name>/<instance-logical-name>`|
            |Credential Name|Name to identify the credential record. For example, `UiPath Credential`.|
            |Token URL|Location of the token endpoint that the instance uses to retrieve and refresh tokens. For example, `https://account.uipath.com/oauth/token`.|
            |Client Id|Value of client ID you had copied from the UiPath Orchestrator application.|
            |Account Logical Name|Organization ID you had copied from the UiPath Orchestrator application.|
            |Tenant Logical Name|Tenant name you had copied from the UiPath Orchestrator application.|
            |User Key|User key you had copied from the UiPath Orchestrator application.|

        -   If you have selected **UiPath Configuration Template - Private/Public Cloud** for **Configuration Template**, fill these fields.

            |Field|Description|
            |-----|-----------|
            |Connection Name|Name to identify the connection record. For example, `UiPath Connection`.|
            |Connection URL|UiPath instance URL.|
            |Credential Name|Name to identify the credential record. For example, `UiPath Credential`.|
            |Token URL|Location of the token endpoint that the instance uses to retrieve and refresh tokens in this format: `http://<instance-URL>/api/account/authenticate`|
            |Tenant Name|Tenant logical name.|
            |Username or email|Username or email address to authenticate the UiPath Orchestrator API.|
            |Password|Associated password.|

        **Note:**

        -   You must enable **Use MID server** option in the connection record and create a SSL certificate from a trusted authority for on-prem support.
        -   The MID Server users must have the sn\_uipath\_spoke.uipath\_admin role.
    7.  Click **Create**.

    8.  Click **Submit**.

        Connection and credential records are created.

    9.  Open the UiPath Connection record, from the **Connections** tab.

    10. Select a value for the **Orchestrator Feature Enabled** field.


### Result

The Connection and Credential alias is configured and the UiPath spoke is set up using API key.

