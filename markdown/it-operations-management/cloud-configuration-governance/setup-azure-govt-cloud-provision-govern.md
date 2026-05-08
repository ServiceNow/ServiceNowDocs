---
title: Set up Microsoft Azure Government Cloud on Cloud Provisioning and Governance
description: Set up Microsoft Azure Government Cloud on Cloud Provisioning and Governance for the first time. You can discover, provision, and manage Microsoft Azure Government Cloud resources using Cloud Provisioning and Governance, thereafter.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Microsoft Azure Government Cloud on Cloud Provisioning and Governance

Set up Microsoft Azure Government Cloud on Cloud Provisioning and Governance for the first time. You can discover, provision, and manage Microsoft Azure Government Cloud resources using Cloud Provisioning and Governance, thereafter.

## Before you begin

To set up Microsoft Azure Government cloud on Cloud Provisioning and Governance, you must:

-   Set up a Microsoft Azure Service Principal on the Azure Government Portal and register the service account on the Cloud Provisioning and Governance application.
-   Configure a MID Server with the required properties to enable Microsoft Azure Government and the ServiceNow instance to communicate correctly.
-   Use the Microsoft Azure Service Principal credentials to discover associated service accounts and cloud resources.
-   In the base system Terraform template, set the *environment* variable to `usgovernment`. For information on where to find the template to modify, see [Discover the Infrastructure as Code \(IaC\) templates](../../cloud-management-v2/concept/exploring-cpg-terraform-connector.md#section_xhl_fjt_xfc).

    ```
    provider "azurerm" {
         subscription_id = "<REPLACE_WITH_ACCOUNT_ID»"
         client_id = "<REPLACE_WITH_APP_ID»"
         client_secret = "<REPLACE_WITH_PASSWORD»"
         tenant_id = "<REPLACE_WITH_TENANT_ID»"
         environment = "usgovernment"
      }
    ```


Role required: admin

**Note:** ServiceNow® ITOM products are not officially certified or supported for Germany and China regions.

## About this task

Be sure to perform the procedures in order. After you have performed the Day 1 setup, you can perform the optional Day 2 setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.

## Procedure

1.  [Create a Microsoft Azure service principal](azure-create-serv-princ-cloud-mgt.md) on the Microsoft Azure Government portal.

    **Note:** Navigate to **App registrations** &gt; **Register an application** &gt; **Supported account types** section. Then, select the **Accounts in this organizational directory only \(Single tenant\)** option to ensure that the Active Directory that is configured for the Microsoft Azure Government cloud is used for authentication.

    For more information, see [Create an Azure AD application and service principal that can access resources](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

2.  Configure MID Servers to connect Cloud Provisioning and Governance to a Microsoft Azure Government cloud account.

    1.  Navigate to **MID server** &gt; **Capabilities**.

    2.  Click **Edit** and add the following options:

        -   **Azure**
        -   **Cloud Management**
    3.  Click **Save**.

    4.  Navigate to **MID server** &gt; **Supported Applications**.

        Skip the next step if **ALL** applications are selected.

    5.  Click **Edit** and add the following applications to the **Supported Applications List**:

        -   **Discovery**
        -   **Cloud Management**
        -   **Orchestration**
    6.  Click **Save**.

        **Note:** For more information, see:

        -   MID server selection
        -   MID server capabilities
3.  Navigate to **MID server** &gt; **Properties**.

    1.  Click **New** and add new records for each of the following name-value pairs:

        MID Server properties

        |Name|Value|
        |----|-----|
        |mid.cmp.azure\_api.base\_endpoint|https://management.usgovcloudapi.net/$\{apiPath\}|
        |mid.cmp.azure\_api.storage.container.path|https://$\{accountName\}.blob.core.usgovcloudapi.net/?comp=list|
        |mid.property.azure\_token\_manager.endpoint|https://login.microsoftonline.us/$\{tenantId\}/oauth2/token|
        |mid.property.azure\_token\_manager.endpoint\_content|grant\_type=client\_credentials&amp;client\_id=$\{clientId\}&amp;resource=https%3A%2F%2Fmanagement.usgovcloudapi.net%2F&amp;client\_secret=$\{clientSecret\}|
        |mid.cmp.azure\_api.storage.blob.path|https://$\{accountName\}.blob.core.usgovcloudapi.net/$\{containerName\}?restype=container&amp;include=snapshots&amp;comp=list|

    2.  Click **Submit**.

4.  [Store the Azure service principal credentials in the instance](azure-create-creds-cloud-mgt.md).

5.  In the **Cloud Admin Portal**, navigate to **Manage** &gt; **Credentials**, and select the Azure Service principal record.

6.  To discover service accounts associated to the Azure subscriptions that are available to this Service principal, click the **Discover Subscriptions** related link.


## Result

The **Azure Subscriptions** related list displays all subscriptions that are associated with the Azure service principal.

## What to do next

[Define the schedule for downloading Microsoft Azure billing data](azure-bill-dwnld-sched-cloud-mgt.md).

