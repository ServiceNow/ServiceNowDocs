---
title: Resource Profiles
description: Resource profiles are cloud provider-agnostic definitions that specify the allowed attribute values for a resource. Resource profiles enable you to control the choices that the user sees when requesting a cloud resource. As a result, you do not need to define a unique blueprint for each variation of the resource.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Resource Profiles

Resource profiles are cloud provider-agnostic definitions that specify the allowed attribute values for a resource. Resource profiles enable you to control the choices that the user sees when requesting a cloud resource. As a result, you do not need to define a unique blueprint for each variation of the resource.

**Note:** In addition to the cloud-agnostic profiles, you can add provider public images to the Cloud Provisioning and Governance catalog. See [Add an AWS public image to Cloud Provisioning and Governance](../task/add-public-image-aws.md) and [Add an Azure public image to Cloud Provisioning and Governance](../task/add-public-image-azure.md).

## Example: Compute profile

You might create a compute profile named **Micro** and map it to a "micro" hardware type, with specified values for memory and CPU. Later, when a user selects a compute resource while requesting a virtual server, **Micro** appears as an option in the list of available compute resources. The user does not need to specify values for memory and CPU — the values come from the profile.

![Compute profile on the request form](../image/compute-profile-request.png "Compute profile on the request form")

## Resource Profile mappings

Resource profiles create mapping associations between the following items:

-   A cloud account.
-   A logical datacenter in the cloud account.
-   A specific resource type in the CMDB that provides the attributes.
-   Optional: A pricing value that appears to users when they request a resource that uses the resource profile.

By default for AWS and Azure, Cloud Provisioning and Governance maps profiles to templates after Discovery runs. For other providers, such as Google cloud, you must manually associate the profile with the correct template and datacenter.

## Resource types

Each resource profile has associated attributes. The attributes depend on the resource types that are populated after you run Discovery on a cloud account.

<table id="table_wkh_rm1_xy"><thead><tr><th>

Resource profile type

</th><th>

Description and attributes

</th><th>

Resource type and template

</th></tr></thead><tbody><tr><td>

Application profile

</td><td>

An application profile specifies application software to install on newly-provisioned resources. Users can select applications when they request a stack. Use application profiles when you integrate with configuration management \(continuous delivery\) providers such as Ansible playbooks. Attributes: Applications running on virtual machines.

</td><td>

Application Template\[sn\_cmp\_application\_template\]

</td></tr><tr><td>

Compute profile

</td><td>

A compute profile specifies the hardware to use for newly-provisioned virtual machines. Attributes: The size of computing resources, including the virtual CPUs, memory, and local storage.

</td><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td></tr><tr><td>

Compute Security Group profile

</td><td>

A compute security group profile applies specified security rules to newly-provisioned resources. You map a compute security group profile to a cloud account, a datacenter, a Compute Security Group template, and security rules for the template. Attributes: Firewall rules, such as enabling HTTP and HTTPS.

</td><td>

Compute Security Group Template

 \[cmdb\_ci\_security\_grp\_template\]

</td></tr><tr><td>

OS profile

</td><td>

An OS profile installs a specified image on a newly-provisioned virtual machine. You map an OS profile to a cloud account, a location \(datacenter\), an image template, and a cloud script. Attributes: Operating system images, including the OS type and version, the root device type, and the image source.

</td><td>

Image\[cmdb\_ci\_os\_template\]

</td></tr><tr><td>

Schedule profile

</td><td>

You map a schedule profile to an instance schedule. The schedule profile applies to all newly-provisioned resources that use the profile. For example, a schedule profile can specify the days of the week and times of day when a stack should start and stop. Attributes: Schedule attributes such as when a stack should be started, stopped, or deprovisioned.

</td><td>

N/A

</td></tr></tbody>
</table>-   **[Create an application profile](../task/create-app-profile.md)**  
An application profile specifies application software to install on newly-provisioned resources. Users can select applications when they request a stack. Use application profiles when you integrate with configuration management \(continuous delivery\) providers such as Ansible playbooks.
-   **[Create a compute profile](../task/create-compute-profile.md)**  
A compute profile specifies the hardware to use for newly-provisioned virtual machines. A compute profile maps to a cloud account, a datacenter, and a hardware template.
-   **[Create a compute security group profile](../task/create-compute-security-profile.md)**  
A compute security group profile applies specified security rules to newly-provisioned resources. You map a compute security group profile to a cloud account, a datacenter, a Compute Security Group template, and security rules for the template.
-   **[Create an OS profile](../task/create-os-profile.md)**  
An OS profile installs a specified image on a newly-provisioned virtual machine. You map an OS profile to a cloud account, a location \(datacenter\), an image template, and a cloud script. OS profiles are provider-agnostic and you can use the same profile for multiple cloud accounts.
-   **[Create a schedule profile](../task/create-schedule-profile.md)**  
You map a schedule profile to an instance schedule. The schedule profile applies to all newly-provisioned resources that use the profile. For example, a schedule profile can specify the days of the week and times of day when a stack should start and stop.
-   **[Add credentials to an image template](../task/add-credential-to-template-type.md)**  
When you add credentials to an image template, the credentials are inherited by all VMs that are provisioned using the template.
-   **[Add an AWS public image to Cloud Provisioning and Governance](../task/add-public-image-aws.md)**  
You can make any AWS image selectable in an OS profile.
-   **[Add an Azure public image to Cloud Provisioning and Governance](../task/add-public-image-azure.md)**  
You can make any Azure image selectable in an OS profile.

**Parent Topic:**[Cloud Admin Portal](cloud-admin-portal.md)

**Related topics**  


[Discover all datacenters in a service account on-demand](../../cloud-management-v2-setup/task/disco-datacntrs-in-srv-acct.md)

