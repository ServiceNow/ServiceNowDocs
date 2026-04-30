---
title: Set up the Microsoft Dynamics 365 for Finance and Operations spoke
description: Integrate the ServiceNow instance and Microsoft Dynamics 365 for Finance and Operations by creating a custom OAuth application in Microsoft Azure to authenticate ServiceNow requests.Register Microsoft Dynamics 365 for Finance and Operations as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.Modify the short description to provide spoke specific information.Create a connection record for your Microsoft Dynamics 365 for Finance and Operations. The Microsoft Dynamics 365 for Finance and Operations spoke connection and credential aliases use these connections to perform actions in Microsoft Dynamics 365 for Finance and Operations.Retrieve the metadata from Microsoft Dynamics 365 Finance and Operations and store it in your ServiceNow instance. Dynamic actions require the latest metadata from Microsoft Dynamics 365 Finance and Operations.Configure webhook to subscribe to Microsoft Dynamics 365 for Finance and Operations Spoke with a ServiceNow callback URL.Create webhook routing policy and subflow as per your requirement in the Microsoft Dynamics 365 Finance and Operations spoke.Register your ServiceNow instance in Microsoft Azure portal in order to use Microsoft Dynamics 365 Finance and Operations spoke.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Microsoft Dynamics 365 for Finance and Operations Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Microsoft Dynamics 365 for Finance and Operations spoke

Integrate the ServiceNow instance and Microsoft Dynamics 365 for Finance and Operations by creating a custom OAuth application in Microsoft Azure to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Dynamics 365 for Finance and Operations spoke.
-   Role required: admin.

**Note:** After configuring the connection and credential alias, make sure to retrieve the latest metadata from Microsoft Dynamics 365 Finance and Operations application.

## Register Microsoft Dynamics 365 for Finance and Operations as an OAuth provider

Register Microsoft Dynamics 365 for Finance and Operations as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open for the record for Microsoft D365 Fin and Ops Spoke OAuth.

3.  On the form, fill these values.

<table id="table_wll_3kv_drb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter: `Microsoft Dynamics 365 for Finance and Operations OAuth`

</td></tr><tr><td>

Client ID

</td><td>

Client ID created during the Microsoft Dynamics 365 for Finance and Operations application configuration.

</td></tr><tr><td>

Client Secret

</td><td>

Client Secret created during the Microsoft Dynamics 365 for Finance and Operations application configuration.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth authorization code endpoint. Enter: `https://login.microsoftonline.com/<AzureTenantID>/oauth2/v2.0/authorize`

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter: `https://login.microsoftonline.com/<AzureTenantID>/oauth2/v2.0/token`

</td></tr><tr><td>

Token Revocation URL

</td><td>

OAuth server token revocation endpoint.

</td></tr><tr><td>

Redirect URL

</td><td>

OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`

</td></tr><tr><td>

OAuth API Script

</td><td>

Script to customize the request and response. Select ****.

</td></tr><tr><td>

Logo URL

</td><td>

URL that contains an image to use as the application logo.

</td></tr><tr><td>

Default Grant Type

</td><td>

Grant type used to establish the token. Select **Client Credentials**.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 8,640,0000 seconds.

</td></tr><tr><td>

PKCE required

</td><td>

Option to enable public clients to require PKCE for an authorization.**Note:** You can use only **Authorization Code** as the **Default Grant type** when **PKCE** is enabled.

</td></tr><tr><td>

Application

</td><td>

Application scope that contains this record.

</td></tr><tr><td>

Accessible from

</td><td>

Application scope that this registry is accessible from.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the application registry.

</td></tr><tr><td>

Use mutual authentication

</td><td>

Option to use mutual authentication for token request and revocation. This option requires a mutual authentication profile to be specified.

</td></tr></tbody>
</table>4.  Right-click the form header, and click **Save**.


## Create a connection record for the Microsoft Dynamics 365 for Finance and Operations

Create a connection record for your Microsoft Dynamics 365 for Finance and Operations. The Microsoft Dynamics 365 for Finance and Operations spoke connection and credential aliases use these connections to perform actions in Microsoft Dynamics 365 for Finance and Operations.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for **MicrosoftD365FinAndOps**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Microsoft Dynamics 365 for Finance and Operations Connection`.|
    |Credential|Credential record created for Microsoft Dynamics 365 for Finance and Operations. Search and select `MicrosoftD365FinAndOps.Credential`.|
    |Connection alias|Alias record associated with this connection. Enter `sn_ms_fin_ops_spk.MicrosoftD365FinAndOps`|
    |Connection URL|Base URL to connect to **Microsoft Dynamics 365 for Finance and Operations**. Enter: `https://<instance_ID>.cloudax.dynamics.com/`|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|

5.  Click **Submit**.


## Retrieve metadata from Microsoft Dynamics 365 Finance and Operations

Retrieve the metadata from Microsoft Dynamics 365 Finance and Operations and store it in your ServiceNow instance. Dynamic actions require the latest metadata from Microsoft Dynamics 365 Finance and Operations.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Microsoft D365 FinOps Metadata** &gt; **Microsoft D365 FinOps Metadata Content**.

2.  Click **Get/Refresh Metadata**.

3.  Select the alias to retrieve updated metadata from Microsoft Dynamics 365 Finance and Operation application and click **Ok**.

    **Note:** Make sure to retrieve the latest metadata whenever there any changes in the Microsoft Dynamics 365 Finance and Operations application.


## Set up bi-directional webhook for the Microsoft Dynamics 365 for Finance and Operations Spoke

Configure webhook to subscribe to Microsoft Dynamics 365 for Finance and Operations Spoke with a ServiceNow callback URL.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Microsoft D365 FnO spoke** &gt; **FnO Webhook Registries**.

2.  Click **New**.

3.  On the form fill in the fields.

<table id="table_txp_n3x_hbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the webhook registry. For example, `Microsoft Dynamics 365 for Finance and Operations webhook`.

</td></tr><tr><td>

Description

</td><td>

Optional description for the webhook.

</td></tr><tr><td>

Generate Callback URL

</td><td>

Option to generate a callback URL which is used to register the webhook in the Microsoft Dynamics 365 Finance and Operations portal.

</td></tr><tr><td>

Generate New Secret

</td><td>

Option to generate a secret key for Microsoft Dynamics 365 Finance and Operations webhook.**Note:**

When you generate a new secret, ensure that you generate the callback URL also after generating the secret.

Record the callback URL for registering the app in Azure portal.

</td></tr></tbody>
</table>
## Customize bi-directional webhook in the Microsoft Dynamics 365 Finance and Operations spoke

Create webhook routing policy and subflow as per your requirement in the Microsoft Dynamics 365 Finance and Operations spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **Subflows**.

3.  Create a copy of the required subflow.

4.  Customize the required subflow as per your requirement and publish it.

5.  Navigate to **Microsoft D365 FnO Spoke** &gt; **FnO WebHook Routing Policies**.

6.  Click **New**.

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

Default answer

</td><td>

Option to specify if this is the default answer. Default answer is applicable when the conditions are not met.1.  Click the Lookup icon.
2.  Select the required subflow from the **Document:** list.

**Note:** Ensure that the **Table name** is `Flow [sys_hub_flow]`.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Microsoft Dynamics 365 Finance and Operations. See [Microsoft Dynamics 365 for Finance and Operations Spoke](../concept/msdyn-finops-spoke.md) for information about the supported fields.

</td></tr><tr><td>

Answer

</td><td>

Subflow that has to be triggered when the specified conditions are met.

</td></tr></tbody>
</table>8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


### Result

Routing policy and subflow are created.

## Register an app in Microsoft Azure portal for Microsoft Dynamics 365 Finance and Operations spoke

Register your ServiceNow instance in Microsoft Azure portal in order to use Microsoft Dynamics 365 Finance and Operations spoke.

### Before you begin

Role required: admin

### Procedure

1.  Log in to Azure portal.

2.  Navigate to App registrations and register an app for the webhook.

3.  Create a key vault using the Azure portal.

    For more information, see [Create a key vault using the Azure portal](https://learn.microsoft.com/en-us/azure/key-vault/general/quick-create-portal).

4.  Navigate to **Access policies**.

5.  Create an access policy.

6.  Select **Get** under Secret permissions and click **Next**.

7.  In the **Principal** tab, search for the name of the app registered earlier and click **Next**.

8.  In the **Application \(optional\)** tab, click Next.

9.  In the **Review + create** tab, click **Create**.

10. Navigate to **Secrets** section.

11. Click on **+ Generate/Import**.

12. On the Create a secret page, enter a name and provide the callback URL generated from your ServiceNow instance.

13. Click **Create**.

14. Log in to your Microsoft Dynamics 365 Finance and Operations portal.

15. Navigate to **System administration** &gt; **Business events** &gt; **Business events catalog**.

16. Navigate to the Endpoints tab and click **New**.

17. Select the endpoint type as HTTPS from the Standard view and click **Next**.

18. On the form, fill in the details.

    | | |
    |---|---|
    |Endpoint name|Name of the endpoint.|
    |Endpoint type|Type of the endpoint.|
    |Key Vault|Key vault created for the application.|
    |Azure Active Directory Application ID|Object ID of the application.|
    |Azure application secret|Secret created for the application|
    |Key vault DNS name|Vault URI of the application.|
    |Key vault secret name|Name of the key vault secret.|

19. Click **Ok**.

    **Note:** Ensure that key vault access policy is created for the application. The access policy should allow the application registry to access secrets from the key vault.

20. Navigate to the Business Events tab and search for a category.

    For example, Purchase orders.

21. Select the required category from the list and click **Activate**.

22. In the Configure new business event section, select the legal entity and endpoint name.

23. Click Ok.

    **Note:** Ensure that these API permissions are enabled for the application.

    -   Access Dynamics AX Custom Service
    -   Access Dynamics AX data
    -   Access Dynamics AX online as organization users

### Result

The webhook is registered and ready for testing.

