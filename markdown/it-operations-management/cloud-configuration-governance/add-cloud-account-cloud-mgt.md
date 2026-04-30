---
title: Set up an additional cloud account
description: During initial installation, you set up one cloud account. To organize and compartmentalize your infrastructure, you can set up additional cloud accounts to include different providers or service accounts or datacenters.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Additional Cloud Provisioning and Governance setup on day 2, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Set up an additional cloud account

During initial installation, you set up one cloud account. To organize and compartmentalize your infrastructure, you can set up additional cloud accounts to include different providers or service accounts or datacenters.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## About this task

A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account. See [Cloud accounts](../../cloud-management-v2/concept/cloud-accounts.md) for detailed information.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Cloud Accounts**.

2.  Click **New**, enter a unique and meaningful **Name** and **Description**, select the cloud **Provider** for the account \(**MyProvider** in the example\), and then click **Next**.

    ![Create a cloud account](../image/create-cloud-account.png)

    Based on the provider you select, the **Service Account** field is populated.

3.  Select the appropriate **Service Account**.

    A list of discovered datacenters appears. If no datacenters appear, click **Discover Now**. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct.md) for details.

4.  Select each of the datacenters that you want to associate with the cloud account, click **Save**, and then close the popup.

    The datacenters appear on the **Datacenters** tab for the cloud account.

    ![New datacenter on the cloud account](../image/new-datacenter-on-cloud-acct.png)

5.  When the datacenters appear, select one or more datacenters to include in the cloud account and then click **Save**.

    **Note:**

    -   Select only those LDCs/Regions where your infrastructure resources are present. If you don't have any resources under these new data centers, exclude them while you run the full discovery.
    -   To discover resources in regions/ LDCs such as, North America\(US East, US West and Canada Central\), South America, Europe, Africa, Middle East and Asia Pacific, raise an access request to the required endpoints with GCP Support.
    The Cloud Account dashboard appears. The datacenters that you selected appear on the **Datacenters** tab.

6.  Click a datacenter.

    The following lists appear:

    -   **Resources**: Cloud resources for the current datacenter. Run Discovery to populate the CMDB for the datacenter and populate the tab. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct-1.md).
    -   **Capacity Limits**: Limits on virtual CPUs, virtual networks, storage volume size, and other services. See [Set capacity limits on user requests for resources](set-capacity-limits-cloud-mgt-1.md).
    -   **Discovery Log**: The process creates a log record for each action associated with a discovery status.
7.  Repeat the process to add as many service accounts as needed.


## What to do next

Repeat the process to create additional cloud accounts as needed. Run Discovery and set capacity limits for each datacenter.

**Parent Topic:**[Additional Cloud Provisioning and Governance setup on day 2](../concept/cloud-mgt-general-setup-day-2.md)

