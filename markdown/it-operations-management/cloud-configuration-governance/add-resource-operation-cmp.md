---
title: Add a resource operation to the execution plan
description: The base system includes a large set of predefined resource operations. Rarely, you might add a custom operation for a resource.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Build a Cloud Provisioning blueprint, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add a resource operation to the execution plan

The base system includes a large set of predefined resource operations. Rarely, you might add a custom operation for a resource.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## Procedure

1.  While working in the blueprint designer, click the **Operations** tab and select the appropriate blueprint operation.

    As an example, you may select the **Provision** operation.

2.  Click **Add**.

    The Add Resource Operation dialog box appears.

3.  Fill in the form fields \(as shown in the table\).

<table id="table_n2g_2dk_xy"><tbody><tr><td>

Resource

</td><td>

Select a resource to perform the operation on.

</td></tr><tr><td>

Interface

</td><td>

Select an interface for the resource.

</td></tr><tr><td>

Operation

</td><td>

Select an operation to perform for the step. By default, **Provision**, **Stop**, **Start** and **Deprovision** are provided. You at least need a provision operation for a user to order a cloud catalog item.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The new operation is added to the operation graph. The system adds the appropriate parameters for the operation.

5.  Click the **Create Form Parameter** check box to select a parameter.

    Parameters differ for each operation. Enter a mapping expression for the selected parameter in the **Mapping** field. See [Using expressions in Cloud Provisioning and Governance](../reference/expressions-cloud-mgt.md).

6.  Click **Save**.


**Parent Topic:**[Build a Cloud Provisioning blueprint](create-blueprint-cmp.md)

**Related topics**  


[Execute blueprint operations in parallel](execute-blueprint-operations-parallel.md)

[Blueprint attributes](../reference/blueprint-attributes.md)

[Configure a blueprint rule](configure-a-blueprint-rule.md#)

