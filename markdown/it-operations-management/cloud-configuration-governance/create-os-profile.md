---
title: Create an OS profile
description: An OS profile installs a specified image on a newly-provisioned virtual machine. You map an OS profile to a cloud account, a location \(datacenter\), an image template, and a cloud script. OS profiles are provider-agnostic and you can use the same profile for multiple cloud accounts.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create an OS profile

An OS profile installs a specified image on a newly-provisioned virtual machine. You map an OS profile to a cloud account, a location \(datacenter\), an image template, and a cloud script. OS profiles are provider-agnostic and you can use the same profile for multiple cloud accounts.

## Before you begin

-   You must have a cloud account with datacenters. You must run Discovery on the service accounts to populate the datacenters.
-   Role required: sn\_cmp.cloud\_admin

## About this task

**Note:** Profile mappings that specify more details run first. For example, a mapping that specifies a blueprint, OS profile, and resource alias takes precedence over a mapping that specifies only an OS profile.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Profiles**.

2.  In the **Profiles** list, select **OS Profile** and then click **New**.

3.  Enter a unique and descriptive **Name** and **Description** for the profile and then click **Submit**.

    The profile is created.

4.  Map the profile to a template.

    1.  In the list, click the profile that you created.

    2.  In the **OS Profile Mappings** related list, click **New**, fill in the form, and then click **Submit**.

        ![OS profile mappings](../image/os-profile-mapping.png)

<table id="table_nd2_k3r_h2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud Account

</td><td>

Select the cloud account to map the OS profile to.

</td></tr><tr><td>

Location

</td><td>

Select a datacenter in the cloud account.

</td></tr><tr><td>

Image Template \[cmdb\_ci\_os\_template\]

</td><td>

Select an image template that the profile should be mapped to. Click the reference icon \(![Reference icon](../../../common/image/icon-reference.png)\) to view the details of the template.

 **Important:** Do not create a new image template. Image templates must be discovered from the Cloud Accounts page on the Cloud Admin Portal \(**Manage** &gt; **Cloud Accounts**\).

 When you add credentials to an image template, the credentials are inherited by all VMs that are provisioned using the template. See [Add credentials to an image template](add-credential-to-template-type-1.md).

</td></tr></tbody>
</table>5.  Map the profile to a cloud script. In this procedure, you specify an existing script. See [Create cloud initialization script templates and a script](create-cloud-init-template-and-script.md).

    1.  On the Cloud Script OS Profile Mappings related list, click **New** and then fill in the form.

<table id="table_xrk_qsj_jfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Blueprint\[Optional\]

</td><td>

Select a blueprint to limit the script to a specific resource block used in the blueprint.

</td></tr><tr><td>

Cloud script

</td><td>

Select a cloud script to map the OS profile to.

</td></tr><tr><td>

Active

</td><td>

Select the check box if the cloud script should be run after the virtual machine is provisioned.

</td></tr><tr><td>

Application

</td><td>

Cloud Provisioning and Governance is auto-selected.

</td></tr><tr><td>

OS profile

</td><td>

If you specify a blueprint, the cloud script is run when the blueprint is provisioned.

</td></tr><tr><td>

Resource Alias\[Optional\]

</td><td>

If you specify a resource alias for the blueprint, then the cloud script is executed when the blueprint with the specified resource alias is provisioned.

</td></tr></tbody>
</table>    2.  Right-click the form header and select **Save**.

        The **Name** attribute `[scriptName]` appears in the OS Profile Mapping Overrides list.

    3.  In the OS Profile Mapping Overrides list, enter an attribute name and value to use when the resource is provisioned.


