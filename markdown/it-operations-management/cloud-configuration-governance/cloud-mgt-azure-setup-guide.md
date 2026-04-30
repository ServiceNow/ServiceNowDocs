---
title: Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance
description: To set up Cloud Provisioning and Governance for the very first time, you perform the procedures in this "Day 1" setup guide. Be sure to perform the procedures in order. After you have performed Day 1 setup, you can perform optional Day 2 setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance

To set up Cloud Provisioning and Governance for the very first time, you perform the procedures in this "Day 1" setup guide. Be sure to perform the procedures in order. After you have performed Day 1 setup, you can perform optional Day 2 setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.

## Request the Cloud Provisioning and Governance application

The Cloud Provisioning and Governance application is available as a separate subscription and requires the Cloud Provisioning and Governance plugin \(com.snc.cloud.mgmt\). See [Request the Cloud Provisioning and Governance application](../task/request-plugin-cloud-mgt-1.md).

## Roles required to set up Cloud Provisioning and Governance

-   Operations on the Azure portal require one of the following roles:

    -   Azure or Azure AD \(Active Directory\) Administrator
    -   Application Administrator
    -   Application Developer
    -   Cloud Application Administrator
    and the Resource Policy Contributor role to create or modify resource policies.

-   Operations in Cloud Provisioning and Governance require the sn\_cmp.cloud\_admin role.

## About terms that Cloud Provisioning and Governance uses

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings. In Azure, the region-specific containers for virtual resources are called regions. In Cloud Provisioning and Governance, regions are called datacenters or logical datacenters \(LDCs\). The term logical is used to reinforce the idea that Cloud Provisioning is provider-agnostic. All infrastructure or applications that are deployed using Cloud Provisioning are associated with a datacenter.

## Quick overview of the setup process

Your setup process includes these tasks:

-   If needed: Request the Cloud Provisioning and Governance application.
-   Assign appropriate roles to cloud users.
-   Set up the MID Servers that will handle secure communications with the provider API endpoints.
-   On the provider portal, collect your account settings and the credentials that the Discovery process will use \(through a MID Server\) to programatically access your provider accounts. Securely associate the account settings and credentials with a service account in Cloud Provisioning and Governance.
-   Set up a cloud account to represent your entire managed cloud infrastructure and set up a service account that works with one of your provider accounts. You specify which datacenters in the service account should be included in the cloud account. \(Later, on "Day 2", you can set up additional cloud accounts and service accounts from the same or other providers.\)
-   Cloud Provisioning uses CMDB data to help users request and manage cloud resources and to help you manage your cloud infrastructure. To populate the CMDB with resource data for all datacenters, you manually run the Discovery process on each datacenter in the service account. Then, to ensure that the data continues to be updated, you configure Discovery to run on a regular schedule. Your cloud account might look like this:

    ![Structure of a cloud account on Day 1](../image/cloud-acct-day-1.png "Structure of a cloud account on Day 1")

-   Providers offer services that can auto-update the CMDB whenever a create/modify/terminate life-cycle change or configuration update occurs to a resource. You can configure the service to integrate directly with Cloud Provisioning and Governance.

## What you will do to integrate Cloud Provisioning and Governance with your Microsoft Azure accounts

Detailed instructions for each procedure follow this overview.

-   **1. Assign roles to Azure users of Cloud Provisioning and Governance**

    You assign Cloud Provisioning and Governance roles to user groups and to individual users based on user activities and responsibilities.

-   **2. [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md)**

    To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. You can set up the MID Servers on your network or in one of your cloud networks.

    **Note:** Data is encrypted to the MID Server and between the MID Server and the API endpoint. To ensure high performance and security, you should configure one or more MID Server for each datacenter under management. Configure the MID Server even if you have already configured other MID Servers while setting up Cloud Provisioning and Governance for another cloud provider.

-   **3. Create a Microsoft Azure service principal**

    To securely access resource and billing data on your Microsoft Azure account, the Discovery process must present appropriate Microsoft Azure account credentials. You create a special programmatic account — a Microsoft Azure service principal — to generate the required credentials.

-   **4. Store the Azure service principal credentials in the instance**

    To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you first create Azure service principal credentials in the Azure Portal. You then securely store the credentials in a service account in your instance.

-   **5. Add an Azure service account**

    A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter.

-   **6. Discover all datacenters in a service account on-demand**

    Discovery uses the information in the service account to identify all logical datacenters associated with the provider account.

-   **7. Set up a cloud account for Azure**

    A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

-   **8. Set capacity limits on user requests for resources**

    Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.

-   **10. Create Microsoft Azure credentials for billing download**

    Define the scheduled job that regularly uses a MID Server to download billing data from the provider. Cloud Provisioning and Governance saves the data in a cost table and uses the information to generate reports.


## Next steps

When you have finished all Day-1 and Day-2 procedures in this setup guide, see the [Cloud Provisioning and Governance administration guide](../../cloud-management-v2/concept/cloud-configuration.md) for information on using the Cloud Provisioning and Governance application in your organization.

