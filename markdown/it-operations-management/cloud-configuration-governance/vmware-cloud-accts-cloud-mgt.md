---
title: Set up cloud accounts for VMware
description: A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Day 1 setup guide for VMware on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Set up cloud accounts for VMware

A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## About this task

See [Cloud accounts](../../cloud-management-v2/concept/cloud-accounts.md) for detailed information.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Cloud Accounts**.

2.  Click **New**, enter a unique and meaningful **Name** and **Description**, and then select the cloud **Provider** for the account \(VMware vCenter\).

    ![Create a cloud account](../image/create-cloud-account.png)

3.  Click **Next**.

    Based on the provider you select, the **Service Account** field is populated and a list of discovered datacenters appears. If no datacenters appear, click **Discover Datacenters** to find them. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct.md) for details.

4.  Select one or more datacenters to associate with the cloud account, click **Save**, and then close the popup.

    The Cloud Account dashboard appears. The datacenters that you selected appear on the **Datacenters** tab.

5.  Click a datacenter.

    The following lists appear:

    -   **Resources**: Cloud resources for the current datacenter. Run Discovery to populate the CMDB for the datacenter and populate the tab. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct.md).
    -   **Capacity Limits**: Limits on virtual CPUs, virtual networks, storage volume size, and other services. [Set capacity limits on user requests for resources](set-capacity-limits-cloud-mgt.md)
    -   **Discovery Log**: The process creates a log record for each action in an datacenter.
    **Note:**

    If you are on a domain separated instance, only those events that are updated to the CMDB and belong to your domain are visible. Events create configuration items \(CI\) in the same domain as the cloud service account they are mapped to.


## What to do next

Repeat the process to create additional cloud accounts as needed. Run Discovery and set capacity limits for each datacenter.

