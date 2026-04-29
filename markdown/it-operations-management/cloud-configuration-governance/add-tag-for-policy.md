---
title: Example policy action script that tags resources
description: Your instance tracks tagged resources for billing and reporting. Policy action scripts can add and modify resource tags. This example tags a storage volume resource.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Example policy action script that tags resources

Your instance tracks tagged resources for billing and reporting. Policy action scripts can add and modify resource tags. This example tags a storage volume resource.

## Before you begin

Role required: sn\_cmp.cloud\_governor or admin

## About this task

See [Create a custom tag for cloud resources](../concept/cloud-tagging.md#) for information about how to create and use tags in Cloud Provisioning and Governance.

## Procedure

1.  On the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  On the **Policy Action Scripts** tab, click **New** and then enter a unique and descriptive **Name**.

3.  Click the lookup icon for **Action Script Category**, click **New** to create a new category, and then click **Submit**.

4.  On the Policy Rule Action Script page, enter the script for the resource you want to tag.

5.  Click **Submit** to save the script.

    The script appears in the list.

6.  On the Policies tab, click **New**, enter a unique and descriptive **Name** for the policy, fill in the form with the following example settings, and then click **Save**.

<table id="table_r3l_v3h_wfb"><tbody><tr><td>

Policy Trigger

</td><td>

on Resource operation

</td></tr><tr><td>

Resource Block

</td><td>

Storage Volume

</td></tr><tr><td>

Operation

</td><td>

Storage Volume Interface.Provision

</td></tr><tr><td>

Moment

</td><td>

Pre Operation

</td></tr></tbody>
</table>7.  On the Rules related list, click **New**, enter **Add Custom Tags for Storage** for the **Name**, accept the default settings, and then click **Submit**.

8.  On the Policy Rule Actions related list, click **New**.

9.  At Execute a Script, click **Create**, fill in the form with the following example settings, and then click **Submit**.

<table id="table_vqb_rjh_wfb"><tbody><tr><td>

Action Name

</td><td>

CreateCustomTagsForStorage

</td></tr><tr><td>

Action Script Category

</td><td>

ScriptsForCustomTags

</td></tr><tr><td>

Action Script

</td><td>

AddCustomTagsForStorage

</td></tr></tbody>
</table>10. Click **Update** on the Policy Rule page.

11. Return to the Policy page and then click **Publish**.


## Result

On the Cloud Admin Portal, launch the stack that is associated with the storage resource. You can then confirm that the tags are applied.

**Parent Topic:**[Create a cloud policy](create-cloud-policy.md)

