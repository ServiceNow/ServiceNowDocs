---
title: Set up the Microsoft Dynamics 365 for Finance and Operations spoke
description: Integrate the ServiceNow instance and Microsoft Dynamics 365 for Finance and Operations by creating a custom OAuth application in Microsoft Azure to authenticate ServiceNow requests.Register your ServiceNow instance in Microsoft Azure portal in order to use Microsoft Dynamics 365 Finance and Operations spoke.Configure the outbound Microsoft Dynamics 365 for Finance and Operations connection record in Workflow Studio to authenticate the requests.Retrieve the metadata from Microsoft Dynamics 365 Finance and Operations and store it in your ServiceNow instance. Dynamic actions require the latest metadata from Microsoft Dynamics 365 Finance and Operations.Configure webhook to subscribe to Microsoft Dynamics 365 for Finance and Operations Spoke with a ServiceNow callback URL.Create webhook routing policy and subflow as per your requirement in the Microsoft Dynamics 365 Finance and Operations spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Microsoft Dynamics 365 for Finance and Operations Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Dynamics 365 for Finance and Operations spoke

Integrate the ServiceNow instance and Microsoft Dynamics 365 for Finance and Operations by creating a custom OAuth application in Microsoft Azure to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Dynamics 365 for Finance and Operations spoke.
-   Role required: admin.

**Note:** After configuring the connection and credential alias, make sure to retrieve the latest metadata from Microsoft Dynamics 365 Finance and Operations application.

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

The app is registered in Azure and the webhook endpoint is configured.

## Configure a connection record

Configure the outbound Microsoft Dynamics 365 for Finance and Operations connection record in Workflow Studio to authenticate the requests.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your ServiceNow instance.

    **Note:** The instance must be the same instance you provided in the redirect URL during the Azure app registration.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

3.  Select the **Integrations** tab.

4.  Under **Connections**, toggle and enable the **Outbound** connections.

5.  Locate the alias for **MicrosoftDynamics365FinAndOps** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Microsoft Dynamics 365 for Finance and Operations spoke, click **View Details**.
    -   To manage more than one Microsoft Dynamics 365 for Finance and Operations spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

6.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection record. The default name is **MicrosoftD365FinAndOps**.

</td></tr><tr><td>

Environment URL

</td><td>

Base URL to connect to Microsoft Dynamics 365 for Finance and Operations. Enter the URL in the format: `https://<instance_ID>.cloudax.dynamics.com/`.

</td></tr><tr><td>

OAuth \(Application ID\) Client ID

</td><td>

Application \(client\) ID generated when you registered the app in the Azure portal.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret generated when you registered the app in the Azure portal.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

OAuth redirect URL in the format: `https://<instance-name>.service-now.com/oauth_redirect.do`. This field is pre-populated and read-only.

</td></tr><tr><td>

Tenant ID

</td><td>

Azure Active Directory Tenant ID.**Tip:** To find the Tenant ID, log in to [https://portal.azure.com/](https://portal.azure.com/). Under the **Manage Azure Active Directory** heading, select **View**. The Tenant ID is available under the **Basic information** heading.

</td></tr></tbody>
</table>7.  Click **Save and Get OAuth Token**.


### Result

The connection is configured.

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

1.  **All** &gt; **Process Automation** &gt; **Workflow Studio**

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

