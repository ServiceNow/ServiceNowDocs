---
title: Setting up Google Cloud Platform on Cloud Services Catalog
description: Integrate Cloud Services Catalog with your Google Cloud Platform account as a part of the Day 1 configuration task toward setting up CSC for the first time.
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Cloud Services Catalog setup for the Day 1 configuration task, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Setting up Google Cloud Platform on Cloud Services Catalog

Integrate Cloud Services Catalog with your Google Cloud Platform account as a part of the Day 1 configuration task toward setting up CSC for the first time.

## Before you begin

Collect your account settings and credentials from the provider portal. These settings and credentials help you to distinguish the resources in one account from another account and sign in or authenticate to Google Cloud. Permission policies specify your approvals within the resources in the account.

Role required:

-   Administrator for operation in Google Cloud or Google Cloud Management Console
-   sn\_cmp.cloud\_admin role for operations in CSC

To learn more about setting up Google Cloud with CSC Terraform Connector app for the first time, see [Day 1 setup guide for Google Cloud through Cloud Services Catalog Terraform Connector](../../cloud-management-v2-setup/concept/cloud-mgt-gcp-setup-day-1.md).

## Procedure

1.  Assign roles to Google Cloud users of CSC and to individual users by their activities and responsibilities.

    For more information, see [Assign roles to Google Cloud Platform users](../../cloud-management-v2-setup/task/gcp-assign-roles-cloud-mgt.md).

2.  Install and configure MID Servers for Cloud Discovery and Cloud Provisioning and Governance.

    To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. For more information, see [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md).

3.  Set up the MID Server on your network or in one of your cloud networks and configure it for CSC to use a proxy server.

    Using a proxy server supports all cloud-based activities, such as running Discovery, billing downloads, provisioning virtual machines, and running life-cycle operations on virtual machines.

4.  Configure one or more MID Servers for each datacenter for high performance and security.

    Data is encrypted to the MID Server and between the MID Server and the API endpoint.

5.  Configure the MID Server even if you have already configured other MID Servers while you were setting up Cloud Services Catalog for another cloud provider

6.  Create Service Account and the keys \(credentials\) in Google Cloud if you don not have it.

    You can securely store the credentials in a service account. You would need Service Account Key Admin \(roles/iam.serviceAccountKeyAdmin\) IAM role on the project, or the service account whose keys you want to manage. These permissions can be provided by administrator. To securely access data on your provider account, the Discovery process must present the appropriate credentials.

    For more information, see [Set up Google Cloud Platform service accounts](../../it-operations-management/concept/set-up-gcp-service-accounts.md).

7.  Set up a cloud account and a service account for Google Cloud Platform.

    -   A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get the data on each resource in each specified datacenter.
    -   A cloud account is the logical representation in Cloud Services Catalog of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts, including the service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.
    For more information, see [Set up a cloud account and service account for Google Cloud Platform](../../cloud-management-v2-setup/task/gcp-first-cld-and-srvc-accts.md).


**Parent Topic:**[Cloud Services Catalog setup for the Day 1 configuration task](../concept/setting-up-cloud-services.md)

