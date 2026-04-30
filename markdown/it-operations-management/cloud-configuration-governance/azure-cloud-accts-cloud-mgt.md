---
title: Set up a cloud account for Azure
description: A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up a cloud account for Azure

A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## About this task

See [Cloud accounts](../../cloud-management-v2/concept/cloud-accounts.md) for more information about cloud accounts.

**Note:** Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings. In Azure, the region-specific containers for virtual resources are called regions. In Cloud Provisioning and Governance, regions are called datacenters or logical datacenters \(LDCs\). The term logical is used to reinforce the idea that Cloud Provisioning is provider-agnostic. All infrastructure or applications that are deployed using Cloud Provisioning are associated with a datacenter..

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Cloud Accounts**.

    ![Cloud Admin portal](../../cloud-management-v2/image/admin-portal.png "Cloud Admin portal")

2.  Click **New**, enter a unique and meaningful **Name** and **Description**, and then select the cloud **Provider** for the account \(Azure\).

    ![General Information page of the create cloud account process](../image/create-cloud-account.png)

3.  Click **Next**.

    Based on the provider you select, the **Service Account** field is populated and a list of discovered datacenters appears. If no datacenters appear, click **Discover Datacenters** to find them. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct-1.md) for details.

4.  When the datacenters appear, select one or more datacenters to include in the cloud account and then click **Save**.

    **Note:**

    -   Select only those LDCs/Regions where your infrastructure resources are present. If you don't have any resources under these new data centers, exclude them while you run the full discovery.
    -   To discover resources in regions/ LDCs such as, North America \(US East, US West and Canada Central\), South America, Europe, Africa, Middle East and Asia Pacific, raise an access request to the required endpoints with GCP Support.
    The Cloud Account dashboard appears. The datacenters that you selected appear on the **Datacenters** tab.

5.  Click a datacenter.

    The following lists appear:

    -   **Resources**: Cloud resources for the current datacenter. Run Discovery to populate the CMDB for the datacenter and populate the tab. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct-1.md).
    -   **Capacity Limits**: Limits on virtual CPUs, virtual networks, storage volume size, and other services. See [Set capacity limits on user requests for resources](set-capacity-limits-cloud-mgt-1.md).
    -   **Discovery Log**: The process creates a log record for each action associated with a discovery status.
6.  Repeat the process to add as many service accounts as needed.


