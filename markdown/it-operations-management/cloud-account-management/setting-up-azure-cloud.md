---
title: Setting up Azure cloud
description: Topics for setting up Azure cloud, arranged in order of configuration priority.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/setting-up-azure-cloud.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Set up Azure cloud with Cloud Workspace]
breadcrumb: [Configuring cloud providers, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Setting up Azure cloud

Topics for setting up Azure cloud, arranged in order of configuration priority.

Two steps are critical when setting up Azure: configuring the Azure Service Principal credential, and creating the Azure service accounts in ServiceNow that mirror your Azure hierarchy management group or subscription. Each subsequent step depends on those credentials and account IDs being correct.

The bulk of the work occurs when setting up the Azure service accounts. An Azure Admin configures the credential on the Azure side. The ServiceNow AI Platform Admin then performs the ServiceNow configuration, including populating dependent tables, creating the service account, configuring scans for data visualization, and reviewing the default certification policy.

Account suspension is also configured on the Azure side by an Azure Admin. This is an optional step, separate from the core setup process.

-   **[Configure account suspension in Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configuring-azure-suspension-permission.md)**  
Manage an Azure subscription using the permission and by assigning the role to a user. The role must have the permission to execute the APIs for suspending and reactivating an Azure account.
-   **[Set up Azure Service Principal credential](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/set-up-azure-service-principal-credential.md)**  
Provide the Azure credentials obtained from your Azure administrator. These credentials are used to create a suspension profile and enables you to suspend temporarily or terminate Azure accounts as needed.
-   **[Set up suspension of a subscription using Azure policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configuring-lock-unlock-policy-for-azure.md)**  
Create the policy at the root level to lock or unlock an Azure account. As an Azure administrator, lock an Azure subscription, resource group, or resource to avoid accidental deletions and modifications.

**Parent Topic:**[Configuring cloud providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configuring-cloud.md)

