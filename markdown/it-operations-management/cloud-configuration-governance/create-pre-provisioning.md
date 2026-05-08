---
title: Create pre-provisioning operations
description: Pre-provisioning operations streamline catalog item deployment by automating tasks like notifications, workflows, or scripts before provisioning. Configuring these operations eliminates manual steps, saving time and effort as the system automatically executes specified actions when a provisioning request is submitted, such as notifying users about the impending item provisioning process.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create pre-provisioning operations

Pre-provisioning operations streamline catalog item deployment by automating tasks like notifications, workflows, or scripts before provisioning. Configuring these operations eliminates manual steps, saving time and effort as the system automatically executes specified actions when a provisioning request is submitted, such as notifying users about the impending item provisioning process.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer.

## About this task

You can create pre-provisioning tasks only for catalog items that are based on templates.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog Items**.

2.  Open a catalog item, click the **Pre Provisioning Operation** tab, click **New**, and then fill in the form.

<table id="table_eyh_qnw_3fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Step Type

</td><td>

Pre-provisioning operation. Based on the type of pre-provisioning operation you select, additional fields appear. -   CAPI:
    -   CAPI Provider
    -   CAPI Method
    -   CAPI Version
-   InstanceScript:

Script: Enter the name of the script.

-   Resource:
    -   Resource Interface
    -   Interface Operation
-   Flow: Select a subflow. All active s in the instance are listed.

**Note:** For more information, see Subflows.

</td></tr><tr><td>

Order

</td><td>

Order of pre-provisioning operation. Enter the order that pre-provisioning operation should be invoked. Lower numbers are invoked first. For example, if you enter 2 for CAPI and 3 for InstanceScript, then CAPI is invoked first and then the InstanceScript gets invoked. If you do not enter any value in this field, the system automatically enters a value in increments of 20.

</td></tr><tr><td>

Enabled

</td><td>

Option for enabling the pre-provision operation you want invoked.

</td></tr></tbody>
</table>3.  Click **Submit**.

    Parameters for the pre-provisioning operations are created as operation attributes in the Manage Attributes page.

4.  To add values for the pre-provision operation attributes, click **Manage Attributes**.

    The Manage Attributes screen appears.

5.  Click **PreProvision**.

    All attributes for the pre-provision operation are listed.

    ![Attributes for pre-provision operation.](../image/manage-attributes.png)

6.  Either create expression mappings for an attribute \(in the **Mapping** field\) or generate variables for an attribute.

    See [Manage operation attributes](manage-attributes.md) for more information.

7.  Click **Apply Changes**.

    All the configurations you made to the attributes are saved and you are returned to the Cloud Catalog Items screen.


