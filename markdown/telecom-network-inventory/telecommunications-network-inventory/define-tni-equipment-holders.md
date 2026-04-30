---
title: Define the equipment holders
description: Define the equipment holder that contains your telecommunications equipment, including the cabinets, racks, shelves, and slots. By defining the equipment holders, you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manually create and review your network asset instances, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Define the equipment holders

Define the equipment holder that contains your telecommunications equipment, including the cabinets, racks, shelves, and slots. By defining the equipment holders, you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

When you create an equipment holder record, it creates a corresponding configuration item \(CI\) record in the Equipment Holder extension class table. To learn more about the Equipment Holder extension class table, see [Equipment holder extension classes](../reference/equipment-holder-types.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Equipment Holders**.

3.  Select **New** and then select the equipment holder type from the list.

    To learn more about the equipment holder types, see [Equipment holder extension classes](../reference/equipment-holder-types.md).

4.  Select **Submit**.

    The inventory form is displayed for the selected equipment holder type.

5.  On the **Details** tab, fill in the form.

    To learn more about the field information, see [Equipment Holder form](../reference/tni-equipment-holder-form-configuration.md)

6.  Create the [Telecommunications Network Inventory](../concept/telecom-network-inventory.md) attributes for the Equipment Holder form by selecting **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a [Telecommunications Network Inventory](../concept/telecom-network-inventory.md) CI record.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the [Telecommunications Network Inventory](../concept/telecom-network-inventory.md) attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Select **Save**.

    The [Telecommunications Network Inventory](../concept/telecom-network-inventory.md) attribute fields are displayed on the Equipment Holder form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn't appear when you reopen the CI record.

9.  Add the attachments, such as the graphics or documents, by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Telecommunications Network Inventory](../concept/telecom-network-inventory.md).

11. View the associated network inventories by selecting the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.

12. View the visual representation of the selected record by selecting **Open Map**.

    **Note:** Install Service Graph Workspace or CMDB Workspace 3.5.0 or a later version to get this button in your instance. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0).

13. To view the Dependency views map, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the specific network asset and the relationships between the CIs.

14. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Attribute pack for CI records](../concept/using-pack-table-ci-record.md).

15. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Manually create and review your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Model your workflow](../concept/telecommunications-network-inventory-workflow.md)

