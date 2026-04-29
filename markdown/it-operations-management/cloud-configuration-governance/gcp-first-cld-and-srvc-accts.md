---
title: Set up a cloud account and service account for Google Cloud Platform
description: A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Day 1 setup guide for Google Cloud through Cloud Services Catalog Terraform Connector, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up a cloud account and service account for Google Cloud Platform

A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

## Before you begin

Role required: none

-   Download and activate the CSC Terraform Connector from the ServiceNow® Store. To try out the [Out Of Box Catalogs using Cloud Services Catalog](../../cloud-services-catalog/concept/out-of-the-box-catalog-items.md) for Google, install the CSC content pack.
-   Operations in the Google Cloud Console require the Google administrator role.
-   Operations in Cloud Provisioning and Governance require the sn\_cmp.cloud\_admin role.

## About this task

When you finish the Day-1 setup process, your cloud account might look like this:

![Structure of a cloud account on Day 1](../image/cloud-acct-day-1.png "Structure of a cloud account on Day 1")

## Procedure

1.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Cloud Accounts**.

2.  Select or create the cloud account:

    -   Select an existing cloud account:
        1.  On the Cloud Account page, click **Configure**.
        2.  On the General Information page, click **Next** and then continue with the next step.
    -   Create a cloud account:
        1.  On the General Information page, click **New** and then enter a unique and meaningful **Name** and **Description** for the cloud account.
        2.  Select the provider.
        3.  Click **Next** and then continue with the next step.
3.  On the Datacenters page, create a service account: Click the **+** next to the **Service Account** field, and then fill in the form for the service account.

4.  From the JSON key file that is associated with the service account, populate the **project\_id** value into the **Account ID** field.

    **Note:** You can use the import JSON file option to populate. For more details, see [Configure the Google API credentials for Cloud Discovery](../../discovery/task/itom-create-google-api-credentials.md).

5.  In the **Discovery credentials** field, select the appropriate credentials for the service account.

    These are the credentials that you generated in the [Specify the credentials that CSC Terraform Connector uses to access Google Cloud Platform data](gcp-create-creds-cloud-mgt-1.md) procedure.

6.  Leave the **Datacenter URL** field blank.

7.  Fill in the remaining fields:

    |Field|Description|
    |-----|-----------|
    |**Datacenter type**|Select **Google Cloud Platform Datacenter**.|
    |**Datacenter discovery status**|Select **Google Cloud Platform Datacenter**.|
    |**Should pull events**|Enables Cloud Provisioning and Governance to collect events from resource types in Google Project LDCs in the `sn_cmp_cloud_event_list`.|

8.  Click **Submit** to create the service account.

9.  Click **Discover Datacenters**.

10. When the datacenters appear, select one or more datacenters to include in the cloud account and then click **Save**.

    **Note:**

    -   Select only those LDCs/Regions where your infrastructure resources are present. If you don't have any resources under these new data centers, exclude them while you run the full discovery.
    -   To discover resources in regions/ LDCs such as, North America \(US East, US West and Canada Central\), South America, Europe, Africa, Middle East and Asia Pacific, raise an access request to the required endpoints with GCP Support.
    The Cloud Account dashboard appears. The datacenters that you selected appear on the **Datacenters** tab.

11. Click a datacenter.

    The following lists appear:

    -   **Resources**: Cloud resources for the current datacenter. Run Discovery to populate the CMDB for the datacenter and populate the tab. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct-1.md).
    -   **Capacity Limits**: Limits on virtual CPUs, virtual networks, storage volume size, and other services. See [Set capacity limits on user requests for resources](set-capacity-limits-cloud-mgt-1.md).
    -   **Discovery Log**: The process creates a log record for each action associated with a discovery status.
12. Repeat the process to add as many service accounts as needed.


## What to do next

After you complete all procedures in this initial "Day 1" setup, you can create additional cloud accounts and service accounts to organize and compartmentalize your cloud infrastructure.

**Related topics**  


[Set up an additional cloud account](add-cloud-account-cloud-mgt.md)

[\(Optional\) Add a Google Cloud Platform service account to the cloud account](gcp-add-service-account-cloud-mgt.md)

[Discovery for Google Cloud Platform](../../service-mapping/reference/google-gcp-discovery-pattern.md)

