---
title: Review and update the telecommunications equipment details
description: Review and update a network asset instance for your telecommunications equipment. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create a telecommunications equipment instance, Manually create and review your network asset instances, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Review and update the telecommunications equipment details

Review and update a network asset instance for your telecommunications equipment. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

You create the equipment form. To learn more, see [Create a telecommunications equipment instance](define-equipment-type.md).

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **All Equipment**.

    The All Equipment window lists the configuration item \(CI\) records, which have an inventory category set as Equipment.

3.  Select the CI record that you want to update.

4.  On the **Details** tab, fill in the fields.

    The following table lists the fields that are unique to the Telco Equipment form.

    To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](../reference/commonly-used-tni-identification-fields.md).

    |Field|Description|
    |-----|-----------|
    |Name|Name of this telecommunications equipment. The ServiceNow AI Platform uses this name to identify it in your network inventory.|
    |Product model|Name of the product model that this telco equipment belongs to. Select the search icon \(![Search icon.](../image/search.png) \) and select a model. To learn more, see [Create an equipment model](create-equipment-models.md).|

5.  On the **Details** tab, in the Configuration section, fill in the configuration information for the telco equipment.

    To learn more about the fields that are unique to the Configuration section in the Telco Equipment form, see [Telco Equipment form](../reference/tni-equipment-form-configuration.md).

    To learn about the remaining configuration fields that are common to most of the Inventory menu forms, see [Commonly used network asset instance configuration fields](../reference/commonly-used-tni-configuration-fields.md).

6.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Telco Equipment form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn’t appear when you reopen the CI record.

7.  Add the attachments, such as the graphics or documents by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

8.  Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

9.  To view the Dependency Views map, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the network asset and the relationships between the CIs.

10. View the visual representation of the selected record by selecting the **Open Map** button.

    **Note:** Install Service Graph Workspace or CMDB Workspace 3.5.0 or a later version to get this button in your instance. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0).

11. View the associated network inventories by selecting the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.


## What to do next

If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

**Parent Topic:**[Create a telecommunications equipment instance](define-equipment-type.md)

**Related topics**  


[Model your workflow](../concept/telecommunications-network-inventory-workflow.md)

