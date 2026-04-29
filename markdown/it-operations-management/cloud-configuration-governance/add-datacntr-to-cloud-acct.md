---
title: Add a datacenter to a cloud account
description: At any time, you can add a logical datacenter to the cloud infrastructure that is represented by a cloud account.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up cloud accounts for VMware, Day 1 setup guide for VMware on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add a datacenter to a cloud account

At any time, you can add a logical datacenter to the cloud infrastructure that is represented by a cloud account.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Cloud Accounts**.

2.  Open a cloud account, set the state to **Draft**, and then click **Configure** in the form header.

3.  Click the **Datacenters** tab and then select the **Service Account** that holds the credentials that enable access to the provider account that includes the datacenter to add.

    ![Add a datacenter](../image/add-datacenter-to-srvc-acct.png)

    When you select the service account, the list of discovered datacenters for the service account appears.

    **Note:** If the expected datacenters do not appear, click **Discover Datacenters** to update the list. Discovery runs and displays all datacenters associated with the service account.

4.  Select the datacenters to add and then click **Save**.

    In the example, you select **ap-northeast-2**.


## Result

The datacenters are added to the cloud account and appear on the **Datacenters** tab. When Discovery runs, the resources in the datacenter appear on the Resources tab.

![New datacenter on the cloud account](../image/new-datacenter-on-cloud-acct.png "New datacenter on the cloud account")

