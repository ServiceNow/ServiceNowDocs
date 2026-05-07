---
title: Create Azure cloud credentials
description: If your cloud resources are in an Azure cloud, create credentials that can access the Azure account. This procedure requires configuration in your Azure account.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Discovery for Microsoft Azure, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create Azure cloud credentials

If your cloud resources are in an Azure cloud, create credentials that can access the Azure account. This procedure requires configuration in your Azure account.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Before you begin

Roles required:

-   discovery\_admin, service\_mapping\_admin, sn\_cmp.cloud\_admin roles in Cloud Provisioning and Governance or sn\_cloud\_ops\_ws.cloud\_ops\_admin role in Cloud Discovery Workspace.
-   Operations on the Microsoft Azure portal require one of the following roles:

    -   Azure or Azure AD \(Active Directory\) Administrator
    -   Application Administrator
    -   Application Developer
    -   Cloud Application Administrator
    and the Resource Policy Contributor role to create or modify resource policies.

-   Enable internal network connection between the MID Servers and the Azure Cloud API endpoints: management.azure.com

## Procedure

1.  Log in to the Azure portal and navigate to **Azure Active Directory**.

2.  Navigate to the **App registrations** section and select **New application registration**.

    Enter the following information for your application:

    ![Register an application](../image/register-app-azure.png)

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the application and its integration credentials. For example, `ServiceNow Integration`.|
    |Supported account types|Specify who can use the application.|
    |Redirect URI \(Optional\)|URL that will access Azure. Typically the URL of the ServiceNow instance.|

3.  Select **Register** to complete the app registration.

4.  When registration completes, copy the Application \(client\) ID and Directory \(tenant\) ID values, and paste them in the text editor.

5.  Label the values **Application ID** and **Directory ID** respectively.

6.  In the Azure portal, navigate to the **Certificates &amp; secrets** section and **New client secret** then specify the following values:

<table id="table_thp_prl_wcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key description

</td><td>

Description for the key.

</td></tr><tr><td>

Duration

</td><td>

Expiration for the key.**Note:** Your organization may apply policies to restrict key durability. Select the appropriate duration.

</td></tr></tbody>
</table>7.  Select **Add**.

8.  Copy and paste the key value into the text editor and label the value **Application key**.

9.  Enable the service principal to access Azure subscriptions based on your environment.

    Choose the option that matches your setup:

    -   Management group: Use this option to grant Reader access to all subscriptions under the management group
    -   Individual subscription: Use this option to grant Reader access to a specific subscription only
<table id="choicetable_fwr_vmt_p3c"><thead><tr><th align="left" id="d571308e353">

Option

</th><th align="left" id="d571308e356">

Steps

</th></tr></thead><tbody><tr><td id="d571308e362">

**Management group**

</td><td>

1.  In the Azure portal, navigate to **Management groups** and select the required management group.
2.  Select from the menu **Access Control \(IAM\)**.
3.  Select **+ Add** and then **Add role assignment**.
4.  In the **Role** field, select the **Reader** value.

**Note:** The **Resource Policy Contributor** role is only required for provisioning.

5.  In the **Assign access to** field, keep the default **User, group, or service principal** value.
6.  In the **Select** field, select the name you created in the registering the application step.
7.  Select **Save**.


</td></tr><tr><td id="d571308e434">

**Individual subscription**

</td><td>

1.  In the Azure portal, navigate to **Subscriptions** and select the required subscription.
2.  Enter the subscription ID into the text editor and label it `Subscription ID`.
3.  Select from the menu **Access Control \(IAM\)**.
4.  Select **+ Add** and then **Add role assignment**.
5.  In the **Role** field, select the **Reader** value.

**Note:** The **Resource Policy Contributor** role is only required for provisioning.

6.  In the **Assign access to** field, keep the default **User, group, or service principal** value.
7.  In the **Select** field, select the name you created in the registering the application step.
8.  Select **Save**.


</td></tr></tbody>
</table>10. Select the **Azure Service Principal** type credential.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **Azure Service Principal**.

11. Specify the following values on the Azure Service Principal form:

<table id="table_m3f_bqm_wcb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the service principal to register with the instance. For example, `Azure service principal credentials`.

</td></tr><tr><td>

Authentication Method

</td><td>

Select **Client secret**.The **Secret key** field appears when you select **Client secret**.

 **Note:** **Client assertion** is not supported.

</td></tr></tbody>
</table>12. Copy and paste values from the temporary text file into the remaining fields.

    ![Azure credentials](../image/azure-copy-to-service-principal.png)

    |Credentials form field|Azure Service Principal value|
    |----------------------|-----------------------------|
    |Tenant ID|Azure **Directory ID** value from the text file.|
    |Client ID|Azure **Application ID** value from the text file.|
    |Secret key|Azure **Application key** value from the text file.|

13. Select **Save** to create the Azure service principal.

14. Select the **Discover Subscriptions** related link to find all subscriptions for the Azure service principal.

    The instance creates a service account for each discovered subscription. The **Azure Subscriptions** related list displays all subscriptions for the Azure service principal.

15. Select a subscription to view the service account created for the subscription.

16. Select a Discovery status entry in the **Credential Discovery Status** list to view the Discovery log.

    Each time you select **Discover Subscription**, the instance generates a new Discovery status and displays it in the **Credential Discovery Status** list.


