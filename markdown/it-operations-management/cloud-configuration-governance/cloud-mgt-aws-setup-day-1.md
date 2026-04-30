---
title: Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance
description: To set up Cloud Provisioning and Governance for the very first time, you perform the procedures in this "Day 1" setup guide. Be sure to perform the procedures in order. After you have performed Day 1 setup, you can perform optional Day 2 setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance

To set up Cloud Provisioning and Governance for the very first time, you perform the procedures in this "Day 1" setup guide. Be sure to perform the procedures in order. After you have performed Day 1 setup, you can perform optional Day 2 setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.

## Request the Cloud Provisioning and Governance application

The Cloud Provisioning and Governance application is available as a separate subscription and requires the Cloud Provisioning and Governance plugin \(com.snc.cloud.mgmt\). See [Request the Cloud Provisioning and Governance application](../task/request-plugin-cloud-mgt-1.md).

## Roles required to set up Cloud Provisioning and Governance

-   Operations in the AWS Management Console require the administrator role.
-   Operations in Cloud Provisioning and Governance require the sn\_cmp.cloud\_admin role.

## About terms that Cloud Provisioning and Governance uses

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings. In AWS, the region-specific containers for virtual resources are called regions. In Cloud Provisioning, regions are called datacenters or logical datacenters \(LDCs\). The term logical is used to reinforce the idea that Cloud Provisioning is provider-agnostic. All infrastructure or applications that are deployed using Cloud Provisioning are associated with a datacenter.

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

## What you will do to integrate Cloud Provisioning and Governance with your AWS accounts

Detailed instructions for each procedure follow this overview.

-   **1. Assign roles to AWS users of Cloud Provisioning and Governance**

    You assign Cloud Provisioning and Governance roles to user groups and to individual users based on user activities and responsibilities.

-   **2. [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md)**

    To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. You can set up the MID Servers on your network or in one of your cloud networks. You can configure the MID Server for Cloud Provisioning and Governance to use a proxy server. Using a proxy server supports all cloud-based activities such as running Discovery, billing downloads, provisioning virtual machines, and running life-cycle operations on virtual machines.

    **Note:** Data is encrypted to the MID Server and between the MID Server and the API endpoint. To ensure high performance and security, you should configure one or more MID Server for each datacenter under management. Configure the MID Server even if you have already configured other MID Servers while setting up Cloud Provisioning and Governance for another cloud provider.

-   **3. [Configure access to the AWS accounts using permanent AWS credentials](../../it-operations-management/task/aws-create-creds-cloud-mgt.md)**

    To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery and Cloud Provisioning and Governance, you first create a user with programmatic access in the AWS Management Console. You then securely store the credentials in a service account at ServiceNow AI Platform.

-   **4. Create AWS GovCloud credentials for Cloud Provisioning and Governance**

    **Note:** Skip this procedure if your organization does not use AWS GovCloud \(US\).

    To securely access data on your provider account, the Discovery process must present appropriate credentials. An AWS GovCloud \(US\) region is an isolated AWS region that meets stringent US government security and compliance requirements to host sensitive workloads. Cloud Provisioning and Governance supports all AWS GovCloud \(US\) services.

-   **5. Create a service account for AWS GovCloud**

    **Note:** Skip this procedure if your organization does not use AWS GovCloud \(US\).

    If your organization uses AWS GovCloud \(US\) regions, you create a service account for each region. These credentials that you create are used for Cloud Discovery, Cloud Provisioning and Governance, and Cloud Cost Management.

-   **6. Set up a cloud account and service account for AWS**

    A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

-   **8. Define the schedule for downloading AWS billing data**

    Define the scheduled job that regularly uses a MID Server to download billing data from the provider. Cloud Provisioning and Governance saves the data in a cost table and uses the information to generate reports.


## Next steps

When you have finished all Day-1 and Day-2 procedures in this setup guide, see the [Cloud Provisioning and Governance administration guide](../../cloud-management-v2/concept/cloud-configuration.md) for information on using the Cloud Provisioning and Governance application in your organization.

