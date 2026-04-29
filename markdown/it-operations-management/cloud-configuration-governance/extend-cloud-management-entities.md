---
title: Extend Cloud Provisioning and Governance resource blocks with an override operation
description: You can extend your existing guest interface to create a new operation. You can also create a new guest interface with its own operations, parameters, and inputs.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Extend Cloud Provisioning and Governance resource blocks with an override operation

You can extend your existing guest interface to create a new operation. You can also create a new guest interface with its own operations, parameters, and inputs.

## Before you begin

Become familiar with resource block input parameters, operations, and steps. See [Configure resource block input parameters](manage-resource-block-operations.md) and [Add operation steps to a resource block](add-operation-steps.md) for instructions.

Role required: sn\_cmp.cloud\_admin

## About this task

The Cloud Provisioning and Governance application is bundled with several useful resource blocks. Create extensions to the existing resource block interfaces to add more functionality to these resource blocks. After creating an interface extension, use it in a blueprint to execute a customized operation. For example, if you do not like the way a virtual server is provisioned, extend the virtual server resource block interface by adding operations or overriding existing operations.

**Note:** Operations in resource blocks are also called operation signatures.

## Procedure

1.  Open a resource block.

2.  Change the status of the resource block from **Published** to **Draft**.

3.  Click the **Operations** tab.

4.  Click the **Override Operation** icon.

    ![Override operation icon on the upper right](../image/override-operation-override.png)

5.  Select an existing guest interface or select the **Create new** check box to create a new guest interface.

6.  If you create an interface, enter a name in the **Interface** field.

7.  Click **Submit** or **Update**.

    The new operation appears in the **Operation** list. If you create a new interface, it appears in the **Interface** list.

8.  Configure the necessary input parameters, steps, and output attributes for your new guest interface.

9.  To edit the operation or to change the access type:

    1.  Click the **Edit Operation Signature** icon.

        ![Editing an operation signature](../image/rb-edit-operation-signature.png)

    2.  Change the **Operation Type** if necessary, and add, edit, or remove input parameters at the bottom.

    3.  If you want the blueprint designer to perform the operation directly on the resource only when it is instantiated, select **Private** for the **Access Type**.

    4.  Click **Update**.

10. After completing the customizations, toggle the switch to **Published**.

11. Navigate to **Cloud Admin Portal** &gt; **Design** &gt; **Blueprints**.

12. Follow the steps in [Build a Cloud Provisioning blueprint](create-blueprint-cmp.md) to add a blueprint.

13. Click **Operations** and click the operation to modify in the resource block.

    The default resource block interface appears in the right column.

14. Click the **Edit Resource Operation** \(pencil\) icon to apply the interface extension you created.

15. Click **Submit**.

    The blueprint gets executed with the customized interface extension.


## Result

After you add this resource block to a blueprint, the parameters you added are available for you to customize.

**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

