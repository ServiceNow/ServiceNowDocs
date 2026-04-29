---
title: Define the cable details
description: Review, update, or create a network asset instance for the cable connecting the various sites within your network. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Define the cable details

Review, update, or create a network asset instance for the cable connecting the various sites within your network. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

Optical fiber cables are installed between sites with open endpoints, indicating that the cables don’t terminate directly on equipment. The cables are pulled through utility holes and spliced together to extend the connection between sites, depending on the distance requirements. When you create a cable record, it creates a corresponding configuration item \(CI\) record in the Fiber Optical Cable \[cmdb\_ci\_fiber\_optical\_cable\] table. To learn more, see [Data model](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Cables**.

3.  Select **New** and then select the **Optical Fiber Cable** from the list.

4.  On the **Details** tab, fill in the fields.

    To learn more about the fields in the Cable form, see [Cable form](../reference/cable-form.md).

5.  To create the Telecommunications Network Inventory attributes for the Cable form, select **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table as well as the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

7.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Cable form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn’t appear when you reopen the CI record.

8.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

9.  Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

10. To view the visual representation of the selected record, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Open Map**.

    **Note:** Install Service Graph Workspace or CMDB Workspace 3.5.0 or greater version to get this button in your instance. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0).

11. Capture the attributes for a configuration item \(CI\) record by selecting **Add Packs**.

    To learn more, see [Attribute pack for CI records](../concept/using-pack-table-ci-record.md).

12. To view the associated network inventories, select the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.


**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Model your workflow](../concept/telecommunications-network-inventory-workflow.md)

