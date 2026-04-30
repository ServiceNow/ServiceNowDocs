---
title: Define the facility hardware details
description: Define the facility hardware record to represent power, thermal, network components and their connectivity in a datacenter. By defining the facility records, you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manually create and review your network asset instances, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Define the facility hardware details

Define the facility hardware record to represent power, thermal, network components and their connectivity in a datacenter. By defining the facility records, you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

When you create a facility hardware record, it creates a corresponding configuration item \(CI\) record in the facility extension class table. To learn more about the Equipment Holder extension class table, see [Network inventory facility classes](../reference/network-inventory-facility-classes.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **All Facilities**.

3.  Select **New** and then select the facility type from the list.

    To learn more about the facility types, see [Network inventory facility classes](../reference/network-inventory-facility-classes.md).

4.  Select **Submit**.

    The Facility form is displayed for the selected facility type.

5.  On the **Details** tab, fill in the form.

    To learn more about the field information, see [Equipment Holder form](../reference/tni-equipment-holder-form-configuration.md)

6.  Create the Telecommunications Network Inventory attributes for the Facility record by selecting **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Facility form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn't appear when you reopen the CI record.

9.  Add the attachments, such as the graphics or documents, by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\).

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Telecommunications Network Inventory](../concept/telecom-network-inventory.md).

11. View the associated network inventories by selecting the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.


## What to do next

If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

**Parent Topic:**[Manually create and review your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Data model](../concept/uses-for-network-inventory-data.md)

