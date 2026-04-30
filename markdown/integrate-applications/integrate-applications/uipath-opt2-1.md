---
title: Option 1: Using OAuth authentication
description: Integrate the ServiceNow instance with your UiPath account using OAuth to authenticate ServiceNow requests.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Option 1: Using OAuth authentication

Integrate the ServiceNow instance with your UiPath account using OAuth to authenticate ServiceNow requests.

## Before you begin

Role required: admin

**Note:**

-   This authentication is available from UiPath spoke v2.2.1.
-   You can't use MID Server if you set up the spoke using OAuth authentication.

## Procedure

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


## Result

The Connection and Credential alias is configured and the UiPath spoke is set up using OAuth authentication.

