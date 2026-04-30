---
title: Add an operation to a resource block to use with a workflow
description: You can select from the existing operations in a resource block to work with your workflow or you can create a custom operation.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add operation steps to a resource block, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add an operation to a resource block to use with a workflow

You can select from the existing operations in a resource block to work with your workflow or you can create a custom operation.

## Before you begin

Role required: Cloud designer or admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Select a resource block, for example **Virtual Server**.

3.  Move the state of the resource block from **Published** to **Draft** to make it editable.

4.  Select the **Operations** tab.

5.  From the Interface drop-down field, select an interface that is available to the user.

    The default interface is **Virtual Server Interface**.

6.  Click **+** to the right of the Operation field, and perform these steps in the Add Operation dialog:

    1.  Enter a meaningful and unique name.

    2.  Select an operation from the Operation Type drop-down.

    3.  Select **Public** from the Access Type field.

7.  Fill in the form, and then click **Submit**.

<table id="table_b5p_hk1_bgb"><tbody><tr><td>

Operation Type

</td><td>

Select the operation to perform.

</td></tr><tr><td>

Access Type

</td><td>

For the user to see the operation at the Resources level during provisioning, select **Public**. Operations set to **Private** are not visible during provisioning.

</td></tr></tbody>
</table>    The operation is available on the resource when you select the resource for your workflow.


## What to do next

[Add a resource operation step to invoke a workflow](add-resource-op-step-invoke-wrkflw.md)

**Parent Topic:**[Add operation steps to a resource block](add-operation-steps.md)

