---
title: Blueprint attributes
description: When you add a blueprint operation to a resource, the system adds the appropriate attributes. You can choose whether or not to make the attributes available as catalog properties on the form when the system performs the operation.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Build a Cloud Provisioning blueprint, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Blueprint attributes

When you add a blueprint operation to a resource, the system adds the appropriate attributes. You can choose whether or not to make the attributes available as catalog properties on the form when the system performs the operation.

## Common attributes for the provisioning operation for virtual machines

|Attribute|Description|
|---------|-----------|
|VmFolderName|The name of the virtual machine folder.|
|ResourceGroupName|The name of the resource group to which the resource belongs.|
|StackName|The name of the stack that the user is provisioning.|
|CloudAccount|The cloud account to which the resource stack belongs.|
|OSProfile|The resource profile, in this case the Operating System profile, upon which the cloud resource is based.|
|DiscoverAndAttachIP|Finds a free elastic IP and assigns it to a virtual machine on AWS. By default, if a VM is deployed on a VPC in AWS, it will not get a public IP. If elastic IPs are not available, no IP can be assigned to the VM.|

**Warning:** It is recommended that you do not use **KeyPreference**. If you use the attribute, do not set **KeyPreference** to `user`.

**Parent Topic:**[Build a Cloud Provisioning blueprint](../task/create-blueprint-cmp.md)

**Related topics**  


[Add a resource operation to the execution plan](../task/add-resource-operation-cmp.md)

[Execute blueprint operations in parallel](../task/execute-blueprint-operations-parallel.md)

[Configure a blueprint rule](../task/configure-a-blueprint-rule.md#)

