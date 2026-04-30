---
title: Cloud accounts
description: A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Cloud accounts

A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

From a cloud account, you can:

-   Add LDCs. A logical datacenter \(LDC\) is a region-specific virtual cloud that is associated with a service account. The datacenter hosts your cloud resources.
-   Run Discovery on LDCs to update the CMDB with configuration changes or life cycle changes \(create/modify/terminate\) for each resource in each logical datacenter \(LDC\) that is associated with the cloud account.
-   Set capacity limits on cloud services like virtual machines, virtual CPUs, virtual networks, aggregate storage volume size, and others. Set limits to help ensure that cloud resources are provisioned at appropriate scales. Limits are especially important for capacity-constrained environments like private clouds.
-   Publish a cloud account to enable business teams to deploy stacks.

## Structure of a cloud account

An advantage of cloud accounts is that you can group specified service accounts with only the regions \(datacenters\) that you want to allow cloud resources in. For example, your AWS account could have more than a dozen datacenters globally. However, you might use only one or two regions. To conform with your security and compliance rules, you might not want any resources provisioned to additional regions around the world.

![Structure of a cloud account](../../cloud-management-v2-setup/image/cloud-acct-makeup.png)

A cloud account can contain as many service accounts as necessary in the following scenarios:

<table id="table_mkd_wfp_l2b"><thead><tr><th>

Structure

</th><th>

Supported

</th><th>

Not supported

</th></tr></thead><tbody><tr><td>

Add the same service account as many times as necessary, provided each entry is associated with a different LDC.

</td><td align="center">

X

</td><td align="center">

 

</td></tr><tr><td>

Add the same LDC from different service accounts in one cloud account.

</td><td align="center">

 

</td><td align="center">

X

</td></tr><tr><td>

Add different LDCs from different service accounts to a particular cloud account, provided the regions are not the same.Example: You have us-west-1 in serviceaccount1 and us-west-2 in serviceaccount2. Both can be added to cloudaccount1. However, both us-west-1 in serviceaccount1 and us-west-1 in serviceaccount2 cannot be added to cloudaccount1.

</td><td align="center">

X

</td><td align="center">

 

</td></tr></tbody>
</table>## Update a cloud account

You keep a cloud account in the **Draft** state until you are ready to make the datacenters and capacity limits available for use — in blueprints and the Cloud User Portal, for example. You can change the state to **Published** after you run Discovery.

## Set up an additional cloud account

See [Set up an additional cloud account](../../cloud-management-v2-setup/task/add-cloud-account-cloud-mgt.md).

## Add a datacenter to a cloud account

At any time, you can add a logical datacenter to the cloud infrastructure that is represented by a cloud account. See [Add a datacenter to a cloud account](../../cloud-management-v2-setup/task/add-datacntr-to-cloud-acct.md).

## Set capacity limits on user requests for resources

Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.

[Set capacity limits on user requests for resources](../../cloud-management-v2-setup/task/set-capacity-limits-cloud-mgt.md)

-   **[Service categories discovered in AWS](../reference/aws-discovered-services.md)**  
The Discovery process discovers AWS services.
-   **[Service categories discovered in Azure](../reference/azure-discovered-services.md)**  
The Discovery process discovers Microsoft Azure services.

**Parent Topic:**[Cloud Provisioning and Governance administration guide](cloud-configuration.md)

**Related topics**  


[Domain separation and Cloud Provisioning and Governance](domain-separation-cloud-management.md)

[Domain separation in Cloud Provisioning and Governance - considerations for service providers](../reference/cloud-mgmt-dom-sep-recommend.md)

[Cloud Provisioning and Governance Recipes](../reference/cloud-mgmt-recipes-day-2.md)

[Cloud Admin Portal](cloud-admin-portal.md)

[Moving Cloud Provisioning and Governance content across environments](move-content-intro.md)

