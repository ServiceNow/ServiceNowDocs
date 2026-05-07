---
title: Define the physical connection details
description: Review update, or create a network asset instance for the physical port connection on the interface cards in your networks. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Define the physical connection details

Review update, or create a network asset instance for the physical port connection on the interface cards in your networks. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

The physical connection data includes the link types, bandwidths, ports, sites, and topologies. When you create a physical connection record, it creates a corresponding configuration item \(CI\) record in the Physical Connection \[cmdb\_ci\_ni\_physical\_link\] table. To learn more, see [Data model](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Physical Connections**.

3.  Select **New**.

4.  On the **Details** tab, in the Physical connection section, fill in the general information for the physical connection.

    To learn more about the fields that are unique to the Physical Connection form, see [Physical Connection form](../reference/physical-connection-form.md).

    To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](../reference/commonly-used-tni-identification-fields.md).

    If you selected **Optical Fiber Cable** in the **Product Model** field, the Cable parameters form appears so that you can enter some information about the cable parameters. To learn more about the fields, see [Cable Parameters form](../reference/cable-parameters-form.md).

5.  On the **Details** tab, in the Configuration section, fill in the configuration information for the physical connection.

    To learn more about the fields that are unique to the Configuration section, see [Physical Connection form - Configuration](../reference/physical-connection-form-configuration.md).

    To learn about the remaining configuration fields that are common to most of the Inventory menu forms, see [Commonly used network asset instance configuration fields](../reference/commonly-used-tni-configuration-fields.md).

6.  To create the Telecommunications Network Inventory attributes for the Physical Connection form, select **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table as well as the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Physical Connection form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn’t appear when you reopen the CI record.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

11. To view the visual representation of the selected record, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Open Map**.

    **Note:** Install Service Graph Workspace or CMDB Workspace 3.5.0 or greater version to get this button in your instance. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0).

12. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Attribute pack for CI records](../concept/using-pack-table-ci-record.md).

13. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).

14. To view the associated network inventories, select the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Modeling your workflow](../concept/telecommunications-network-inventory-workflow.md)

