---
title: Set up Microsoft Dynamics CRM spoke
description: Integrate the ServiceNow instance and Microsoft Dynamics CRM by using the Windows credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Microsoft Dynamics CRM account to enable OAuth 2.0 authentication with the Microsoft Dynamics CRM.Use the information generated during Microsoft Dynamics CRM account configuration to register Microsoft Dynamics CRM as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create Credential records for the Microsoft Dynamics CRM custom OAuth application you created during Microsoft Dynamics CRM account configuration. The Microsoft Dynamics CRM spoke connection and credential aliases use these credentials to authorize actions.Create Connection records to your Microsoft Azure account. The Microsoft Dynamics CRM spoke connection and credential alias uses these connections to perform actions on Microsoft Dynamics CRM.Register Microsoft Dynamics CRM webhook in ServiceNow to notify the ServiceNow application when certain events occur in Microsoft Dynamics CRM.Create webhook routing policy and subflow according to your requirements.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 6
breadcrumb: [Microsoft Dynamics CRM Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Microsoft Dynamics CRM spoke

Integrate the ServiceNow instance and Microsoft Dynamics CRM by using the Windows credentials to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription.
-   Install Microsoft AD.
-   Activate the Microsoft Dynamics CRM spoke.
-   Role required: admin.

## About this task

Perform these steps to use all Microsoft Dynamics CRM spoke actions.

## Configure Microsoft Dynamics CRM application

Create a custom OAuth application from your Microsoft Dynamics CRM account to enable OAuth 2.0 authentication with the Microsoft Dynamics CRM.

### Before you begin

Microsoft Dynamics CRM requirements:

-   Microsoft Dynamics CRM account
-   [Microsoft Azure](https://portal.azure.com) account
-   Role required: Microsoft Dynamics CRM admin

### About this task

Complete these steps from your Azure Developer account. See the [Azure](https://docs.microsoft.com/en-us/azure/) product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Log in to the [Microsoft Azure App registration portal](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) with your organization credentials.

2.  Register a new custom application by filling in the application name, the supported account type, and the redirect URI, and then click **Register**.

    An overview of the application's basic information is shown.

3.  Copy the application ID to a text file.

    You will use this ID and the client secret generated in the next step to register the app as a third-party OAuth provider on your ServiceNow instance. You use the application ID as the client ID when you connect the application to ServiceNow.

4.  Add a client secret.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Provide a description and an expiration date and click **Add**.

        **Note:** The client secret is only displayed in plain text for a short time. You use the client secret when you connect the application to ServiceNow.

5.  Enable the permissions you want the application to support.

    For more information, see the [Microsoft Graph permissions reference](https://docs.microsoft.com/en-us/graph/permissions-reference).

    1.  In Microsoft Azure, navigate to **Manage** &gt; **API permissions**.

    2.  Click the Microsoft Graph tile.

    3.  Select the Delegated or Application permissions that the application supports.

        Delegated permissions enable the application to access the API as a signed-in user. Application permissions enable the application to run as a background service or daemon without a signed-in user.

    4.  Click **Add permissions**.


### What to do next

[Register Microsoft Dynamics CRM as OAuth provider](setup-ms-dynamics-crm.md#).

## Register Microsoft Dynamics CRM as OAuth provider

Use the information generated during Microsoft Dynamics CRM account configuration to register Microsoft Dynamics CRM as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

-   Request Integration Hub subscription.
-   Activate Microsoft Dynamics CRM.
-   Create a Microsoft Dynamics CRM application.
-   Role required: admin.

### Procedure

1.  In ServiceNow, navigate to **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

3.  On the screen titled **What kind of OAuth application**, select **Connect to a third-party OAuth Provider**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record, for example `Dynamics CRM OAuth profile`.|
    |Client ID|Enter the Application ID of the Microsoft Dynamics CRM application you created in Azure.|
    |Client Secret|Enter the Client Secret you generated when you created the application in Azure.|
    |Default Grant type|Select **Authorization Code**.|
    |Authorization URL|Click the lock icon \(![Lock icon](../../../common/image/icon-lock.png)\), enter `https://login.microsoftonline.com/common/oauth2/v2.0/authorize` followed by a question mark and the resource attribute of your instance, and then click the lock icon again. The resource attribute of the URL. For example, `?resource=https://mycompany.crm.dynamics.com`. This attribute is the URL of your Microsoft application.|
    |Token URL|Click the lock icon \(![Lock icon](../../../common/image/icon-lock.png)\), enter `https://login.microsoftonline.com/common/oauth2/v2.0/token`, and then click the lock icon again.|
    |Redirect URL|Click the lock icon \(![Lock icon](../../../common/image/icon-lock.png)\), enter `https://<instance>.service-now.com/oauth_redirect.do`, and then click the lock icon again.|

5.  In the **OAuth Entity Scopes** related list, edit the provided entity scope to include the URL of your Microsoft Dynamics CRM application.

    The name and the OAuth scope are often the same string.

    ![The Microsoft Dynamics CRM OAuth entity scopes.](../image/oauth-entity-scopes-ms-dyn-crm.png)

6.  Right-click the form header, and click **Save**.

    The system validates the OAuth credentials.


### What to do next

Create credential record for Microsoft Dynamics CRM.

## Create Credential records for the Microsoft Dynamics CRM spoke

Create Credential records for the Microsoft Dynamics CRM custom OAuth application you created during Microsoft Dynamics CRM account configuration. The Microsoft Dynamics CRM spoke connection and credential aliases use these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays a blank OAuth 2.0 Credentials form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `Dynamics Credentials`.|
    |Active|Enable|
    |OAuth Entity Profile|Select the OAuth profile you created when you registered the custom Microsoft Dynamics CRM application as an OAuth provider. For example, select **Dynamics OAuth profile**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Save the record.

6.  From Related Links, click **Get OAuth Token**.

    The system displays a confirmation message that the OAuth token flow is completed successfully. Review the details if the flow is not completed successfully.

    **Note:** Ensure that you allow pop-up windows in your browser.


## Create Connection records for the Microsoft Dynamics CRM spoke

Create Connection records to your Microsoft Azure account. The Microsoft Dynamics CRM spoke connection and credential alias uses these connections to perform actions on Microsoft Dynamics CRM.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the connection and credential alias for the Microsoft Dynamics CRM application.

3.  On the **Connections** tab, click **New**.

    The system displays a blank **HTTP\(s\) Connection** form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `MS Dynamics CRM Connection`.|
    |Credential|Select the Credential record you created for Microsoft Dynamics CRM. For example, select **MS Dynamics Credentials**.|
    |Connection alias|Select the Connection alias record you created for Microsoft Dynamics CRM.|
    |Active|Enable|
    |Connection URL|Enter the root Dynamics URL. For example, `https://<SiteName>.dynamics.com`.|

5.  Click **Submit**.


## Configure Microsoft Dynamics CRM webhook details

Register Microsoft Dynamics CRM webhook in ServiceNow to notify the ServiceNow application when certain events occur in Microsoft Dynamics CRM.

### Before you begin

Role required: admin

-   Microsoft Dynamics CRM requires registration through the Windows Plugin Registration Tool. To install the Windows Plugin Registration Tool, see the Microsoft document [Download tools from NuGet](https://docs.microsoft.com/en-us/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
-   The Endpoint URL is the ServiceNow instance URL to which event information is posted. For example, `https://<instance-name>.service-now.com/api/sn_ms_crm_spoke/dynamics_webhook_callbacks`.
-   The key-value pair you use to register the webhook in the Plugin Registration Tool is the same as the Name and Authorization Key in Dynamics CRM Webhook Details.

### Procedure

1.  Navigate to **All** &gt; **Dynamics CRM Webhook Details** &gt; **Client Details**.

2.  Click **New**.

3.  In the **Name** field, enter the webhook's plugin key.

4.  In the **Authorization Key** field, enter the value from the webhook's key-value pair.


### Configure Microsoft Dynamics CRM webhook decision policy

Create webhook routing policy and subflow according to your requirements.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**

2.  Click **Subflows**.

3.  Create a copy of the default sample subflow, Process Dynamics CRM Webhook.

4.  Customize the subflow according to your requirement and publish it.

    See [Create a subflow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-subflow&version=australia&pubname=australia-build-workflows&ft:locale=en-US) for more information about creating and using subflows.

5.  Navigate to **Dynamics CRM Webhook Details** &gt; **Decision Policy**.

6.  On the **Decisions** tab, click **New**.

7.  On the form, fill in the fields.

<table id="table_awj_xgv_z3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label to identify the routing policy.

</td></tr><tr><td>

Answer

</td><td>

Option to specify if this answer is the default answer. Default answer is applicable when the conditions are not met.1.  Click the Lookup icon.
2.  Select the required subflow from the **Document:** list.

**Note:** Ensure that the **Table name** is `Dynamics CRM Webhook Answer Subflow [sn_ms_crm_spoke_dynamic_crm_webhook_answer_subflow]`.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Microsoft Dynamics CRM.

</td></tr></tbody>
</table>8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


#### Result

Decision policy and subflow are created.

