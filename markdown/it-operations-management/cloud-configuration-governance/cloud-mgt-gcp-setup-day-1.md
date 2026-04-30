---
title: Day 1 setup guide for Google Cloud through Cloud Services Catalog Terraform Connector
description: To set up Google Cloud for the first time, follow the steps in this Day 1 setup guide in the order they are presented. After completing the Day 1 setup, you can proceed with the optional Day 2 configuration steps as needed, in any order. Detailed instructions for each step are provided in the sections below.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Day 1 setup guide for Google Cloud through Cloud Services Catalog Terraform Connector

To set up Google Cloud for the first time, follow the steps in this Day 1 setup guide in the order they are presented. After completing the Day 1 setup, you can proceed with the optional Day 2 configuration steps as needed, in any order. Detailed instructions for each step are provided in the sections below.

**Note:** The ServiceNow® Cloud Provisioning and Governance: Google Cloud Connector is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Roles required to set up Google Cloud Platform

-   Operations in the Google Cloud Console require the Google administrator role.
-   Operations in Cloud Provisioning and Governance require the sn\_cmp.cloud\_admin role.

## About terms that Cloud Provisioning and Governance uses

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings. In the Google Cloud Platform, the region-specific containers for virtual resources are called regions. In ServiceNow cloud data model, regions are called datacenters or logical datacenters \(LDCs\). The term logical is used to reinforce the idea that Cloud Provisioning is provider-agnostic. All infrastructure or applications that are deployed using Cloud Provisioning are associated with a datacenter.

## Quick overview of the setup process

Your Day 1 setup process includes these tasks:

-   If needed: Request the Cloud Provisioning and Governance application.
-   [Download the Connector app](https://www.servicenow.com/docs/access?context=download-app-first-time&version=zurich&pubname=zurich-security-management&ft:locale=en-US) and supporting store apps on the ServiceNow Store and [activate](https://www.servicenow.com/docs/access?context=activate-entitled-store-app&version=zurich&pubname=zurich-security-management&ft:locale=en-US) the store applications.
-   Assign appropriate roles to cloud admins and end users.
-   On the provider portal, collect your account settings and the credentials that the Discovery process will use \(through a MID Server\) to programmatically access your provider accounts. Securely associate the account settings and credentials with a service account in Cloud Provisioning.
-   Set up the MID Servers that will handle secure communications with the provider API endpoints.
-   Set up a cloud account to represent your entire managed cloud infrastructure and set up a service account that works with one of your provider accounts. You specify which datacenters in the service account should be included in the cloud account. \(Later, on "Day 2", you can set up additional cloud accounts and service accounts from the same or other providers.\)
-   To populate the CMDB with resource data for all datacenters, you manually run the Discovery process on each datacenter in the service account. Then, to ensure that the data continues to be updated, you configure Discovery to run on a regular schedule. Your cloud account might look like this:

    ![Structure of a cloud account on Day 1](../image/cloud-acct-day-1.png "Structure of a cloud account on Day 1")

-   Providers offer services that can auto-update the CMDB whenever a create/modify/terminate life-cycle change or configuration update occurs to a resource. You can configure the service to integrate directly with Cloud Provisioning and Governance.

## What you will do to integrate your Google Cloud Platform cloud accounts

Detailed instructions for each procedure follow this overview.

1.  Get the CSC Terraform Connector app on the ServiceNow Store
2.  Assign roles to Google Cloud Platform users

    You assign Cloud Provisioning and Governance roles to user groups and to individual users based on user activities and responsibilities.

3.  [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md)

    To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. You can set up the MID Servers on your network or in one of your cloud networks.

    **Note:** Data is encrypted to the MID Server and between the MID Server and the API endpoint. To ensure high performance and security, you should configure one or more MID Server for each datacenter under management. Configure the MID Server even if you have already configured other MID Servers while setting up Cloud Provisioning and Governance for another cloud provider.

4.  Specify the credentials that CSC Terraform Connector uses to access Google Cloud Platform data

    To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you open the Google Cloud Console to identify the Google Cloud Platform project that will have programmatic access to your Google Cloud Platform data. You then securely store the credentials in a service account in your instance.

5.  Set up a cloud account and service account for Google Cloud Platform

    A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter.


## Next steps

When you have finished all Day-1 and Day-2 procedures in this setup guide, see the [Cloud Provisioning and Governance administration guide](../../cloud-management-v2/concept/cloud-configuration.md) for information on using the Cloud Provisioning and Governance application in your organization.

