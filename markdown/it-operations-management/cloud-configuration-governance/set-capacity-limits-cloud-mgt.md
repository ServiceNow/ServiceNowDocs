---
title: Set capacity limits on user requests for resources
description: Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Additional Cloud Provisioning and Governance setup on day 2, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Set capacity limits on user requests for resources

Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.

## Before you begin

-   A cloud account must exist with service accounts and associated datacenters. You must run on-demand Discovery to discover datacenters before you can schedule Discovery.
-   Use the Cloud Discovery Workspace, and at least version 1.15 of Discovery and Service Mapping Patterns from the ServiceNow Store.

Role required: sn\_cmp.cloud\_admin

## About this task

**Note:** You can also use quotas to set per-user and total capacity limitations on resources. See [Quotas and resource order controls](../../cloud-management-v2/concept/quotas-1.md).

## Procedure

1.  Navigate to **All** &gt; **Cloud Admin Portal** &gt; **Manage** &gt; **Cloud Accounts**.

2.  Click a cloud account, and then, on the **Datacenters** tab, select a datacenter.

3.  Set the state to **Draft**.

4.  On the **Capacity Limits** tab, set the **Capacity Limit** values as needed.

    ![Use the Capacity Limits tab to limit options like the number of CPUs](../image/capacity-limits-tab.png)

    |Value|Description|
    |-----|-----------|
    |Discovered|Total value discovered by the Discovery process for all resources in the selected service account.|
    |Provisioned|Total value provisioned for the selected service account.|
    |Capacity Limit|Maximum allowed value calculated as the sum for all resources in the selected service account.|
    |Unit|Unit of measure for the specified value. For example, storage is measured in units of GB.|

5.  Click **Update**.

6.  Set the state to **Published**.


## What to do next

Click **Discover Now** to run Discovery on the logical datacenters.

**Parent Topic:**[Additional Cloud Provisioning and Governance setup on day 2](../concept/cloud-mgt-general-setup-day-2.md)

