---
title: Create a Microsoft Azure service principal
description: To securely access resource and billing data on your Microsoft Azure account, the Discovery process must present appropriate Microsoft Azure account credentials. You create a special programmatic account — a Microsoft Azure service principal — to generate the required credentials.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a Microsoft Azure service principal

To securely access resource and billing data on your Microsoft Azure account, the Discovery process must present appropriate Microsoft Azure account credentials. You create a special programmatic account — a Microsoft Azure service principal — to generate the required credentials.

## Before you begin

Roles required:

-   discovery\_admin, service\_mapping\_admin, sn\_cmp.cloud\_admin roles in Cloud Provisioning and Governance or sn\_cloud\_ops\_ws.cloud\_ops\_admin role in Cloud Discovery Workspace.
-   Operations on the Microsoft Azure portal require one of the following roles:

    -   Azure or Azure AD \(Active Directory\) Administrator
    -   Application Administrator
    -   Application Developer
    -   Cloud Application Administrator
    and the Resource Policy Contributor role to create or modify resource policies.

-   Enable internal network connection between the MID Servers and the Azure Cloud API endpoints:
    -   The US GovCloud URL is `https://management.usgovcloudapi.net/`.
    -   The commercial Azure Cloud URL is management.azure.com.

        **Note:** It isn't necessary when adding a credential if the account being added is already a GovCloud account.


## Procedure

1.  Log in to the Azure portal and navigate to **Azure Active Directory**.

2.  Navigate to the **App registrations** section and click **New application registration**.

    Enter the following information for your application:

    ![Register an application](../../discovery/image/register-app-azure.png)

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
</table>7.  Click **Add**.

8.  Copy and paste the key value into the text editor and label the value **Application key**.

9.  To enable the service principal to work with various Azure subscriptions, navigate to **Subscriptions**.

    To manage multiple subscriptions, you must perform the following procedure for each subscription:

    1.  Paste the subscription ID into the text editor and label it **Subscription ID**.

        The text file that you generate during this procedure might look something like this: ![Text file that temporarily holds Azure service principal credential values](../../discovery/image/azure-text-file.png)

    2.  Navigate to the subscription and select **Access Control \(IAM\)** from the menu.

    3.  Click **+ Add** at the top of the screen then **Add role assignment**.

    4.  Select the value **reader** from the **Role** field.

        Let the default value **User, group, or service principal** remain as is in the **Assign access to** field.

        **Note:** The **Resource policy contributor** role is only required for provisioning.

    5.  Select the name you created in step 2 in the **Select** field and click **Save**.

        ![Add role assignment](../../discovery/image/add-role-assignment.png)

10. Perform the appropriate action.

    -   If you are not using Cloud Discovery through Cloud Discovery Workspace, do the following:

        In the Discovery Manager, click the plus icon \(**+**\) and then select **Azure Service Principal** from the list.

    -   If you are using Cloud Discovery through Cloud Discovery Workspace, do the following:
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

    ![Azure credentials](../../discovery/image/azure-copy-to-service-principal.png)

    |Credentials form field|Azure Service Principal value|
    |----------------------|-----------------------------|
    |Tenant ID|Azure **Directory ID** value from the text file.|
    |Client ID|Azure **Application ID** value from the text file.|
    |Secret key|Azure **Application key** value from the text file.|

13. Click **Save** to create the Azure service principal.

14. Click the **Discover Subscriptions** related link to find all subscriptions for the Azure service principal.

    The instance creates a service account for each discovered subscription. The **Azure Subscriptions** related list displays all subscriptions for the Azure service principal.

15. Click a subscription to view the service account created for the subscription.

16. Click a Discovery status entry in the **Credential Discovery Status** list to view the Discovery log.

    Each time you click **Discover Subscription**, the instance generates a new Discovery status and displays it in the **Credential Discovery Status** list.


## What to do next

Cloud Provisioning and Governance only: Create a record of the service principal credentials on the ServiceNow instance so that Cloud Provisioning and Governance processes can access Microsoft Azure data. See [Store the Azure service principal credentials in the instance](azure-create-creds-cloud-mgt-1.md).

