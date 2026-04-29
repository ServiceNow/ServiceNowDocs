---
title: Create a compute profile
description: A compute profile specifies the hardware to use for newly-provisioned virtual machines. A compute profile maps to a cloud account, a datacenter, and a hardware template.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a compute profile

A compute profile specifies the hardware to use for newly-provisioned virtual machines. A compute profile maps to a cloud account, a datacenter, and a hardware template.

## Before you begin

Role required: sn\_cmp.cloud\_admin

You must have a cloud account with datacenters. You must run Discovery on the service accounts to populate the datacenters.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Profiles**.

2.  In the **Profiles** list, select **Compute Profile** and then click **New**.

3.  Enter a unique and descriptive **Name** and **Description** for the profile and then click **Submit**.

    The profile is created.

4.  Click the resource profile that you created.

5.  Map the profile to a template.

    1.  In the list, click the profile that you created.

    2.  In the **Profile Mappings** related list, click **New**, fill in the form, and then click **Submit**.

        ![Compute resource profile](../image/compute-profile-mapping.png "Example compute profile")

<table id="table_n3n_zvt_ddb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud Account

</td><td>

Select a cloud account that the profile is valid for.

</td></tr><tr><td>

Location

</td><td>

Select the datacenter that the profile is valid for.

</td></tr><tr><td>

Hardware Template \[cmdb\_ci\_compute\_template\]

</td><td>

Select the hardware type that the profile should be mapped to.Click the reference icon \(![Reference image](../../../common/image/icon-reference.png)\) to view the details of the template.

</td></tr></tbody>
</table>
**Related topics**  


[Discover all datacenters in a service account on-demand](../../cloud-management-v2-setup/task/disco-datacntrs-in-srv-acct-1.md)

