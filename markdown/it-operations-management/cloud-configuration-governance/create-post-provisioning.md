---
title: Create post-provision operations
description: Create post-provision tasks for newly provisioned catalog items by defining subflows, scripts, CAPI calls, or resource operations. For efficiency, set up a post-provision operation, eliminating the need for manual invocation. This approach enhances time management, ensuring seamless execution of desired actions on the catalog item after resource provisioning.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create post-provision operations

Create post-provision tasks for newly provisioned catalog items by defining subflows, scripts, CAPI calls, or resource operations. For efficiency, set up a post-provision operation, eliminating the need for manual invocation. This approach enhances time management, ensuring seamless execution of desired actions on the catalog item after resource provisioning.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## About this task

You can create post-provision operations only for catalog items that are based on templates.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog Items**.

2.  Open the catalog item, click the **Post Provisioning Operation** tab, and then click **New**.

3.  On the form, fill in the fields.

<table id="table_eyh_qnw_3fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Step Type

</td><td>

Post-provision operation. Based on the post-operation you select, additional fields appear.-   CAPI:
    -   CAPI Provider
    -   CAPI Interface
    -   CAPI Method
    -   CAPI Version
-   InstanceScript:

Script: Enter the name of the script.

-   Resource:
    -   Resource Interface
    -   Interface Operation
-   Flow: Select a subflow. All active subflows in the instance are listed.

**Note:** For more information, see [Subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md).

</td></tr><tr><td>

Order

</td><td>

Order of post-provision operations. Enter the order \(in numerals\) in which you want the post-provision operation to be invoked. For example, if you enter the value 2 for CAPI and the value 3 for InstanceScript, then CAPI is invoked first and then the InstanceScript gets invoked. If you do not enter any value in this field, the system automatically enters a value in increments of 20.

</td></tr><tr><td>

Enabled

</td><td>

Option for enabling the post-provision operation you want invoked.

</td></tr></tbody>
</table>4.  Click **Submit**.

    Parameters for the post-provision operation are automatically created as operation attributes on the Manage Attributes form.

5.  To set attribute values for a post-provision operation:

    1.  Click the **Manage Attributes** related link.

        The Manage Attributes form opens.

    2.  Select the post-provision operation to update.

        All attributes for the selected operation appear in the Operations list. You can either create expression mappings \(shown in the **Mapping** column\) for an attribute or can you generate variables for an attribute. See [Manage operation attributes](manage-attributes.md) for more information.

        ![Post-provisioning attributes](../image/manage-attributes-post-provision.png)

    3.  On the Operation Attributes form, edit the values in the **Mapping** field as needed.

    4.  To set a value and not show the field to the cloud user, set **Generate Variable** to false.

        For VMware post-provision operations, you can set the following attribute values:

<table id="table_yxs_nzg_r3b"><thead><tr><th>

Attribute name

</th><th>

&lt;Value field&gt; to set in the Mapping expression

</th></tr></thead><tbody><tr><td>

NodeCredential

</td><td>

$\(capiResolver.NodeCredentialResolver\#nodeCredentialId=`<Credential SysID>`\)**Note:** You must create the credentials manually to be able to specify the sys\_id in the expression

</td></tr><tr><td>

NodeAddress

</td><td>

$\(Script:CMPVMUtils.getReachableIp\[arg=$\(Stack.items\[`<VM Name>`\].attributes\[sys\_id\]\)\]\)

</td></tr><tr><td>

ScriptExpression

</td><td>

$\{CloudScript.scripts.`<Script Name>`\}

</td></tr></tbody>
</table>    5.  Click **Apply Changes**.

        All configurations are saved and the Cloud Catalog Items page opens.


