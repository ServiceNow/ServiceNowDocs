---
title: Configuring Cloud Services Catalog
description: You can configure the Cloud Services Catalog application so that so can begin to automate cloud management tooling.
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Configuring Cloud Services Catalog

You can configure the Cloud Services Catalog application so that so can begin to automate cloud management tooling.

## Configuration overview

The configuration is in a sequential order where you create and set up the prerequisites first, and then integrate the credentials with your Cloud account profile. These setup steps are identified as Day 1 and Day 2 tasks.

The Cloud Services Catalog Day 1 configuration includes tasks like creating MID Servers, setting up your cloud providers, Amazon Web Services, or Microsoft Azure Cloud. You can also associate it with your cloud account, and schedule the datacenter [Discovery](../../discovery/reference/r-discovery.md).

An overview of the Day 1 setup process is outlined here:

1.  Request the Cloud Services Catalog application, if needed.
2.  Assign the appropriate roles to your cloud users.
3.  Set up the MID Servers that handle the secure communications with the provider API endpoints.
4.  On the provider portal, collect your account settings and the credentials that the [Discovery](../../discovery/reference/r-discovery.md) process uses \(through a MID Server\) to access your provider accounts.
5.  Securely associate the account settings and credentials with a service account in Cloud Services Catalog.
6.  Set up a cloud account to represent your entire managed cloud infrastructure, and set up a service account that works with one of your provider accounts.
7.  Specify the datacenters in the service account that should be included in the cloud account.

On Day 2, you can set up the additional cloud accounts and service accounts from the same or other providers.

1.  Use the Configuration Management Database \(CMDB\) data to help you request and manage the cloud resources and manage your cloud infrastructure.
2.  Manually run the [Discovery](../../discovery/reference/r-discovery.md) process on each datacenter in the service account to populate the CMDB with the resource data for all datacenters.
3.  Configure Discovery to run on a regular schedule to ensure that the data remains updated.

## Using Guided Setup to implement Cloud Services Catalog

Guided Setup provides a sequence of tasks that help you configure CSC on your ServiceNow instance. To open Guided Setup for Cloud Services Catalog, navigate to **All** &gt; **Cloud Services catalog- Guided Setup** on your instance.

For more information, see Guided Setup.

-   **[Install Cloud Services Catalog](install-csc.md)**  
You can install the Cloud Services Catalog application purchased from the ServiceNow® Store, to make it available on your instance. The application also includes demo data and installs related to ServiceNow applications and plugins, if you don’t have them installed already.
-   **[Cloud Services Catalog setup for the Day 1 configuration task](setting-up-cloud-services.md)**  
You're ready to do the Day 1 configuration task of setting up the Cloud Services Catalog application for the first time. You can do the optional Day 2 setup and configure procedures as needed, in any order.
-   **[Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline](integrating-azure-devops-and-cicd-pipeline.md)**  
You can process the release request from the Cloud Services Catalog workflow with Azure DevOps for end-to-end automation of the development process, including provisioning the resources, and deploying and monitoring the applications.
-   **[Integrating Ansible with Cloud Services Catalog](integrating-ansible-with-cloud-services-catalog.md)**  
Integrate Ansible with Cloud Services Catalog as a Day 1 activity. With this activity, you can deploy an Ansible job template via a ServiceNow catalog item.
-   **[Cloud Services Catalog administration guide](cloud-services-catalog-administration-guide.md)**  
After you set up the Cloud Services Catalog application, you must set up some additional items so that your users can request and manage any cloud resource.

**Parent Topic:**[Cloud Services Catalog](csc-home.md)

