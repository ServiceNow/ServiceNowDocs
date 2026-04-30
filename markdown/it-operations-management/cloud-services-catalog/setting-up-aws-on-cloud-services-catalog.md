---
title: Set up Amazon Web Services on Cloud Services Catalog
description: Integrate Cloud Services Catalog with your Amazon Web Services account as a part of the Day 1 configuration task of setting up the application for the first time.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud Services Catalog setup for the Day 1 configuration task, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Amazon Web Services on Cloud Services Catalog

Integrate Cloud Services Catalog with your Amazon Web Services account as a part of the Day 1 configuration task of setting up the application for the first time.

## Before you begin

Collect your account settings and credentials from the provider portal. These settings and credentials help you to distinguish the resources in one account from another account and sign in or authenticate to AWS. Permission policies specify your approvals within the resources in the account.

Role required:

-   Administrator for operation in AWS or AWS Management Console
-   sn\_cmp.cloud\_admin role for operations in Cloud Services Catalog

## Procedure

1.  Assign roles to AWS users of Cloud Services Catalog and to individual users by their activities and responsibilities.

    For more information, see [Assign roles to AWS users of Cloud Services Catalog](../../cloud-management-v2-setup/task/aws-assign-roles-cloud-mgt.md).

2.  Install and configure MID Servers for Cloud Discovery and Cloud Provisioning and Governance.

    To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. For more information, see [Install and configure MID Servers for Cloud Discovery and Cloud provisioning and governance](../../it-operations-management/task/mid-server-configuration-cloud.md).

3.  Set up the MID Server on your network or in one of your cloud networks and configure it for Cloud Services Catalog to use a proxy server.

    Using a proxy server supports all cloud-based activities, such as running Discovery, billing downloads, provisioning virtual machines, and running life-cycle operations on virtual machines.

4.  Configure one or more MID Servers for each datacenter for high performance and security.

    Data is encrypted to the MID Server and between the MID Server and the API endpoint.

5.  Configure the MID Server even if you have already configured other MID Servers while you were setting up Cloud Services Catalog for another cloud provider.

6.  Configure access to the AWS accounts by using permanent AWS credentials.

    -   To securely access data on your provider account, the Discovery process must present the appropriate credentials.
    -   To make the credentials available to Discovery and Cloud Services Catalog, you first create a user with programmatic access to the AWS Management Console.
    -   You can securely store the credentials in a service account on the ServiceNow AI Platform®.
    -   For more information, see [Configure access to the AWS accounts using permanent AWS credentials](../../it-operations-management/task/aws-create-creds-cloud-mgt.md).
7.  Set up a cloud account and a service account for AWS.

    A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get the data on each resource in each specified datacenter. A cloud account is the logical representation in Cloud Services Catalog of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts, including the service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account. For more information, see [Set up a cloud account and service account for AWS](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md).


**Parent Topic:**[Cloud Services Catalog setup for the Day 1 configuration task](setting-up-cloud-services.md)

