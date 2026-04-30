---
title: Map a script to an OS profile
description: To execute scripted actions during VM provisioning, you can map a script to an OS profile. The script runs on VMs that are created based on the image template in the OS profile.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Cloud scripts and cloud script templates, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Map a script to an OS profile

To execute scripted actions during VM provisioning, you can map a script to an OS profile. The script runs on VMs that are created based on the image template in the OS profile.

## Before you begin

Role required: sn\_cmp.cloud\_admin

You must have a cloud account with datacenters. You must run Discovery on the service accounts to populate the datacenters.

## About this task

In this procedure, you specify an existing script. See [Create cloud initialization script templates and a script](create-cloud-init-template-and-script.md).

**Note:** Profile mappings that specify more details run first. For example, a mapping that specifies a blueprint, OS profile, and resource alias takes precedence over a mapping that specifies only an OS profile.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Profiles**.

2.  In the **Profiles** list, select **OS Profile** and then open the profile.

3.  On the Cloud Script OS Profile Mappings related list, click **New** and then fill in the form.

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
</table>4.  Right-click the form header and select **Save**.

    The **Name** attribute `[scriptName]` appears in the OS Profile Mapping Overrides list.

5.  In the OS Profile Mapping Overrides list, enter an attribute name and value to use when the resource is provisioned.


**Related topics**  


[Create an OS profile](create-os-profile.md)

