---
title: Create a compute security group profile
description: A compute security group profile applies specified security rules to newly-provisioned resources. You map a compute security group profile to a cloud account, a datacenter, a Compute Security Group template, and security rules for the template.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a compute security group profile

A compute security group profile applies specified security rules to newly-provisioned resources. You map a compute security group profile to a cloud account, a datacenter, a Compute Security Group template, and security rules for the template.

## Before you begin

You must have a cloud account with datacenters. You must run Discovery on the service accounts to populate the datacenters.

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Profiles**.

2.  In the **Profiles** list, select **Compute Security Group Profile** and then click **New**.

3.  Enter a unique and descriptive **Name** and **Description** for the profile and then click **Submit**.

    The profile is created.

4.  Map the profile to a template.

    1.  In the list, click the profile that you created.

    2.  In the **Compute Security Group Profile Mappings** related list, click **New**, fill in the form, and then click **Submit**.

        ![Compute security group profile](../image/compute-securitygrp-profile.png)

<table id="table_n3n_zvt_ddb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud Account

</td><td>

Select a cloud account for the profile.

</td></tr><tr><td>

Location

</td><td>

Select the datacenter that belongs to the cloud account.

</td></tr><tr><td>

Compute Security Group Template \[cmdb\_ci\_security\_grp\_template\]

</td><td>

Select or create a template that the profile should be mapped to.To create a new template, click the list icon and then click **New**. Enter a name and a template ID and click **Submit**.

 Click the reference icon \(![Reference image](../../../common/image/icon-reference.png)\) to view the details of the template.

</td></tr></tbody>
</table>5.  Add rules to the template.

    You can create more than one rule per template.

    1.  In the **Security Group Profile Mappings** related list, under the **Compute Security Group Template** heading, click the template name.

    2.  In the **Compute Security Group Rule Template** related list, click **New**, fill in the form, and then click **Submit**.

        |Field|Description|
        |-----|-----------|
        |CIDR Range|Specify a CIDR range. For example, 10.0.0.0/24.|
        |IP Protocol|Select an IP protocol. In Azure, the protocols supported are TDP and UDP. ICMP is not supported.|
        |From Port|Specify the source port number.|
        |Is Outbound|Enter `0` for inbound and `1` for outbound.|
        |Name|Specify a name for the rule.|
        |Network Type|Select the type of network.|
        |To Port|Specify the destination port number.|


**Parent Topic:**[Resource Profiles](../concept/cloud-resource-profiles.md)

**Related topics**  


[Discover all datacenters in a service account on-demand](../../cloud-management-v2-setup/task/disco-datacntrs-in-srv-acct.md)

