---
title: Set up Microsoft Azure Cloud on Cloud Services Catalog
description: Integrate Cloud Services Catalog with your Microsoft Azure account as a part of the Day 1 configuration task toward setting up CSC for the first time.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Cloud Services Catalog setup for the Day 1 configuration task, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Microsoft Azure Cloud on Cloud Services Catalog

Integrate Cloud Services Catalog with your Microsoft Azure account as a part of the Day 1 configuration task toward setting up CSC for the first time.

## Before you begin

Collect your account settings and credentials from the provider portal. These settings and credentials help you to distinguish the resources in one account from another account and sign in or authenticate to Microsoft Azure. Permission policies specify your approvals within the resources in the account.

Roles required:

-   Microsoft Azure or Microsoft Azure AD \(Active Directory\) Administrator
-   Application Administrator
-   Application Developer
-   Cloud Application Administrator and the Resource Policy Contributor role to create or modify the resource policies.
-   sn\_cmp.cloud\_admin role for operations in Cloud Services Catalog

## Procedure

1.  Assign roles to Azure users of Cloud Provisioning and Governance.

    You assign Cloud Provisioning and Governance roles to the user groups and individual users based on the user activities and responsibilities. For more information, see [Assign roles to Azure users of Cloud Provisioning and Governance](../../cloud-management-v2-setup/task/azure-assign-roles-cloud-mgt.md).

2.  Install and configure MID Servers for Cloud Discovery and Cloud Provisioning and Governance.

    To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. For more information, see [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md).

3.  Set up the MID Servers on your network or in one of your cloud networks.

    Data is encrypted to the MID Server and between the MID Server and the API endpoint.

4.  Configure one or more MID Servers for each datacenter under management for high performance and security.

    Configure the MID Server even if you have already configured other MID Servers while setting up Cloud Services Catalog for another cloud provider.

5.  Create a Microsoft Azure service principal.

    To access the resources and billing data securely on your Microsoft Azure account, the Discovery process must present appropriate Microsoft Azure account credentials. You create a special programmatic account—a Microsoft Azure service principal—to generate the required credentials. For more information, see [Create a Microsoft Azure service principal](../../cloud-management-v2-setup/task/azure-create-serv-princ-cloud-mgt.md).

6.  Store the Azure service principal credentials in the instance.

    To access the data on your provider account securely, the Discovery process must present the appropriate credentials. To make the credentials available to Discovery, you first create Microsoft Azure service principal credentials in the Azure Portal. You can then securely store the credentials in a service account in your instance. For more information, see [Store the Azure service principal credentials in the instance](../../cloud-management-v2-setup/task/azure-create-creds-cloud-mgt.md).

7.  Add an Azure service account. [Add an Azure service account](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md)

    A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. For more information, see [Add an Azure service account](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md).

8.  Discover all datacenters in a service account.

    Discovery uses the information in the service account to identify all logical datacenters that are associated with the provider account.

9.  Set up a cloud account for Azure.

    A cloud account is the logical representation in Cloud Services Catalog of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts, including the service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account. For more information, see [Set up a cloud account for Azure](../../cloud-management-v2-setup/task/azure-cloud-accts-cloud-mgt.md).

10. Set the capacity limits on user requests for resources.

    Capacity limits place restrictions on the attributes of the cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set the limits on the resources separately for each logical datacenter in a cloud account.


**Parent Topic:**[Cloud Services Catalog setup for the Day 1 configuration task](setting-up-cloud-services.md)

