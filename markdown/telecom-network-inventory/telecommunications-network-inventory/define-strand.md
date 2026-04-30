---
title: Define the strand details
description: Review, update, or create a network asset instance for a strand in the cable. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manually creating and reviewing your network asset instances, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Define the strand details

Review, update, or create a network asset instance for a strand in the cable. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

A strand refers to an individual conductor or wire within the cable. Cables are composed of multiple strands twisted or grouped. When you create a strand record, it creates a corresponding configuration item \(CI\) record in the Fiber Strand \[cmdb\_ci\_fiber\_strand\] table. To learn more, see [Data model for Telecommunications Network Inventory](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Strands**.

3.  Select **New** and then select the **Optical Fiber Strand** from the list.

4.  On the **Details** tab, fill in the fields.

    To learn more about the fields, see [Strand form](../reference/strand-form.md).

5.  Create the Telecommunications Network Inventory attributes for the Strand form by selecting **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table as well as the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

7.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Strand form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn’t appear when you reopen the CI record.

8.  Add the attachments, such as graphics or documents, by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

9.  Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

10. View the visual representation of the selected record by selecting the **Open Map** button.

    **Note:** Install CMDB Workspace 3.5.0 or greater version to get this button in your instance. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0).

11. Capture the attributes for a configuration item \(CI\) record by selecting **Add Packs**.

    To learn more, see [Using an attribute pack for a CI record](../concept/using-pack-table-ci-record.md).

12. View the associated network inventories by selecting the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.


**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Modeling your Telecommunications Network Inventory workflow](../concept/telecommunications-network-inventory-workflow.md)

